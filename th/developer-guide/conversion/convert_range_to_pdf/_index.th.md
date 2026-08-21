---
title: "ConvertRangeToPdf"
ArticleTitle: "การแปลงช่วงข้อมูลเป็น PDF – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktitle: "ConvertRangeToPdf"
type: docs
url: /cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, แปลงช่วงข้อมูลเป็น PDF, API"
description: "แปลงช่วงข้อมูลที่ระบุของไฟล์สเปรดชีตเป็น PDF โดยใช้ Aspose.Cells Cloud"
weight: 1
---

## ConvertRangeToPdf ของเว็บเซอร์วิส Aspose.Cells Cloud

แปลงช่วงข้อมูลของไฟล์สเปรดชีตที่อยู่บนไดรฟ์ในเครื่องเป็นไฟล์ PDF

### จุดสิ้นสุดของเว็บ API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|--------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ไฟล์   | FormData                    | อัปโหลดไฟล์สเปรดชีต |
| worksheet        | สตริง | Query                       | ชื่อชีตของสเปรดชีต |
| range            | สตริง | Query                       | พื้นที่ของเซลล์ เช่น A1:C10 |
| outPath          | สตริง | Query                       | (ไม่บังคับ) พาธของโฟลเดอร์ที่จัดเก็บสมุดงาน โดยค่าเริ่มต้นเป็นค่า null |
| outStorageName   | สตริง | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| fontsLocation    | สตริง | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| AutoRowsFit      | ค่าบูลีน| Query                       | (ไม่บังคับ) ปรับขนาดความสูงของแถวทั้งหมดในชีตอัตโนมัติ |
| AutoColumnsFit   | ค่าบูลีน| Query                       | (ไม่บังคับ) ปรับขนาดความกว้างของคอลัมน์ทั้งหมดในชีตอัตโนมัติ |
| region           | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสเปรดชีต (เช่น `en-US`, `fr-FR`) มีผลต่อรูปแบบตัวเลข การแยกวิเคราะห์วันที่ และพฤติกรรมเฉพาะของภูมิภาค |
| password         | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สเปรดชีต |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ประเภท | คำอธิบาย |
|----------------|------|-------------|
| Spreadsheet    | ไฟล์ | อัปโหลดไฟล์สเปรดชีต |

### **การตอบกลับ**

```json
{
  "file": "<เนื้อหา PDF แบบไบนารี>"
}
```

**โค้ดสถานะการตอบกลับ**

| โค้ด | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ (OK) | การแปลงเสร็จสมบูรณ์ ส่งคืนสตรีมไฟล์ PDF ที่สร้างขึ้น |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | URL ไม่ถูกต้อง |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | การยืนยันตัวตนล้มเหลว หรือไม่ได้ระบุข้อมูลการยืนยันตัวตน |
| 413 | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | สเปรดชีตมีข้อผิดพลาดในการดึงข้อมูลสำหรับการแปลง |

## วิธีการใช้งาน ConvertRangeToPdf ด้วย SDK

### ข้อมูลเฉพาะของ ConvertRangeToPdf

[ข้อมูลเฉพาะของ API ConvertRangeToPdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้สาธารณะ และช่วยให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<เนื้อหา PDF แบบไบนารี>"
}
```

{< /tab >}

{< /tabs >}

### การใช้งาน Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose Cells Cloud โดยใช้ SDK ต่างๆ:
```csharp
// ตัวอย่างโค้ด SDK สำหรับ C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// ตัวอย่างโค้ด SDK สำหรับ Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# ตัวอย่างโค้ด SDK สำหรับ Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// ตัวอย่างโค้ด SDK สำหรับ JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---