---
title: "ลบพื้นที่เซลล์ – เอกสารประกอบ API ของ Aspose.Cells Cloud"
type: docs
url: /conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: "Aspose.Cells Cloud, ลบพื้นที่เซลล์, API การจัดรูปแบบตามเงื่อนไข, Excel REST API"
description: "ใช้ Aspose.Cells Cloud REST API เพื่อลบพื้นที่เซลล์ที่ระบุออกจากกฎการจัดรูปแบบตามเงื่อนไขในแผ่นงาน Excel ประกอบด้วยตัวอย่าง ASP.NET, Java และ Python"
ArticleTitle: "ลบพื้นที่เซลล์ – เอกสารประกอบ API ของ Aspose.Cells Cloud"
weight: 70
---

REST API นี้จะลบพื้นที่เซลล์ออกจากกฎการจัดรูปแบบตามเงื่อนไข

## ความปลอดภัยและการยืนยันตัวตน
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้[การยืนยันตัวตนแบบ JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                      |
| ---------------- | ---------- | -------- | ---------------------------------------------------------------------------- |
| `name`           | string     | path     | ชื่อไฟล์ Excel                                                                |
| `sheetName`      | string     | path     | ชื่อแผ่นงานที่มีการจัดรูปแบบตามเงื่อนไข                                     |
| `startRow`       | integer    | query    | ดัชนีเริ่มต้นแบบศูนย์ของแถวแรกของพื้นที่ที่จะถูกลบ                            |
| `startColumn`    | integer    | query    | ดัชนีเริ่มต้นแบบศูนย์ของคอลัมน์แรกของพื้นที่ที่จะถูกลบ                        |
| `totalRows`      | integer    | query    | จำนวนแถวในพื้นที่ที่จะถูกลบ                                                   |
| `totalColumns`   | integer    | query    | จำนวนคอลัมน์ในพื้นที่ที่จะถูกลบ                                               |
| `folder`         | string     | query    | โฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์ที่ไฟล์ตั้งอยู่ (ไม่บังคับ)                   |
| `storageName`    | string     | query    | ชื่อของบริการจัดเก็บข้อมูล (ไม่บังคับ)                                        |

### การตอบกลับข้อผิดพลาด

| สถานะ HTTP | โค้ด            | คำอธิบาย                                                                  | JSON ตัวอย่าง                                                   |
| ----------- | --------------- | ------------------------------------------------------------------------- | ------------------------------------------------------------- |
| 400         | `BadRequest`    | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง                                          | `{ "Code": "400", "Message": "Invalid request parameters." }` |
| 401         | `Unauthorized`  | JWT token ขาดหายหรือไม่ถูกต้อง                                            | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404         | `NotFound`      | ไม่พบไฟล์ แผ่นงาน หรือการจัดรูปแบบตามเงื่อนไข                           | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500         | `InternalError` | เกิดข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด                                 | `{ "Code": "500", "Message": "Internal server error." }`      |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL จากบรรทัดคำสั่งเพื่อเข้าถึงบริการของ Aspose.Cells Cloud ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้จุดสิ้นสุด **Delete Cell Area** ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดู[ kho คลัง GitHub ](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}