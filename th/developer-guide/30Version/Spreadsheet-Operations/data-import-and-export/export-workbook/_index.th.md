---
title: "ส่งออกสมุดงาน"
second_title: "เอกสาร"
linktype: "สมุดงาน"
type: docs
url: /export-excel-to-different-formats/
aliases: [/export/excel-to-different-formats/]
keywords: "Aspose.Cells Cloud, การส่งออก Excel, การแปลงสมุดงาน, PDF, CSV, JSON, รูปแบบภาพ, API สเปรดชีต, XLSX, ODS, PNG"
description: "คู่มือแบบทีละขั้นตอนเกี่ยวกับการส่งออกสมุดงาน Excel ไปยังรูปแบบต่างๆ มากมาย รวมถึง PDF, CSV, JSON และประเภทภาพต่างๆ โดยใช้ Aspose.Cells Cloud REST API และ SDK"
weight: 20
---

คุณสามารถส่งออกสมุดงานไปยังรูปแบบต่อไปนี้ได้: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | จำเป็น | คำอธิบาย |
|----------------|---------|-----------------------------|-----------|------------------------------------------------------------|
| file           | ไฟล์    | formData                    | ใช่ | ไฟล์ที่จะอัปโหลด |
| objectType     | สตริง   | query                       | ใช่ | ชนิดของออบเจกต์ที่จะส่งออก สำหรับการส่งออกชาร์ตให้ใช้ `chart` ค่าที่เป็นไปได้อื่นๆ ได้แก่ `worksheet`, `picture` เป็นต้น |
| format         | สตริง   | query                       | ใช่ | รูปแบบผลลัพธ์ที่ต้องการ ค่าที่รองรับ: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf` |

### **การตอบกลับ**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**รหัสสถานะ HTTP**

| รหัส | ความหมาย              | คำอธิบาย |
|------|-----------------------|-------------|
| 200  | สำเร็จ (OK)           | ส่งออกชape สำเร็จ; การตอบกลับมีรายชื่อไฟล์ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | เทคนิคการเข้าถึงไม่ถูกต้องหรือขาดหาย |
| 413  | พายโหลดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

## วิธีใช้ PostExport API ด้วย SDKs

### ข้อกำหนด PostExport API


[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถดำเนินการโต้ตอบ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ command-line **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API โดยใช้ cURL:

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK จะเร่งความเร็วการพัฒนาด้วยการจัดการรายละเอียดระดับล่าง ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจได้ รายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud มีอยู่ใน [GitHub repository](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}