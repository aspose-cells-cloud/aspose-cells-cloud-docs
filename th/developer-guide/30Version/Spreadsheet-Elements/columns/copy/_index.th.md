---
title: "คัดลอกคอลัมน์ในสมุดงาน Excel"
second_title: "เอกสาร"
linktype: "คัดลอก"
type: docs
url: /columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, คัดลอกคอลัมน์, Excel API, REST, Cloud SDK, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "เรียนรู้วิธีการคัดลอกคอลัมน์หนึ่งคอลัมน์หรือหลายคอลัมน์ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) รวมถึงไวยากรณ์คำขอ พารามิเตอร์ที่จำเป็น รายละเอียดการยืนยันตัวตน การจัดการข้อผิดพลาด และตัวอย่าง SDK ใน C#, Java, Python, Ruby, Node.js, Go, Perl และอื่นๆ"
articleTitle: "คัดลอกคอลัมน์ในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
weight: 30
---

REST API นี้คัดลอก **คอลัมน์** ในสมุดงาน Excel การดำเนินการ **Copy Columns** ช่วยให้คุณทำซ้ำคอลัมน์เดียวหรือช่วงของคอลัมน์ และแทรกสำเนาไว้ที่ตำแหน่งที่กำหนดภายในสมุดงานเดียวกัน ใช้ endpoint นี้เพื่อคัดลอกคอลัมน์ได้อย่างมีประสิทธิภาพเมื่อทำงานกับสเปรดชีตขนาดใหญ่ และอ้างอิงการดำเนินการที่เกี่ยวข้อง เช่น [เพิ่มคอลัมน์](/columns/add/) และ [ซ่อนคอลัมน์](/columns/hide/) สำหรับงานการจัดการคอลัมน์เพิ่มเติม

## ความปลอดภัยและการยืนยันตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนแบบ JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### พารามิเตอร์คำขอ

| ชื่อพารามิเตอร์           | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                            |
| -------------------------- | --------- | -------- | ----------------------------------------------------------------------------------- |
| **name**                   | string    | path     | ชื่อสมุดงาน                                                                        |
| **sheetName**              | string    | path     | ชื่อworksheet                                                                      |
| **sourceColumnIndex**      | integer   | query    | ดัชนีของคอลัมน์ที่จะคัดลอก (เริ่มต้นที่ 0)                                         |
| **destinationColumnIndex** | integer   | query    | ดัชนีของตำแหน่งที่จะแทรกคอลัมน์ที่คัดลอก (เริ่มต้นที่ 0)                          |
| **columnNumber**           | integer   | query    | จำนวนคอลัมน์ที่ต่อเนื่องกันที่จะคัดลอก                                            |
| **worksheet**              | string    | query    | _(ไม่บังคับ)_ ตัวระบุ worksheet ที่ใช้เมื่อชื่อ worksheet ไม่ตรงกับค่าใน path        |
| **folder**                 | string    | query    | เส้นทางไปยังโฟลเดอร์ที่เก็บสมุดงานในพื้นที่จัดเก็บของ Aspose Cloud                 |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) กำหนดสัญญาแบบเต็มสำหรับการดำเนินการนี้

### ตัวอย่าง cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### การตอบกลับ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## การจัดการข้อผิดพลาด

API จะส่งคืนโค้ดสถานะ HTTP มาตรฐานพร้อม JSON payload ที่อธิบายข้อผิดพลาด

| โค้ดสถานะ | ความหมาย                                              | ตัวอย่าง JSON Body                                                        |
| --------- | ------------------------------------------------------ | ------------------------------------------------------------------------ |
| **400**   | คำขอไม่ถูกต้อง – พารามิเตอร์ไม่ถูกต้อง               | `{ "Code": 400, "Message": "Invalid column index." }`                    |
| **401**   | ไม่ได้รับอนุญาต – ไม่มีโทเค็นหรือโทเค็นไม่ถูกต้อง    | `{ "Code": 401, "Message": "Access token is invalid or expired." }`      |
| **404**   | ไม่พบ – สมุดงานหรือ worksheet ไม่มีอยู่              | `{ "Code": 404, "Message": "Workbook not found." }`                      |
| **500**   | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – เงื่อนไขที่ไม่คาดคิด | `{ "Code": 500, "Message": "An unexpected error occurred." }`            |

> **วิธีแก้ไขปัญหา:** ตรวจสอบให้แน่ใจว่าโทเค็นการเข้าถึงยังไม่หมดอายุ ชื่อสมุดงานและ worksheet ถูกต้อง และ `sourceColumnIndex`, `destinationColumnIndex`, และ `columnNumber` อยู่ในช่วงคอลัมน์ของ worksheet

## กลุ่ม SDK สำหรับ Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "ฉันจะยืนยันตัวตนเมื่อเรียกใช้ Copy Columns API ได้อย่างไร?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "รับ OAuth2 access token จาก Aspose Cloud โดยใช้ client ID และ secret ของคุณ แล้วแนบไว้ใน header คำขอเป็น `Authorization: Bearer <access_token>`"
      }
    },
    {
      "@type": "Question",
      "name": "`sourceColumnIndex` และ `destinationColumnIndex` ต่างกันอย่างไร?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "`sourceColumnIndex` คือดัชนีที่เริ่มต้นที่ 0 ของคอลัมน์ที่คุณต้องการคัดลอก ส่วน `destinationColumnIndex` คือดัชนีที่เริ่มต้นที่ 0 ของตำแหน่งที่จะแทรกคอลัมน์ที่คัดลอก"
      }
    },
    {
      "@type": "Question",
      "name": "ถ้าการดำเนินการคัดลอกล้มเหลว ฉันจะได้รับการตอบกลับแบบใด?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "API จะส่งคืนโค้ดสถานะที่ไม่ใช่ 200 (เช่น 400 สำหรับคำขอที่ไม่ถูกต้อง 401 สำหรับการไม่ได้รับอนุญาต) ตัว body ของการตอบกลับจะมี JSON object ที่มีฟิลด์ `Code` และ `Message` ซึ่งอธิบายข้อผิดพลาด"
      }
    }
  ]
}
</script>
---