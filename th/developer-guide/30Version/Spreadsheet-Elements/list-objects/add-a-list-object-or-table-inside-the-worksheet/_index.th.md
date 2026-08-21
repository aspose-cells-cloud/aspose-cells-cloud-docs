---
title: "เพิ่มวัตถุรายการ (ตาราง) ลงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "เพิ่ม"
type: docs
url: /th/list-objects/add/
aliases: [  /th/add-a-list-object-or-table-inside-the-worksheet/ , /th/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel API, วัตถุรายการ, ตาราง, REST API, แผ่นงาน"
description: "เรียนรู้วิธีการเพิ่มวัตถุรายการ (ตาราง Excel) ลงในแผ่นงานโดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึง endpoint, พารามิเตอร์, ขั้นตอนการยืนยันตัวตน, ตัวอย่าง cURL และตัวอย่างโค้ด SDK"
weight: 10
ArticleTitle: "เพิ่มวัตถุรายการ (ตาราง) ลงในแผ่นงาน Excel – เอกสารประกอบ Aspose.Cells Cloud"
---

REST API นี้จะเพิ่ม **วัตถุรายการ (ตาราง)** ลงในแผ่นงาน Excel

ก่อนใช้งาน endpoint นี้ โปรดตรวจสอบให้แน่ใจว่าคุณมี JWT token ที่ถูกต้อง สมุดงานถูกจัดเก็บไว้ในคลาวด์สโตร์ที่รองรับ และแผ่นงานมีอยู่แล้ว

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | --------- | -------- | ------------------------------------------------------------------------ |
| **name**         | string    | path     | ชื่อไฟล์สมุดงาน                                                         |
| **sheetName**    | string    | path     | ชื่อแผ่นงาน                                                             |
| **startRow**     | integer   | query    | ดัชนีเริ่มต้นแบบศูนย์ของแถวแรกของช่วงตาราง                             |
| **startColumn**  | integer   | query    | ดัชนีเริ่มต้นแบบศูนย์ของคอลัมน์แรกของช่วงตาราง                         |
| **endRow**       | integer   | query    | ดัชนีสุดท้ายแบบศูนย์ของแถวสุดท้ายของช่วงตาราง                          |
| **endColumn**    | integer   | query    | ดัชนีสุดท้ายแบบศูนย์ของคอลัมน์สุดท้ายของช่วงตาราง                      |
| **hasHeaders**   | boolean   | query    | `true` หากแถวแรกมีหัวคอลัมน์ มิฉะนั้นเป็น `false`                      |
| **listObject**   | object    | body     | คำนิยามของวัตถุรายการ (ดู **โครงร่างเนื้อหาคำขอ**)                     |
| **folder**       | string    | query    | โฟลเดอร์ที่เก็บสมุดงาน                                                  |
| **storageName**  | string    | query    | ชื่อคลังเก็บข้อมูล                                                       |

### โครงร่างเนื้อหาคำขอ

วัตถุ **listObject** ใช้อธิบายตารางที่จะถูกสร้างขึ้น ตัวอย่างด้านล่างแสดงเฉพาะคุณสมบัติที่พบบ่อยที่สุด โปรดดูข้อกำหนด OpenAPI สำหรับรายชื่อที่สมบูรณ์

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### ตัวอย่างคำขอ (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### ตัวอย่างการตอบกลับ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### รหัสข้อผิดพลาด

| สถานะ HTTP | เหตุผล                 | คำอธิบาย                                              |
| ----------- | ----------------------- | ----------------------------------------------------- |
| **400**     | Bad Request             | พารามิเตอร์ช่วงไม่ถูกต้องหรือเนื้อหา JSON ผิดรูปแบบ |
| **401**     | Unauthorized            | ไม่มีหรือ JWT token หมดอายุ                           |
| **404**     | Not Found               | สมุดงานหรือแผ่นงานที่ระบุไม่มีอยู่                   |
| **500**     | Internal Server Error   | ข้อผิดพลาดที่ไม่คาดคิดเกิดขึ้นที่เซิร์ฟเวอร์           |

**ตัวอย่างการตอบกลับ 400**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**ตัวอย่างการตอบกลับ 401**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) ให้สัญญาเต็มรูปแบบสำหรับการดำเนินการนี้

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำและช่วยให้คุณมุ่งเน้นไปที่งานโครงการของคุณ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}