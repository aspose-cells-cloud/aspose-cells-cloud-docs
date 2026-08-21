---
title: "อัปเดตรูปแบบของเซลล์หลายเซลล์ – เอกสารอ้างอิง API ของ Aspose.Cells Cloud (เวอร์ชัน 3.0)"
type: docs
url: /th/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "อัปเดตรูปแบบของเซลล์หลายเซลล์", "API รูปแบบเซลล์ Excel", "cloud SDK", "REST API", "ตัวอย่าง cURL", "คำขอ JSON", "การยืนยันตัวตนด้วย JWT"]
description: "เรียนรู้วิธีการอัปเดตรูปแบบของช่วงเซลล์ในสมุดงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud เวอร์ชัน 3.0 ซึ่งประกอบด้วย endpoint, วิธี HTTP, พารามิเตอร์, ตัวอย่าง cURL และ SDK, การยืนยันตัวตน, การจัดการข้อผิดพลาด และข้อมูลเวอร์ชัน"
ArticleTitle: "อัปเดตรูปแบบของเซลล์หลายเซลล์ – เอกสารอ้างอิง API ของ Aspose.Cells Cloud (เวอร์ชัน 3.0)"
---

## API REST

API REST นี้ตั้งค่า **รูปแบบ (style)** สำหรับช่วงเซลล์ในสมุดงาน Excel

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## ความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ JWT token [ดูรายละเอียดเพิ่มเติมที่นี่](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย |
|----------------|--------|----------|-------------|
| **name**       | string | path     | ชื่อสมุดงาน |
| **sheetName**  | string | path     | ชื่อแผ่นงาน |
| **range**      | string | query    | ช่วงของเซลล์ (เช่น `A1:A10`) |
| **style**      | object | body     | วัตถุ JSON ที่กำหนดรูปแบบที่จะนำไปใช้ |
| **folder**     | string | query    | โฟลเดอร์ที่เก็บสมุดงานไว้ |
| **storageName**| string | query    | ชื่อของพื้นที่จัดเก็บ |

#### วัตถุ Style
วัตถุ JSON `style` แทนการจัดรูปแบบเซลล์ ซึ่งอาจประกอบด้วยคุณสมบัติเสริมต่อไปนี้:

- **Font** – การตั้งค่าแบบฟอนต์ (`Name`, `Size`, `IsBold`, `IsItalic`, `Color` เป็นต้น)  
- **BackgroundColor** – สีพื้นหลังในรูปแบบ ARGB  
- **ForegroundColor** – สีพื้นหน้าในรูปแบบ ARGB  
- **Name**, **CultureCustom**, **Custom** – เมตาดาต้าเพิ่มเติมของรูปแบบ

## **การตอบกลับ**

ส่งคืน CellCloudResponse

- **ภาพรวมฟิลด์ของการตอบกลับ**

| ฟิลด์           | ประเภท    | คำอธิบาย                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                    |
| `Code`           | integer | 200,400,401,500,...                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                     | คำอธิบาย                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับประกอบด้วยรายละเอียดของ операции |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลที่ส่งมีขนาดใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500  | ข้อผิดพลาดภายในของเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์ |
## วิธีใช้ PostUpdateWorksheetRangeStyle API ร่วมกับ SDK

### ข้อมูลจำเพาะของ PostUpdateWorksheetRangeStyle API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) ให้โครงสร้างแบบเต็ม

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ผ่าน cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [คลังข้อมูลบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}