---
title: "รับกฎการจัดรูปแบบตามเงื่อนไข"
type: docs
url: /th/conditional-formattings/get-all/
aliases: [  /th/get-conditional-formattings-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, REST API, Excel, การจัดรูปแบบตามเงื่อนไข, แผ่นงาน, API การจัดรูปแบบตามเงื่อนไข"
description: "ดึงกฎการจัดรูปแบบตามเงื่อนไขทั้งหมดที่ใช้กับแผ่นงานโดยใช้ Aspose.Cells Cloud REST API รวมถึงไคลเอนต์ไคลเอ็นซิสของคำสั่ง, ขั้นตอนการยืนยันตัวตน, พารามิเตอร์, ตัวอย่างการตอบกลับที่กระชับ และการจัดการข้อผิดพลาด"
weight: 20
---

REST API นี้ดึงกฎการจัดรูปแบบตามเงื่อนไขที่ใช้กับแผ่นงาน

## ความปลอดภัยและการยืนยันตัวตน
API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้[การยืนยันตัวตนแบบใช้โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                  |
| ---------------- | -------- | ------- | ------------------------------------------ |
| name             | string   | path    | ชื่อไฟล์ Excel                            |
| sheetName        | string   | path    | ชื่อแผ่นงาน                               |
| folder           | string   | query   | ตำแหน่งโฟลเดอร์ที่จัดเก็บไฟล์ไว้         |
| storageName      | string   | query   | ชื่อของบริการจัดเก็บข้อมูล (ไม่บังคับ)     |

### การตอบกลับข้อผิดพลาด

| โค้ด HTTP | เหตุผล                                              | ตัวอย่างเนื้อหาตอบกลับ                                               |
| --------- | ---------------------------------------------------- | -------------------------------------------------------------------- |
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์หายไปหรือไม่ถูกต้อง   | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | ไม่ได้รับอนุญาต – โทเค็น JWT หายไปหรือไม่ถูกต้อง  | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่               | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – เซิร์ฟเวอร์ล้มเหลวโดยไม่คาดคิด | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">สเปค OpenAPI</a> นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และอนุญาตให้คุณเรียกใช้การโต้ตอบ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_ตัวอย่างด้านบนแสดงเฉพาะฟิลด์ที่เกี่ยวข้องมากที่สุดเพื่อให้ข้อมูลที่ส่งกลับมีความกระชับ_

**พารามิเตอร์การตอบกลับ**

| พารามิเตอร์                        | ชนิดข้อมูล | คำอธิบาย                                         |
|------------------------------------|-----------|--------------------------------------------------|
| Status                             | string    | สถานะผลลัพธ์ของคำขอ (เช่น **OK**)              |
| ConditionalFormattings             | object    | คอนเทนเนอร์สำหรับข้อมูลการจัดรูปแบบตามเงื่อนไข |
| ConditionalFormattings.Count       | integer   | จำนวนกฎการจัดรูปแบบตามเงื่อนไขที่ส่งกลับมา     |
| ConditionalFormattings.ConditionalFormattingList | array     | รายการวัตถุการจัดรูปแบบตามเงื่อนไข             |
| ConditionalFormattingList[].sqref  | string    | ช่วงเซลล์ที่รูปแบบใช้ (เช่น **A1:B10**)         |
| ConditionalFormattingList[].FormatConditions | array     | คอลเลกชันของวัตถุเงื่อนไขรูปแบบสำหรับช่วงนั้น   |
| FormatConditions[].Priority        | integer   | ลำดับความสำคัญในการประเมินเงื่อนไข             |
| FormatConditions[].Type            | string    | ประเภทของเงื่อนไข (เช่น **CellValue**)          |
| FormatConditions[].Operator        | string    | โอเปอเรเตอร์ที่ใช้กับเงื่อนไข (เช่น **GreaterThan**) |
| FormatConditions[].Formula1        | string    | สูตรหรือค่าแรกของเงื่อนไข                        |
| FormatConditions[].Style           | object    | การจัดรูปแบบที่ใช้เมื่อเงื่อนไขเป็นจริง          |
| Style.Font.Color                   | object    | นิยามสี RGBA สำหรับแบบอักษร                     |
| Style.Font.IsBold                  | boolean   | บ่งชี้ว่าแบบอักษรเป็นตัวหนาหรือไม่              |

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                      | คำอธิบาย                                        |
|-----|-------------------------------|------------------------------------------------|
| 200 | สำเร็จ (OK)                   | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์หายไปหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเค็น JWT ไม่ถูกต้องหรือหายไป                |
| 413 | เนื้อหาที่ส่งมามีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด     |
| 500 | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์      |

{{< /tab >}}

{{< /tabs >}}

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโปรเจกต์ของคุณได้ โปรดตรวจสอบ<a href="https://github.com/aspose-cells-cloud" target="_blank">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}