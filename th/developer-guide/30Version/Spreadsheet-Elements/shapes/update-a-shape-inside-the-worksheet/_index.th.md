---
title: "อัปเดตรูปร่างในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "อัปเดต"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "อัปเดตรูปร่างผ่าน API ของ Excel, Aspose.Cells Cloud, การอัปเดตรูปร่างใน Excel, REST API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "เรียนรู้วิธีอัปเดตรูปร่างในแผ่นงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud ซึ่งประกอบด้วยปลายทาง HTTPS, รายละเอียดการยืนยันตัวตน, โครงสร้าง DTO, ขั้นตอนการใช้งานแบบเป็นขั้นตอน, ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับภาษาโปรแกรมต่างๆ"
ArticleTitle: "อัปเดตรูปร่างในแผ่นงาน Excel - Aspose.Cells Cloud API"
weight: 31
---

REST API นี้ใช้อัปเดตรูปร่างในแผ่นงาน Excel

## ความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ JWT token <sup>[[1]](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)</sup>

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์   | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                       |
| ------------------ | ---------- | -------- | ----------------------------------------------------------------------------------------------- |
| **name**           | string     | path     | ชื่อไฟล์สมุดงาน                                                                                 |
| **sheetName**      | string     | path     | ชื่อของแผ่นงานที่มีรูปร่าง                                                                      |
| **shapeindex**     | integer    | path     | ดัชนีแบบเริ่มต้นที่ 0 ของรูปร่างภายในแผ่นงาน                                                   |
| **dto**            | object     | body     | วัตถุถ่ายโอนข้อมูลของรูปร่าง (data-transfer object) ซึ่งประกอบด้วยคุณสมบัติที่อัปเดตแล้ว (ดู _โครงสร้าง DTO_ ด้านล่าง) |
| **folder**         | string     | query    | โฟลเดอร์ที่เก็บสมุดงาน                                                                         |
| **storageName**    | string     | query    | ชื่อของพื้นที่จัดเก็บบน Aspose Cloud                                                            |

### โครงสร้าง DTO

วัตถุ `dto` ประกอบด้วยคุณสมบัติที่สามารถอัปเดตได้ ฟิลด์ทั้งหมดเป็นฟิลด์ไม่บังคับ เว้นแต่จะระบุไว้เป็นอย่างอื่น

| ฟิลด์               | ชนิดข้อมูล | บังคับ | คำอธิบาย                                                                               |
| -------------------- | ---------- | ------ | --------------------------------------------------------------------------------------- |
| **Name**             | string     | ไม่    | ชื่อใหม่ของรูปร่าง                                                                      |
| **UpperLeftRow**     | integer    | ไม่    | ดัชนีแถวของมุมบนซ้ายของรูปร่าง                                                         |
| **UpperLeftColumn**  | integer    | ไม่    | ดัชนีคอลัมน์ของมุมบนซ้ายของรูปร่าง                                                    |
| **Width**            | integer    | ไม่    | ความกว้างของรูปร่าง (หน่วย: จุด)                                                       |
| **Height**           | integer    | ไม่    | ความสูงของรูปร่าง (หน่วย: จุด)                                                         |
| **RotationAngle**    | integer    | ไม่    | มุมหมุนเป็นองศา                                                                         |
| **IsHidden**         | boolean    | ไม่    | ค่า `true` เพื่อซ่อนรูปร่าง                                                             |
| **IsLocked**         | boolean    | ไม่    | ค่า `true` เพื่อล็อก rูปร่าง                                                            |
| **Font**             | object     | ไม่    | การตั้งค่าฟอนต์ (ดู OpenAPI specification สำหรับคุณสมบัติย่อย)                         |
| **...**              | …          | ไม่    | คุณสมบัติเพิ่มเติม เช่น `HtmlText`, `AlternativeText`, `ZOrderPosition` ฯลฯ           |

> สำหรับรายการที่สมบูรณ์ โปรดดูที่ OpenAPI specification อย่างเป็นทางการ: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>

### ส่วนหัวของคำขอ

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(JWT token จากขั้นตอนการ _ยืนยันตัวตน_)_

### เนื้อหาคำขอ (ตัวอย่าง)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## ตัวอย่างโดยใช้ cURL (เครื่องมือบรรทัดคำสั่ง)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### การตอบกลับ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**การจัดการข้อผิดพลาด** – API อาจส่งกลับสถานะโค้ดต่อไปนี้:

| โค้ด | ความหมาย                | สาเหตุที่พบบ่อย                                         |
| ---- | ------------------------ | -------------------------------------------------------- |
| 400  | Bad Request              | JSON ไม่ถูกต้อง หรือขาดฟิลด์ที่จำเป็น                   |
| 401  | Unauthorized             | ขาด JWT token หรือ JWT token ไม่ถูกต้อง                 |
| 404  | Not Found                | ไม่พบสมุดงาน แผ่นงาน หรือดัชนีรูปร่างที่ระบุ             |
| 500  | Internal Server Error    | ปัญหาที่เกิดขึ้นภายในเซิร์ฟเวอร์โดยไม่คาดคิด             |

**ตัวอย่างการตอบกลับข้อผิดพลาด**

*400 – Bad Request*

```json
{
  "Code": 400,
  "Message": "Invalid request payload. 'Name' field exceeds maximum length."
}
```

*401 – Unauthorized*

```json
{
  "Code": 401,
  "Message": "Authentication failed. Invalid or expired JWT token."
}
```

*404 – Not Found*

```json
{
  "Code": 404,
  "Message": "The specified workbook, worksheet, or shape index was not found."
}
```

*500 – Internal Server Error*

```json
{
  "Code": 500,
  "Message": "An unexpected error occurred on the server."
}
```

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}