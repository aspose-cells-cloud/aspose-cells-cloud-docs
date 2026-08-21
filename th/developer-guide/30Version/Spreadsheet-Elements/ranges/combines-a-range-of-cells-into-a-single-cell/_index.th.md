---
title: "Aspose.Cells Cloud API – ผสานช่วงเซลล์"
second title: "เอกสาร"
linktitle: "ผสาน"
type: docs
url: /ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: "Aspose.Cells, ผสานเซลล์, Excel API, REST, SDK บนคลาวด์"
description: "ผสานช่วงเซลล์หลายเซลล์ให้เป็นเซลล์เดียวโดยใช้ Aspose.Cells Cloud REST API เรียนรู้เกี่ยวกับรูปแบบคำขอ พารามิเตอร์ และตัวอย่าง SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 20
---

API นี้ผสานช่วงเซลล์หลายเซลล์ให้เป็นเซลล์เดียวในแผ่นงาน Excel

**ภาพรวม** – การผสานช่วงจะรวมเซลล์ที่เลือกไว้ให้เป็นเซลล์เดียว โดยรักษาค่าของเซลล์มุมบนซ้ายไว้และทิ้งค่าของเซลล์อื่นๆ ไป คุณสามารถใช้การดำเนินการนี้เมื่อต้องการสร้างส่วนหัวที่ขยายครอบคลุมหลายคอลัมน์หรือหลายแถว หรือเมื่อต้องการปรับโครงสร้างแผ่นงานให้เรียบง่ายขึ้น

## API บนคลาวด์

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                          |
| ---------------- | --------- | -------- | ------------------------------------------------- |
| **name**         | สตริง     | path     | ชื่อสมุดงาน                                     |
| **sheetName**    | สตริง     | path     | ชื่อแผ่นงาน                                     |
| **range**        | ออบเจกต์  | body     | ออบเจกต์ช่วงที่ระบุเซลล์ที่จะผสาน               |
| **folder**       | สตริง     | query    | โฟลเดอร์ที่เก็บสมุดงานไว้                      |
| **storageName**  | สตริง     | query    | ชื่อพื้นที่จัดเก็บ                              |

#### โครงสร้างเนื้อหาคำขอ

ออบเจกต์ **Range** จะต้องมีฟิลด์ต่อไปนี้ (ฟิลด์อื่นๆ เป็นทางเลือก):

| คุณสมบัติ        | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                             |
| ---------------- | --------- | ------ | ---------------------------------------------------- |
| **FirstRow**     | จำนวนเต็ม  | ใช่    | ดัชนีเริ่มต้นที่ 0 ของแถวแรกในช่วง                  |
| **FirstColumn**  | จำนวนเต็ม  | ใช่    | ดัชนีเริ่มต้นที่ 0 ของคอลัมน์แรกในช่วง              |
| **RowCount**     | จำนวนเต็ม  | ใช่    | จำนวนแถวที่จะรวมอยู่ในช่วง                          |
| **ColumnCount**  | จำนวนเต็ม  | ใช่    | จำนวนคอลัมน์ที่จะรวมอยู่ในช่วง                     |
| **Name**         | สตริง      | ไม่ใช่ | ชื่อทางเลือกของช่วง                                |
| **RefersTo**     | สตริง      | ไม่ใช่ | สูตรที่ช่วงนี้อ้างอิงถึง                            |
| **Worksheet**    | สตริง      | ไม่ใช่ | ชื่อแผ่นงาน (ถ้าต่างจากพารามิเตอร์ path)           |
| **RowHeight**    | จำนวนจริง  | ไม่ใช่ | ความสูงของแถวในช่วง (หน่วยเป็นพิกเซล)             |
| **ColumnWidth**  | จำนวนจริง  | ไม่ใช่ | ความกว้างของคอลัมน์ในช่วง (หน่วยเป็นพิกเซล)       |

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
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

{{< /tab >}}

{{< /tabs >}}

#### รายละเอียดการตอบกลับ

| สถานะ HTTP                   | คำอธิบาย                                               | JSON ตัวอย่าง                                         |
| ---------------------------- | ------------------------------------------------------ | ---------------------------------------------------- |
| **200 OK**                   | ผสานช่วงสำเร็จแล้ว                                   | `{ "Code": 200, "Status": "OK" }`                    |
| **400 Bad Request**          | พารามิเตอร์ช่วงไม่ถูกต้อง (เช่น ดัชนีเกินขอบเขต)       | `{ "Code": 400, "Message": "Invalid range." }`      |
| **401 Unauthorized**         | ไม่มีหรือโทเค็น JWT ไม่ถูกต้อง                         | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**            | ไม่พบสมุดงานหรือแผ่นงาน                              | `{ "Code": 404, "Message": "Resource not found." }` |
| **500 Internal Server Error** | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                 | `{ "Code": 500, "Message": "Internal server error." }` |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}