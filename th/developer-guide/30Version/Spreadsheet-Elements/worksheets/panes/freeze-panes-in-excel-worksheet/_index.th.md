---
title: "การแช่ช่วงในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "แช่ช่วง"
type: docs
url: /worksheets/panes/freeze/
aliases: [/freeze-panes-in-excel-worksheet/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, Freeze Panes, Excel, REST API, Worksheet"
description: "เรียนรู้วิธีการแช่ช่วงแถวและคอลัมน์ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งประกอบด้วยไวยากรณ์ของ endpoint, พารามิเตอร์ที่จำเป็น, ตัวอย่าง cURL, คำแนะนำการยืนยันตัวตน, รายละเอียดการตอบกลับข้อผิดพลาด และตัวอย่างโค้ด SDK สำหรับหลายภาษา"
weight: 190
---

REST API นี้ **ตั้งค่า** การแช่ช่วงในแผ่นงาน Excel

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

พารามิเตอร์ของคำขอมีดังนี้:

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                           |
| ---------------- | --------- | -------- | -------------------------------------------------- |
| name             | string    | path     | ชื่อไฟล์สมุดงาน                                   |
| sheetName        | string    | path     | ชื่อแผ่นงานที่แช่ช่วง                                   |
| row              | integer   | query    | ดัชนีแบบเริ่มต้นที่ 0 ของแถวแรกที่ **ยังไม่ได้แช่ช่วง** |
| column           | integer   | query    | ดัชนีแบบเริ่มต้นที่ 0 ของคอลัมน์แรกที่ **ยังไม่ได้แช่ช่วง** |
| frozenRows       | integer   | query    | จำนวนแถวที่แช่ช่วงเริ่มจากด้านบน                    |
| frozenColumns    | integer   | query    | จำนวนคอลัมน์ที่แช่ช่วงเริ่มจากด้านซ้าย               |
| folder           | string    | query    | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานตั้งอยู่    |
| storageName      | string    | query    | ชื่อของบริการพื้นที่จัดเก็บ                           |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### การตอบกลับข้อผิดพลาด

| สถานะ HTTP                | โค้ด | ข้อความ                              | ตัวอย่าง                                                  |
| ------------------------- | ---- | ------------------------------------ | -------------------------------------------------------- |
| 400 Bad Request           | 400  | พารามิเตอร์ไม่ถูกต้อง               | `{ "Code": 400, "Message": "ค่า frozenRows ไม่ถูกต้อง" }` |
| 401 Unauthorized          | 401  | ไม่มีหรือ JWT token ไม่ถูกต้อง       | `{ "Code": 401, "Message": "โทเคนการเข้าถึงไม่ถูกต้อง" }` |
| 404 Not Found             | 404  | ไม่พบสมุดงานหรือแผ่นงาน            | `{ "Code": 404, "Message": "ไม่พบไฟล์" }`           |
| 500 Internal Server Error | 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด | `{ "Code": 500, "Message": "ข้อผิดพลาดภายในของเซิร์ฟเวอร์" }` |

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}