---
title: "การแปลงตารางเป็น PDF"
ArticleTitle: "การแปลงตารางเป็น PDF – Aspose.Cells Cloud API"
second_title: "เอกสาร"
linktype: "docs"
url: "/cells/convert/table/pdf"
aliases: []
keywords: "แปลงตารางเป็น PDF, Aspose.Cells, API"
description: "แปลงตารางของสมุดงานที่อยู่ในไดรฟ์ท้องถิ่นเป็นไฟล์ PDF โดยใช้ Aspose.Cells Cloud"
weight: 1000
---

## การแปลงตารางเป็น PDF ของบริการเว็บ Aspose.Cells Cloud

การดำเนินการนี้จะอ่านไฟล์สมุดงานจากระบบไฟล์ท้องถิ่น แปลงตารางที่ระบุเป็นเอกสาร PDF และส่งคืนผลลัพธ์ที่แปลงแล้ว โดยดำเนินการทั้งหมดบนเซิร์ฟเวอร์คลาวด์ จึงไม่จำเป็นต้องอัปโหลดไฟล์ไปยังพื้นที่จัดเก็บบนคลาวด์เป็นขั้นตอนกลาง API นี้รองรับพารามิเตอร์แบบเลือกเติมสำหรับตำแหน่งที่เก็บไฟล์ผลลัพธ์ ฟอนต์ที่กำหนดเอง การปรับขนาดแถว/คอลัมน์อัตโนมัติ การตั้งค่าภูมิภาค และสมุดงานที่มีการป้องกันด้วยรหัสผ่าน

### จุดสิ้นสุดของ Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | Path/Query String/HTTP Body | คำอธิบาย |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ไฟล์   | FormData                    | อัปโหลดไฟล์สมุดงาน |
| worksheet        | สตริง | Query                       | ชื่อแผ่นงานของสมุดงาน |
| tableName        | สตริง | Query                       | ชื่อตาราง |
| outPath          | สตริง | Query                       | (ไม่บังคับ) เส้นทางโฟลเดอร์ที่เก็บสมุดงาน ค่าเริ่มต้นคือ null |
| outStorageName   | สตริง | Query                       | ชื่อพื้นที่จัดเก็บสำหรับไฟล์ผลลัพธ์ |
| fontsLocation    | สตริง | Query                       | ใช้ฟอนต์ที่กำหนดเอง |
| AutoRowsFit      | บูลีน | Query                       | (ไม่บังคับ) ปรับขนาดแถวทั้งหมดในแผ่นงานอัตโนมัติ |
| AutoColumnsFit   | บูลีน | Query                       | (ไม่บังคับ) ปรับขนาดคอลัมน์ทั้งหมดในแผ่นงานอัตโนมัติ |
| region           | สตริง | Query                       | การตั้งค่าภูมิภาค/ภาษาของสมุดงาน (เช่น `en-US`, `fr-FR`) ซึ่งมีผลต่อการจัดรูปแบบตัวเลข การแปลงวันที่ และพฤติกรรมเฉพาะของแต่ละภูมิภาค |
| password         | สตริง | Query                       | รหัสผ่านสำหรับเปิดไฟล์สมุดงาน |

### พารามิเตอร์ของเนื้อหาคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | คำอธิบาย |
|----------------|------|-------------|
| *ไม่มี* | *ไม่มี* | *ไม่จำเป็นต้องส่ง JSON body; ไฟล์จะถูกส่งผ่าน multipart/form-data* |

### **การตอบกลับ**

```json
{
  "file": "<เนื้อหา PDF แบบไบนารี>"
}
```

**รหัสสถานะของการตอบกลับ**

| รหัส | ความหมาย | คำอธิบาย |
|------|---------|-------------|
| 200 | สำเร็จ | ตารางถูกแปลงเป็น PDF สำเร็จ; เนื้อหาในส่วน response body คือสตรีมไฟล์ PDF |
| 400 | คำขอไม่ถูกต้อง | พารามิเตอร์ของคำขอไม่ถูกต้อง หรือ URL มีรูปแบบผิดพลาด |
| 401 | ไม่ได้รับอนุญาต | การยืนยันตัวตนล้มเหลว หรือไม่ได้ส่งข้อมูลยืนยันตัวตนมา |
| 404 | ไม่พบ | ไม่สามารถเข้าถึงไฟล์ต้นทาง หรือไม่พบแผ่นงาน/ตาราง |
| 413 | ข้อมูลที่ส่งมีขนาดใหญ่เกินไป | ขนาดของไฟล์สมุดงานที่อัปโหลดเกินขีดจำกัดที่อนุญาต |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ | เกิดข้อผิดพลาดขณะแปลงสมุดงานเป็น PDF |

## วิธีใช้การแปลงตารางเป็น PDF ด้วย SDK

### ข้อกำหนดของการแปลงตารางเป็น PDF

[ข้อกำหนดของ API การแปลงตารางเป็น PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) กำหนดอินเทอร์เฟซการโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST API ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}

{< tab tabNum="1" >}

```bash
# ใช้ HTTPS เพื่อการเชื่อมต่อที่ปลอดภัย
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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

### ใช้ Aspose Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะซ่อนรายละเอียดระดับต่ำไว้ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells Cloud ผ่าน SDK ต่างๆ:

```csharp
// ตัวอย่างโค้ด SDK สำหรับ C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// ตัวอย่างโค้ด SDK สำหรับ Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# ตัวอย่างโค้ด SDK สำหรับ Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---