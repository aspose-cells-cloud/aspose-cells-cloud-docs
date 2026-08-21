---
title: "คัดลอกช่วงข้อมูลในแผ่นงานพร้อมตัวเลือกการวาง"
second_title: "เอกสาร"
linktitle: "คัดลอก"
type: docs
url: /th/ranges/copy/
aliases: [  /th/copy-range-in-a-worksheet-with-paste-options/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, คัดลอกช่วงข้อมูล, แผ่นงาน, ตัวเลือกการวาง"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อคัดลอกช่วงข้อมูลภายในแผ่นงานของสมุด Excel โดยรองรับตัวเลือกการวางแบบเต็มรูปแบบ รวมตัวอย่าง SDK สำหรับภาษาโปรแกรมต่างๆ หลายภาษา"
weight: 20
ArticleTitle: "คัดลอกช่วงข้อมูลในแผ่นงานพร้อมตัวเลือกการวาง – Aspose.Cells Cloud API"
---

REST API นี้คัดลอกช่วงข้อมูลในแผ่นงานของสมุด Excel สำหรับการดำเนินการที่เกี่ยวข้อง โปรดดูเอกสาร **Get Range** และ **Update Range**

**ข้อกำหนดเบื้องต้น:** เพื่อใช้งาน endpoint นี้ คุณต้องมีโทเค็น OAuth 2.0 / JWT ที่ถูกต้อง และต้องแน่ใจว่าเวอร์ชัน API ของคุณตรงกับ URL คำขอ

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | ---------- | -------- | ------------------------------------------------------------------------ |
| name             | string     | path     | ชื่อของสมุดงาน                                                         |
| sheetName        | string     | path     | ชื่อของแผ่นงาน                                                          |
| rangeOperate     | string     | body     | การดำเนินการที่จะทำ: `copydata`, `copystyle`, `copyto` หรือ `copyvalue` |
| folder           | string     | query    | โฟลเดอร์ที่เก็บสมุดงาน                                                  |
| storageName      | string     | query    | ชื่อของบริการจัดเก็บข้อมูล                                               |

**หมายเหตุ:** ฟิลด์ `rangeOperate` กำหนดสิ่งที่จะถูกคัดลอก ใช้ `copydata` เพื่อคัดลอกเฉพาะค่าของเซลล์, `copystyle` สำหรับรูปแบบ, `copyto` สำหรับทั้งข้อมูลและรูปแบบ และ `copyvalue` เพื่อคัดลอกค่าโดยไม่รวมสูตร API รองรับช่วงข้อมูลสูงสุด 1 ล้านเซลล์; ช่วงข้อมูลที่ใหญ่กว่านั้นอาจทำให้เกิดการหมดเวลา (timeout)

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangesCopy) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "Operate": "string",
        "Source": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "Target": {
          "ColumnCount": 0,
          "ColumnWidth": 0,
          "FirstColumn": 0,
          "FirstRow": 0,
          "Name": "string",
          "RefersTo": "string",
          "RowCount": 0,
          "RowHeight": 0,
          "Worksheet": "string"
        },
        "PasteOptions": {
          "OnlyVisibleCells": true,
          "PasteType": "string",
          "SkipBlanks": true,
          "Transpose": true
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

การตอบกลับที่สำเร็จจะส่งกลับสถานะ `200 OK` ในกรณีที่เกิดข้อผิดพลาด API อาจส่งกลับข้อมูล payload เช่น:

```json
{
  "Code": 400,
  "Message": "Bad Request – พารามิเตอร์ไม่ถูกต้อง"
}
```

หรือ

```json
{
  "Code": 401,
  "Message": "Unauthorized – โทเค็นยืนยันตัวตนหายไปหรือไม่ถูกต้อง"
}
```

วัตถุข้อผิดพลาดเหล่านี้ประกอบด้วยรหัสสถานะ HTTP และข้อความอธิบายเพื่อช่วยในการวิเคราะห์ปัญหา

{{< /tab >}}

{{< /tabs >}}

คุณสามารถดาวน์โหลดสมุดงานตัวอย่างเพื่อทดสอบการดำเนินการคัดลอกได้ [ที่นี่](https://example.com/sample.xlsx)

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ จึงสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangesCopy.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangesCopy.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangesCopy.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangesCopy.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangesCopy.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangesCopy.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangesCopy.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangesCopy.go" >}}

{{< /tab >}}

{{< /tabs >}}