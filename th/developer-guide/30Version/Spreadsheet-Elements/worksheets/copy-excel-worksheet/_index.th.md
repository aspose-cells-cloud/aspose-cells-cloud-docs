---
title: "คัดลอกเนื้อหาและรูปแบบจากวาร์กชีตอื่น"
second_title: "เอกสาร"
linktype: "คัดลอก"
type: docs
url: /th/worksheets/copy/
aliases: [  /th/copy-excel-worksheet/ ]
keywords: "API คัดลอกวาร์กชีตของ Aspose Cells, การคัดลอกชีต Excel ผ่าน REST, SDK ของ Aspose Cloud สำหรับการคัดลอก, การคัดลอกวาร์กชีตสเปรดชีต"
description: "เรียนรู้วิธีการคัดลอกวาร์กชีตและรูปแบบของมันไปยังชีตใหม่โดยใช้ Aspose.Cells Cloud REST API ประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL และ SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 20
---

REST API นี้คัดลอกวาร์กชีตและรูปแบบของมันไปยังชีตใหม่ภายในสมุดงานเดียวกัน

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

พารามิเตอร์คำขอแสดงไว้ด้านล่าง:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                           |
| ---------------- | -------- | ------- | ------------------------------------------------------------------ |
| `name`           | string   | path    | ชื่อไฟล์สมุดงาน                                                   |
| `sheetName`      | string   | path    | ชื่อวาร์กชีตปลายทาง (ชีตใหม่)                                     |
| `sourceSheet`    | string   | query   | ชื่อวาร์กชีตที่จะถูกคัดลอก                                        |
| `options`        | object   | body    | วัตถุ JSON ที่มีตัวเลือกการคัดลอก (เช่น ความกว้างคอลัมน์ สูตร)     |
| `sourceWorkbook` | string   | query   | ชื่อสมุดงานต้นฉบับหากแตกต่างจากสมุดงานปัจจุบัน                   |
| `sourceFolder`   | string   | query   | ตำแหน่งโฟลเดอร์ที่เก็บสมุดงานต้นฉบับ                            |
| `folder`         | string   | query   | ตำแหน่งโฟลเดอร์ที่จะบันทึกสมุดงานปลายทาง                        |
| `storageName`    | string   | query   | ชื่อของบริการจัดเก็บข้อมูลที่จะใช้                               |

### ตัวอย่างคำขอ & การตอบกลับ

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### การจัดการข้อผิดพลาด

API จะส่งกลับโค้ดสถานะ HTTP มาตรฐานพร้อมเนื้อหา JSON ของข้อผิดพลาด การตอบกลับทั่วไปมีดังนี้:

| โค้ด HTTP | คำอธิบาย                                                   | ตัวอย่างเนื้อหา JSON ข้อผิดพลาด                               |
| --------- | ---------------------------------------------------------- | ------------------------------------------------------------- |
| 400       | คำขอไม่ถูกต้อง – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง         | `{ "Code": 400, "Message": "Invalid request parameters." }`   |
| 401       | ไม่ได้รับอนุญาต – โทเคนขาดหายหรือไม่ถูกต้อง              | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404       | ไม่พบ – สมุดงาน วาร์กชีต หรือโฟลเดอร์ไม่มีอยู่จริง        | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิด          | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานโปรเจกต์ของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) สำหรับรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}

---