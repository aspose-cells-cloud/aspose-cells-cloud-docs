---
title: "เพิ่มไฮเปอร์ลิงก์ในแผ่นงาน"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, เพิ่มไฮเปอร์ลิงก์, Excel REST API, cloud SDK"
description: "เรียนรู้วิธีการเพิ่มไฮเปอร์ลิงก์ในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud v3.0 REST API ประกอบด้วย endpoint, คู่มือพารามิเตอร์แบบเต็ม, ตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ"
weight: 20
---

REST API นี้เพิ่มไฮเปอร์ลิงก์ในแผ่นงาน Excel

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | ---------- | -------- | ------------------------------------------------------------------------ |
| name             | string     | path     | ชื่อเอกสาร                                                              |
| sheetName        | string     | path     | ชื่อแผ่นงาน                                                            |
| firstRow         | integer    | query    | ดัชนีเริ่มต้นที่ 0 ของแถวแรกของช่วงที่จะใช้ไฮเปอร์ลิงก์                |
| firstColumn      | integer    | query    | ดัชนีเริ่มต้นที่ 0 ของคอลัมน์แรกของช่วงที่จะใช้ไฮเปอร์ลิงก์            |
| totalRows        | integer    | query    | จำนวนแถวที่ช่วงไฮเปอร์ลิงก์ครอบคลุม                                   |
| totalColumns     | integer    | query    | จำนวนคอลัมน์ที่ช่วงไฮเปอร์ลิงก์ครอบคลุม                              |
| address          | string     | query    | URL เป้าหมายที่ไฮเปอร์ลิงก์ชี้ไป (ต้องเข้ารหัสในรูปแบบ URL)           |
| folder           | string     | query    | โฟลเดอร์ของเอกสาร                                                       |
| storageName      | string     | query    | ชื่อพื้นที่จัดเก็บ                                                    |

คำขอสามารถมี JSON body ที่ประกอบด้วยพารามิเตอร์เดียวกัน (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`) ด้วย ซึ่งการส่ง body จะมีประโยชน์เมื่อคุณต้องการใช้ payload แทนพารามิเตอร์ใน query string

### การตอบกลับข้อผิดพลาด

| HTTP Code | เหตุผล                                               | ตัวอย่าง Body                                                       |
| --------- | ----------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – พารามิเตอร์ขาดหายหรือไม่ถูกต้อง        | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized – JWT token ขาดหายหรือไม่ถูกต้อง         | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – สมุดงานหรือแผ่นงานไม่มีอยู่จริง          | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error – เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) กำหนด API ที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการ REST interaction ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก Cloud API โดยใช้ cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
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

หากคำขอล้มเหลว API จะส่งกลับ HTTP error codes มาตรฐาน (เช่น 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error) พร้อมกับ JSON payload ที่ประกอบด้วยข้อความและรหัสข้อผิดพลาด

## Cloud SDK Family

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}