---
title: "ล้างรูปแบบที่มีเงื่อนไข"
type: docs
url: /th/conditional-formattings/clear/
aliases: [  /th/clear-all-condition-formattings/ ]
keywords: "Aspose.Cells Cloud, REST API, ล้างรูปแบบที่มีเงื่อนไข, Excel, ชีตงาน, JWT, v3.2"
description: "ลบกฎรูปแบบที่มีเงื่อนไขทั้งหมดออกจากชีตงานโดยใช้ Aspose.Cells Cloud API (v3.2) เรียนรู้ไวยากรณ์คำขอ พารามิเตอร์ที่จำเป็น ขั้นตอนการยืนยันตัวตน และดูตัวอย่างโค้ดใน SDK หลายภาษา"
weight: 80
---

REST API นี้ล้างกฎรูปแบบที่มีเงื่อนไขทั้งหมดออกจากชีตงาน

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | --------- | -------- | ------------------------------------------------------------------------ |
| **name**         | string    | path     | ชื่อไฟล์สมุดงาน (เช่น `Book1.xlsx`)                                      |
| **sheetName**    | string    | path     | ชื่อชีตงานที่ต้องการลบรูปแบบที่มีเงื่อนไข                              |
| **folder**       | string    | query    | _(ไม่บังคับ)_ ตำแหน่งโฟลเดอร์ในที่จัดเก็บที่อยู่กับสมุดงาน              |
| **storageName**  | string    | query    | _(ไม่บังคับ)_ ชื่อของบริการที่จัดเก็บข้อมูล                              |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบสาธารณะ และ **OpenAPI Specification** ช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงผ่านเบราว์เซอร์เว็บ

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
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

### การตอบกลับข้อผิดพลาด

| โค้ด HTTP | เหตุผล                                                  | เนื้อหาตัวอย่าง                                                    |
| --------- | -------------------------------------------------------- | ------------------------------------------------------------------ |
| **400**   | คำขอไม่ถูกต้อง – ขาดหรือค่าพารามิเตอร์ไม่ถูกต้อง         | `{ "Code":"400", "Message":"Invalid parameter value." }`          |
| **401**   | ไม่ได้รับอนุญาต – ขาดหรือโทเคน JWT ไม่ถูกต้อง           | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | ไม่พบ – สมุดงานหรือชีตงานไม่มีอยู่                      | `{ "Code":"404", "Message":"File not found." }`                   |
| **500**   | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เซิร์ฟเวอร์ล้มเหลวอย่างไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }`     |

## ตัวอย่าง SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ โปรดตรวจสอบที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}