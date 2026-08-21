---
title: "ส่งออกเวิร์กชีต – Aspose.Cells Cloud"
second_title: "เอกสาร"
linktitle: "เวิร์กชีต"
type: docs
url: /th/export-excel-worksheet-to-different-formats/
aliases: [  /th/export/excel-worksheet-to-different-formats/ ]
keywords: "Aspose.Cells, ส่งออกเวิร์กชีต, Excel API, PDF, CSV, TIFF, ODS, รูปแบบภาพ"
description: "เรียนรู้วิธีการส่งออกเวิร์กชีต Excel ไปยังรูปแบบต่างๆ เช่น PDF, CSV, TIFF และอื่นๆ โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL, ขั้นตอนการยืนยันตัวตนที่จำเป็น, รายละเอียดพารามิเตอร์ และการจัดการผลลัพธ์"
weight: 20
ArticleTitle: "ส่งออกเวิร์กชีต Excel ไปยังรูปแบบต่างๆ – Aspose.Cells Cloud"
---

คุณสามารถส่งออกเวิร์กชีตไปยังรูปแบบต่อไปนี้:

- **XLS** – [รายละเอียดรูปแบบ XLS](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [รายละเอียดรูปแบบ XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [รายละเอียดรูปแบบ XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [รายละเอียดรูปแบบ CSV](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [รายละเอียดรูปแบบ TSV](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [รายละเอียดรูปแบบ XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [รายละเอียดรูปแบบ ODS](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [รายละเอียดรูปแบบ TXT](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [รายละเอียดรูปแบบ PDF](https://docs.fileformat.com/pdf/)
- **OTS** – [รายละเอียดรูปแบบ OTS](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [รายละเอียดรูปแบบ XPS](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [รายละเอียดรูปแบบ DIF](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [รายละเอียดรูปแบบ PNG](https://docs.fileformat.com/Image/png/)
- **JPEG** – [รายละเอียดรูปแบบ JPEG](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [รายละเอียดรูปแบบ BMP](https://docs.fileformat.com/image/bmp/)
- **SVG** – [รายละเอียดรูปแบบ SVG](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [รายละเอียดรูปแบบ TIFF](https://docs.fileformat.com/image/tiff/)
- **EMF** – [รายละเอียดรูปแบบ EMF](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [รายละเอียดรูปแบบ Numbers](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [รายละเอียดรูปแบบ FODS](https://docs.fileformat.com/spreadsheet/fods/)

[สำรวจการดำเนินการส่งออกอื่นๆ เช่น การส่งออกสมุดงานทั้งหมดหรือกราฟ](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## API PostExport

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT</a>

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ประเภท | เส้นทาง/สตริงคำค้นหา/เนื้อหา HTTP Body | จำเป็น | คำอธิบาย |
|------------------|--------|----------------------------------------|--------|-----------|
| file             | ไฟล์   | formData                               | ใช่    | ไฟล์ที่จะอัปโหลด |
| objectType       | สตริง   | query                                  | ใช่    | ประเภทของวัตถุที่จะส่งออก สำหรับการส่งออกกราฟให้ใช้ `chart` ค่าอื่นที่เป็นไปได้คือ `worksheet`, `picture` เป็นต้น |
| format           | สตริง   | query                                  | ใช่    | รูปแบบเอาต์พุตที่ต้องการ ค่าที่รองรับ: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf` |

### ผลลัพธ์

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **การจัดการข้อผิดพลาด**

หากคำขอล้มเหลว API จะส่งคืนวัตถุข้อผิดพลาด JSON ซึ่งมีฟิลด์เช่น `Code` และ `Message` โค้ดสถานะ HTTP ที่พบบ่อย ได้แก่ **401 Unauthorized** (โทเค็นขาดหายหรือไม่ถูกต้อง) และ **400 Bad Request** (พารามิเตอร์ไม่ถูกต้อง)

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                    | คำอธิบาย |
|-----|-----------------------------|----------|
| 200 | สำเร็จ (OK)                | กรองใช้งานได้สำเร็จ; ผลลัพธ์มีรายละเอียดการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | ข้อมูลร้องขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์ |

**หมายเหตุ**

- ขนาดไฟล์สูงสุดสำหรับการอัปโหลดคือ 50 MB  
- API รองรับการส่งออกเวิร์กชีตหลายอันในคำขอเดียว โดยแต่ละเวิร์กชีตจะถูกส่งคืนเป็นไฟล์แยกในอาร์เรย์ `Files`  
- มีการประมวลผลแบบอะซิงโครนัสสำหรับสมุดงานขนาดใหญ่ ให้ใช้การตอบกลับ `202 Accepted` เพื่อตรวจสอบสถานะการดำเนินการ

## วิธีใช้ PostExport API ด้วย SDK

### ข้อกำหนดเบื้องต้น

ก่อนเรียก API คุณต้องได้รับโทเค็นการเข้าถึง JWT ที่ถูกต้องโดยใช้ขั้นตอนการยืนยันตัวตนของ Aspose.Cells Cloud ตรวจสอบให้แน่ใจว่าโทเค็นถูกใส่ไว้ในหัวข้อ `Authorization` ของการร้องขอแต่ละครั้ง SDK จะจัดการการขอรับโทเค็นให้อัตโนมัติเมื่อกำหนดค่าด้วยข้อมูลประจำตัวไคลเอนต์ของคุณ

### ข้อมูลจำเพาะ API PostExport

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

```bash
# ส่งออกเวิร์กชีตไปยังรูปแบบ TIFF
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาด้วย Aspose.Cells Cloud SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ สำหรับรายการ SDK ที่รองรับทั้งหมด โปรดเยี่ยมชม [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud)

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}