---
title: "เพิ่มเงื่อนไขการจัดรูปแบบ"
type: docs
url: /th/conditional-formattings/add-format-condition/
aliases: [  /th/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, Conditional Formatting API, เพิ่มเงื่อนไขการจัดรูปแบบ, Excel REST API, Cells API"
description: "เรียนรู้วิธีเพิ่มเงื่อนไขการจัดรูปแบบให้กับแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมถึงไวยากรณ์คำขอ พารามิเตอร์ ตัวอย่าง cURL ที่ปลอดภัย และตัวอย่าง SDK"
ArticleTitle: "เพิ่มเงื่อนไขการจัดรูปแบบ – เอกสารประกอบ Aspose.Cells Cloud API"
weight: 50
---

REST API นี้จะเพิ่มเงื่อนไขการจัดรูปแบบให้กับแผ่นงาน

## ความปลอดภัยและการยืนยันตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนด้วยโทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                                                        |
| -------------- | ------- | -------- | ------------------------------------------------------------------------------- |
| name           | string  | path     | ชื่อของสมุดงาน Excel                                                           |
| sheetName      | string  | path     | ชื่อของแผ่นงานที่มีช่วงของเซลล์ที่ต้องการจัดรูปแบบ                           |
| index          | integer | path     | ดัชนีแบบ zero-based ของเงื่อนไขการจัดรูปแบบที่จะเพิ่มหรือแทนที่               |
| cellArea       | string  | query    | ช่วงของเซลล์ (เช่น `A1:C3`) ที่เงื่อนไขนี้นำไปใช้ได้                          |
| type           | string  | query    | ประเภทของเงื่อนไข (เช่น `Expression`, `CellValue`)                             |
| operatorType   | string  | query    | ตัวดำเนินการสำหรับเงื่อนไข (เช่น `Between`, `Equal`)                          |
| formula1       | string  | query    | สูตรหรือค่าแรกที่ใช้ในเงื่อนไข                                                   |
| formula2       | string  | query    | สูตรหรือค่าที่สอง (จำเป็นสำหรับตัวดำเนินการบางประเภท เช่น `Between`)           |
| folder         | string  | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานอยู่                                         |
| storageName    | string  | query    | ชื่อของบริการพื้นที่จัดเก็บ (เช่น `Default`)                                   |

### การตอบกลับข้อผิดพลาด

| โค้ด HTTP | เหตุผล                                              | ตัวอย่างเนื้อหา                                                     |
| --------- | ---------------------------------------------------- | -------------------------------------------------------------------- |
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์หายไปหรือไม่ถูกต้อง   | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | ไม่ได้รับอนุญาต – โทเค็น JWT หายไปหรือไม่ถูกต้อง   | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่                | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – เซิร์ฟเวอร์ล้มเหลวโดยไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

### การตอบกลับที่สำเร็จ

| โค้ด HTTP | เหตุผล                                         | ตัวอย่างเนื้อหา                          |
| --------- | ----------------------------------------------- | ------------------------------------------ |
| **200**   | สำเร็จ – เพิ่มหรืออัปเดตเงื่อนไขสำเร็จแล้ว    | `{ "Code": "200", "Status": "OK" }` |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้ **cURL** เพื่อเรียก Aspose.Cells API ได้ ตัวอย่างด้านล่างแสดงคำขอที่สมบูรณ์ รวมถึงเนื้อหา JSON ว่างเปล่า

### ตัวอย่าง cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
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

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ดังนั้นคุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่มีทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียก Aspose.Cells web services โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}