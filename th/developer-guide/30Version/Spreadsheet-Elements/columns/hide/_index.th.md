---
title: "ซ่อนคอลัมน์ในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "ซ่อน"
type: docs
url: /columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, hide columns API, Excel column hide, REST API hide columns, Aspose.Cells SDK, spreadsheet automation"
description: "เรียนรู้วิธีการซ่อนคอลัมน์หนึ่งคอลัมน์หรือหลายคอลัมน์ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ซึ่งรวมถึง endpoint, พารามิเตอร์, ตัวอย่าง cURL, ตัวอย่างโค้ด SDK และการจัดการข้อผิดพลาด"
weight: 40
---

REST API นี้ใช้ซ่อนคอลัมน์ในวอร์กชีต

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | ---------- | -------- | ------------------------------------------------------------------------ |
| name             | string     | path     | ชื่อไฟล์สมุดงาน                                                         |
| sheetName        | string     | path     | ชื่อวอร์กชีตที่จะซ่อนคอลัมน์                                            |
| startColumn      | integer    | query    | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกที่จะซ่อน                           |
| totalColumns     | integer    | query    | จำนวนคอลัมน์ที่ต่อเนื่องกันที่จะซ่อน โดยเริ่มจาก **startColumn**        |
| folder           | string     | query    | เส้นทางไปยังโฟลเดอร์ที่เก็บสมุดงาน                                     |
| storageName      | string     | query    | ชื่อของบริการจัดเก็บข้อมูลที่ไฟล์นั้นตั้งอยู่                             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือคำสั่ง **cURL** เพื่อเรียกใช้บริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีการซ่อนคอลัมน์โดยใช้ cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**รหัสการตอบกลับที่เป็นไปได้**

| รหัส HTTP | ความหมาย                                    | ตัวอย่าง JSON (ข้อผิดพลาด)                            |
| --------- | ------------------------------------------- | ----------------------------------------------------- |
| 200       | สำเร็จ                                      | `{ "Code": 200, "Status": "OK" }`                     |
| 400       | คำขอผิดพลาด (เช่น พารามิเตอร์ไม่ถูกต้อง)   | `{ "Code": 400, "Message": "Invalid column range." }` |
| 401       | ไม่ได้รับอนุญาต (ไม่มี/โทเค็นไม่ถูกต้อง)    | `{ "Code": 401, "Message": "Invalid access token." }` |
| 404       | ไม่พบ (สมุดงานหรือวอร์กชีต)                | `{ "Code": 404, "Message": "File not found." }`       |
| 500       | ข้อผิดพลาดภายในเซิร์ฟเวอร์                   | `{ "Code": 500, "Message": "Unexpected error." }`     |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำไว้ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}