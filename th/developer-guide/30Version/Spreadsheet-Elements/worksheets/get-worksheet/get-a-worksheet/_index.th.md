---
title: "การส่งออกชีตงานด้วย Aspose.Cells Cloud API – รูปแบบ, ตัวอย่าง cURL และ SDK"
second_title: "เอกสาร"
linktitle: "การส่งออกชีตงาน"
type: docs
url: /th/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, การส่งออกชีตงาน, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, cloud API"
description: "เรียนรู้วิธีการส่งออกชีตงานเดียวจากไฟล์ Excel โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL ที่ถูกต้อง, รายละเอียดการยืนยันตัวตน, การจัดการข้อผิดพลาด และตัวอย่างโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 10
ArticleTitle: "การส่งออกชีตงานด้วย Aspose.Cells Cloud API – รูปแบบ, ตัวอย่าง cURL และ SDK"
---

API นี้เป็น REST API ที่ช่วยให้คุณ **ส่งออกชีตงาน** จากไฟล์ Excel ไปยังรูปแบบไฟล์ต่างๆ ได้หลายรูปแบบ

**สรุป** – ใช้ endpoint **Get Worksheet** เพื่อดาวน์โหลดชีตงานเดียวจากสมุดงานในรูปแบบที่คุณเลือก

คุณสามารถส่งออกข้อมูลไปยังรูปแบบต่อไปนี้:

| รูปแบบ | นามสกุลไฟล์ | MIME Type                                                         |
|-------|-------------|-------------------------------------------------------------------|
| XLS   | .xls        | application/vnd.ms-excel                                          |
| XLSX  | .xlsx       | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB  | .xlsb       | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV   | .csv        | text/csv                                                          |
| TSV   | .tsv        | text/tab-separated-values                                         |
| XLSM  | .xlsm       | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS   | .ods        | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT   | .txt        | text/plain                                                        |
| PDF   | .pdf        | application/pdf                                                   |
| OTS   | .ots        | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS   | .xps        | application/vnd.ms-xpsdocument                                    |
| DIF   | .dif        | application/x-dif                                                 |
| PNG   | .png        | image/png                                                         |
| JPEG  | .jpeg       | image/jpeg                                                        |
| GIF   | .gif        | image/gif                                                         |
| BMP   | .bmp        | image/bmp                                                         |
| WMF   | .wmf        | image/wmf                                                         |
| TIFF  | .tiff       | image/tiff                                                        |
| EMF   | .emf        | image/emf                                                         |
| NUMBERS | .numbers  | application/vnd.apple.numbers                                     |
| FODS  | .fods       | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## ความปลอดภัยและการยืนยันตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) 

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์         | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
|--------------------------|-----------|----------|---------------------------------------------------------------------------|
| **name**                 | string    | path     | **จำเป็น** ชื่อของไฟล์ Excel                                              |
| **sheetName**            | string    | path     | **จำเป็น** ชื่อของชีตงานที่ต้องการส่งออก                                 |
| **format**               | string    | query    | รูปแบบไฟล์เป้าหมายสำหรับชีตงานที่ส่งออก (เช่น `pdf`, `png`)              |
| **verticalResolution**   | integer   | query    | ความละเอียด DPI ของภาพสำหรับรูปแบบที่รองรับการกำหนดความละเอียด (เช่น PNG, JPEG) |
| **horizontalResolution** | integer   | query    | ความละเอียด DPI ของภาพสำหรับรูปแบบที่รองรับการกำหนดความละเอียด          |
| **area**                 | string    | query    | ช่วงของเซลล์ที่ต้องการส่งออก (เช่น `A1:D10`)                             |
| **pageIndex**            | integer   | query    | ดัชนีของหน้าที่ต้องการส่งออกเมื่อชีตงานถูกแบ่งเป็นหน้า                  |
| **folder**               | string    | query    | ตำแหน่งโฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ต้นฉบับอยู่                        |
| **storageName**          | string    | query    | ชื่อของพื้นที่จัดเก็บ Aspose Cloud                                        |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> กำหนด API ที่สามารถเข้าถึงได้สาธารณะและอนุญาตให้คุณใช้งาน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง cURL เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<ข้อมูลไบนารี>
```

{{< /tab >}}

{{< /tabs >}}

## การจัดการข้อผิดพลาด

API จะส่งกลับรหัสสถานะ HTTP มาตรฐาน ซึ่งมีการตอบกลับที่พบบ่อยดังนี้:

| รหัสสถานะ | ความหมาย                                                        | ตัวอย่าง JSON Body                         |
|-----------|------------------------------------------------------------------|-------------------------------------------|
| **200**   | ความสำเร็จ – สตรีมของชีตงานจะถูกส่งกลับ                                        | `{ "stream": "..." }`                     |
| **400**   | คำขอผิดรูปแบบ – พารามิเตอร์ที่ขาดหรือไม่ถูกต้อง                               | `{ "error": "Invalid format parameter." }` |
| **401**   | ไม่ได้รับอนุญาต – JWT token ไม่ถูกต้องหรือขาดหาย                              | `{ "error": "Authentication failed." }`   |
| **404**   | ไม่พบ – ไฟล์หรือชีตงานที่ระบุไม่มีอยู่                                         | `{ "error": "Worksheet not found." }`     |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดบนเซิร์ฟเวอร์                | `{ "error": "Unexpected error." }`        |

จัดการการตอบกลับเหล่านี้ในโค้ดไคลเอนต์ของคุณเพื่อให้ข้อมูลย้อนกลับที่เหมาะสมแก่ผู้ใช้

## กลุ่ม SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และอนุญาตให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> สำหรับรายชื่อ SDK ของ Aspose.Cells Cloud อย่างละเอียด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}