---
title: "ส่งออกภาพ"
second_title: "เอกสาร"
linktype: docs
url: /export-excel-picture-to-different-formats/
aliases: [/export/excel-picture-to-different-formats/]
keywords: "ส่งออกภาพ, Aspose.Cells Cloud, REST API, Excel, รูปแบบภาพ, PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF"
description: "ส่งออกภาพจาก Excel ไปยังรูปแบบภาพต่างๆ โดยใช้ Aspose.Cells Cloud REST API บริการนี้รองรับ SDK สำหรับภาษาโปรแกรมต่างๆ ได้แก่ C#, Java, PHP, Ruby, Node.js, Python, Perl, Go และ Swift"
weight: 20
---

คุณสามารถส่งออกภาพไปยังรูปแบบต่อไปนี้: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), และ [WMF](https://docs.fileformat.com/image/Wmf/)

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **ความปลอดภัยและการตรวจสอบสิทธิ์**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การตรวจสอบสิทธิ์แบบใช้โทเค็น JWT</a>

### พารามิเตอร์คำขอ

| พารามิเตอร์     | ตำแหน่ง | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                                                     |
| --------------- | -------- | ---------- | ------ | ------------------------------------------------------------------------------ |
| `file`          | Form‑data | ไฟล์      | ใช่    | สมุดงาน Excel (`.xlsx`, `.xls` ฯลฯ) ที่มีวัตถุ OLE                         |
| `outputFormat`  | Query    | สายอักขระ | ใช่    | รูปแบบเป้าหมายสำหรับวัตถุที่ส่งออก (`pdf`, `png`, `jpeg`, `docx`, `pptx`) |
| `objectType`    | Query    | สายอักขระ | ใช่    | ค่าคงที่คือ `oleobject`                                                      |

### การตอบกลับ

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                   | คำอธิบาย                                        |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                | ประมวลผลตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                  |
| 413  | ข้อมูลส่งออกมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์          |

## วิธีใช้ PostExport API ร่วมกับ SDKs

### ข้อมูลจำเพาะ PostExport API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเบราว์เซอร์เว็บ

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### ใช้ SDKs ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำต่างๆ ให้คุณสามารถมุ่งเน้นไปที่ตรรกะของโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกเว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}