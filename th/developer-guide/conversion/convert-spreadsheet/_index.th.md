---
title: "Aspose.Cells Cloud Web API - แปลงไฟล์สเปรดชีตเป็นรูปแบบอื่น - เครื่องมือออนไลน์ฟรี"
second_title: "เอกสาร"
ArticleTitle: "วิธีการแปลงไฟล์สเปรดชีตเป็นรูปแบบอื่น: คู่มือทีละขั้นตอน"
linktitle: "แปลงสเปรดชีต"
type: docs
url: /th/convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, การแปลงสเปรดชีต, Excel เป็น PDF, Excel API, การแปลงไฟล์บนคลาวด์"
description: "แปลงไฟล์สเปรดชีตเป็นรูปแบบอื่นโดยใช้ Aspose.Cells Cloud API"
weight: 100
---

แปลงไฟล์สเปรดชีต/Excel ที่อยู่ในเครื่องของคุณเป็นรูปแบบอื่นผ่าน Aspose.Cells Cloud Web API

## **API แปลงสเปรดชีต**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### **พารามิเตอร์คำขอ:**

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTPBody | คำอธิบาย                                                                                      |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------- |
| Spreadsheet    | ไฟล์   | FormData                   | อัปโหลดไฟล์สเปรดชีตที่ต้องการแปลง                                                           |
| format         | สตริง | Query                      | (จำเป็น) รูปแบบเอาต์พุตที่ต้องการ (เช่น "XLSX", "PDF", "CSV")                                  |
| outPath        | สตริง | Query                      | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่จะบันทึกสมุดงานที่แปลงแล้ว ค่าเริ่มต้นคือ null                |
| outStorageName | สตริง | Query                      | ระบุชื่อพื้นที่จัดเก็บสำหรับไฟล์เอาต์พุต                                                       |
| fontsLocation  | สตริง | Query                      | ใช้ฟอนต์ที่กำหนดเองสำหรับสเปรดชีต                                                             |
| region         | สตริง | Query                      | ระบุการตั้งค่าภูมิภาคของสเปรดชีต                                                              |
| password       | สตริง | Query                      | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีตหากไฟล์นั้นมีการป้องกันไว้                                    |

### **คำตอบ (Response)**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**สถานะความสำเร็จ**

- **200 OK** – การแปลงสำเร็จ และเนื้อหาใน response body จะประกอบด้วยสตรีมของไฟล์ที่แปลงแล้ว
- ส่วนหัว `Content-Type` จะสะท้อน MIME type ของรูปแบบเอาต์พุตที่ร้องขอ (เช่น `application/pdf` สำหรับ PDF)

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย               | คำอธิบาย                                                          |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | กรองข้อมูลสำเร็จ; response ประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request           | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ไม่รองรับ)              |
| 401  | Unauthorized          | JWT token ไม่ถูกต้องหรือขาดหาย                                     |
| 413  | Payload Too Large     | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                |
| 500  | Internal Server Error | ข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                              |

## รูปแบบเอาต์พุต

| **รูปแบบเอาต์พุต**                                                                                     | **คำอธิบาย**                                                                                                               |
| :--------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>             | Excel 95/5.0 - 2003 Workbook                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>           | รูปแบบไฟล์ Office Open XML SpreadsheetML                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>           | Excel Binary Workbook                                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>           | Excel Macro-Enabled Workbook                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>             | Excel 97 - Excel 2003 Template                                                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>           | Excel Template                                                                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>           | Excel Macro-Enabled Template                                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>           | ไฟล์ Add-In ของ Excel ที่รองรับมาโคร ใช้เพื่อเพิ่มฟังก์ชันใหม่ให้กับ Excel                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>             | ไฟล์ CSV (Comma Separated Value)                                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>             | ไฟล์ TSV (Tab-separated values)                                                                                            |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>         | ไฟล์ข้อความธรรมดาที่คั่นด้วยเครื่องหมายกำกับ                                                                              |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                   | รูปแบบ HTML                                                                                                                |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                 | ไฟล์ MHTML                                                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>             | ODS (OpenDocument Spreadsheet)                                                                                             |
| SpreadsheetML                                                                                        | ไฟล์ Excel 2003 XML                                                                                                        |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>     | เอกสารที่สร้างด้วยแอปพลิเคชัน "Numbers" ของ Apple ซึ่งอยู่ในชุด iWork สำหรับ macOS และ iOS                               |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                   | JavaScript Object Notation                                                                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>             | Data Interchange Format                                                                                                    |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                | ไฟล์ที่มีนามสกุล .dbf เป็นไฟล์ฐานข้อมูลที่ใช้ในระบบจัดการฐานข้อมูล dBASE                                                  |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                         | Adobe Portable Document Format                                                                                             |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | รูปแบบ XML Paper Specification                                                                                             |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | รูปแบบ Scalable Vector Graphics                                                                                            |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                 | Tagged Image File Format                                                                                                   |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                   | รูปแบบ Portable Network Graphics                                                                                           |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                   | รูปแบบ Bitmap Image                                                                                                        |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                   | รูปแบบ Enhanced Metafile                                                                                                   |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                 | JPEG เป็นรูปแบบภาพที่บีบอัดแบบ lossy                                                                                      |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                   | Graphics Interchange Format                                                                                                |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>     | แสดงถึงเอกสาร Markdown                                                                                                     |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>             | รูปแบบที่ใช้ XML ซึ่งใช้ใน OpenOffice และ StarOffice                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>           | รูปแบบ Open Document ที่จัดเก็บในรูปแบบ XML แบบแบน                                                                         |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>       | รูปแบบที่เป็นที่รู้จักกันดีสำหรับเอกสาร Microsoft Word ซึ่งรวมไฟล์ XML และไบนารีไว้ด้วยกัน                                  |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>          | รูปแบบ PPTX ใช้พื้นฐานจาก Microsoft PowerPoint Open XML presentation file format                                         |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>         | Structured Query Language                                                                                                  |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                | XHTML เป็นรูปแบบไฟล์ข้อความที่ใช้ markup ในรูปแบบ XML โดยอ้างอิงจาก HTML 4.0                                               |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                | ไฟล์ที่มีนามสกุล .epub เป็นรูปแบบหนังสือดิจิทัลที่ให้มาตรฐานการเผยแพร่เนื้อหาดิจิทัลสำหรับผู้เผยแพร่และผู้บริโภค         |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                    | XML ย่อมาจาก Extensible Markup Language; มีลักษณะคล้าย HTML แต่ใช้แท็กเพื่อกำหนดวัตถุ                                      |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>             | ไฟล์ Open Document Template Sheet (OTS)                                                                                   |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                | AZW เป็นรูปแบบไฟล์หนังสือดิจิทัลที่พัฒนาโดย Amazon สำหรับอุปกรณ์ Kindle AZW3 หรือที่เรียกอีกอย่างว่า Kindle Format 8 (KF8) |

## คุณควรใช้ Convert Spreadsheet API ที่ไหน?

- **การย้ายระบบเก่า**: แปลงไฟล์ XLS แบบเก่าหลายพันไฟล์เป็น XLSX เพื่อใช้กับระบบสมัยใหม่
- **การมาตรฐานไฟล์เก็บถาวร**: ทำให้รูปแบบสเปรดชีตต่างๆ (XLS, XLSM, ODS, CSV) อยู่ในรูปแบบเดียวกันเพื่อการเก็บถาวร
- **ความเข้ากันได้กับชุดแอปพลิเคชันสำนักงาน**: แปลงไฟล์ Excel เป็นรูปแบบที่ใช้ได้กับ LibreOffice, Google Sheets หรือ Apple Numbers
- **การมาตรฐานแหล่งข้อมูล**: แปลงสเปรดชีตรูปแบบต่างๆ เป็น CSV หรือ JSON เพื่อนำเข้าสู่ฐานข้อมูล
- **การเผยแพร่บนเว็บ**: แปลงโมเดลการเงินเป็น HTML เพื่อแสดงผลบนเว็บ

## ทำไมคุณควรใช้ Convert Spreadsheet API?

- **เป็นมิตรกับนักพัฒนา**: Aspose.Cells Cloud มี SDK ให้ใช้งานในหลายภาษา ทำให้พัฒนาได้อย่างรวดเร็ว และมีเอกสารประกอบอย่างครบถ้วน เมื่อเทียบกับการสร้างโซลูชันสำหรับเรนเดอร์กราฟิกด้วยตนเอง ซึ่งช่วยลดภาระงานพัฒนาลงอย่างมาก
- **ประหยัดต้นทุน**: คุณสามารถแปลงข้อมูลในตารางได้โดยไม่จำเป็นต้องอัปโหลดสมุดงานก่อน ซึ่งช่วยประหยัดพื้นที่จัดเก็บและลดค่าใช้จ่าย
- **รองรับรูปแบบได้ครบถ้วน**: แปลงระหว่างรูปแบบสเปรดชีตมากกว่า 20 รูปแบบ
- **คงความถูกต้องของข้อมูลและรูปแบบ**

## วิธีใช้ Convert Spreadsheet API ผ่าน SDK?

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีใช้ Convert Spreadsheet API ผ่าน SDK ต่างๆ

### ข้อกำหนด Convert Spreadsheet API

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">ข้อกำหนด Convert Spreadsheet API</a> กำหนด programming interface ที่เข้าถึงได้แบบสาธารณะ ซึ่งคุณสามารถใช้ REST API โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่าน command-line เพื่อเข้าถึง Aspose.Cells web services ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา เนื่องจาก SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถแปลงไฟล์สเปรดชีตเป็นรูปแบบอื่นได้ด้วยโค้ดที่กระชับ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "แปลงไฟล์สเปรดชีตเป็นรูปแบบอื่นโดยใช้ Aspose.Cells Cloud",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "แปลงสเปรดชีตเป็นรูปแบบที่ระบุ"
    }
  ]
}
</script>