---
title: "ส่งออกกราฟใน Excel"
second_title: "เอกสาร"
linktype: "กราฟ"
type: docs
url: /export-excel-chart-to-different-formats/
aliases: [/export/excel-chart-to-different-formats/]
description: "ส่งออกวัตถุกราฟใน Excel ไปยังรูปแบบยอดนิยมต่างๆ เช่น PNG, JPEG, PDF, SVG, TIFF, EMF, WMF และอื่นๆ โดยใช้ Aspose.Cells Cloud REST API หรือ SDK มีตัวอย่างการตรวจสอบสิทธิ์ ตัวอย่าง cURL และตัวอย่างโค้ดสำหรับหลายภาษา"
keywords: "Aspose.Cells, ส่งออกกราฟ, การส่งออกกราฟใน Excel, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, รูปแบบกราฟ, Aspose Cells Cloud"
weight: 20
ArticleTitle: "ส่งออกกราฟใน Excel – เอกสาร"
---

การส่งออกวัตถุกราฟจากสมุดงาน Excel ไปยังรูปแบบต่างๆ ทั้งภาพและเอกสาร เป็นความต้องการที่พบบ่อยในการทำรายงานและการเผยแพร่ข้อมูล Aspose.Cells Cloud มีจุดปลายทาง REST ที่เรียบง่ายซึ่งแปลงกราฟโดยตรงเป็นรูปแบบยอดนิยมต่างๆ เช่น PNG, JPEG, PDF, SVG, TIFF, EMF, WMF และอื่นๆ

คุณสามารถส่งออกกราฟไปยังรูปแบบต่อไปนี้: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), และ [PDF](https://docs.fileformat.com/pdf/)

**ข้อกำหนดเบื้องต้น:**  
- บัญชี Aspose.Cells Cloud ที่ถูกต้องและมีการสมัครสมาชิกที่ใช้งานอยู่  
- โทเค็น JWT (OAuth 2.0 Bearer token) ที่ได้รับจากการตรวจสอบสิทธิ์ตามขั้นตอนที่กำหนด  
- ไฟล์สมุดงานที่ต้องการอัปโหลด (ขนาดสูงสุด < 50 MB)  

## **API ของ REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์ด้วยโทเค็น JWT</a>

### พารามิเตอร์สำหรับคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | จำเป็น | คำอธิบาย                                                                                                                     |
|----------------|--------|-----------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| file           | ไฟล์   | formData                    | จำเป็น   | ไฟล์ที่จะอัปโหลด                                                                                                                  |
| objectType     | สายอักขระ | query                       | จำเป็น   | ชนิดของวัตถุที่จะส่งออก สำหรับการส่งออกกราฟให้ใช้ `chart` ค่าที่เป็นไปได้อื่นๆ ได้แก่ `worksheet`, `picture` เป็นต้น            |
| format         | สายอักขระ | query                       | จำเป็น   | รูปแบบของผลลัพธ์ที่ต้องการ ค่าที่รองรับ: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.                        |

### **คำตอบ**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของ оперation |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่มีสิทธิ์ (Unauthorized)                | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |
## วิธีใช้ API PostExport ด้วย SDK

### ข้อมูลกำกับ API PostExport

[ข้อมูลกำกับ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการเชื่อมต่อ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คำขอทั้งหมดต้องระบุโทเค็น OAuth 2.0 Bearer ที่ถูกต้องในส่วนหัว `Authorization` ตัวอย่างด้านล่างแสดงวิธีเรียก API ด้วย **cURL** และอัปโหลดสมุดงานโดยใช้ multipart/form‑data

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการกับรายละเอียดระดับต่ำ และช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}