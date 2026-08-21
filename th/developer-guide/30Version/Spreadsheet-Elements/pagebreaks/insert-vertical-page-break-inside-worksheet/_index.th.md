---
title: "เพิ่มการแบ่งหน้าแนวตั้ง"
second_title: "เอกสาร"
linktitle: "เพิ่มการแบ่งหน้าแนวตั้ง"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, vertical page break, REST API, Excel, SDK, cURL"
description: "เรียนรู้วิธีการแทรกการแบ่งหน้าแนวตั้งลงในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมถึงไวยากรณ์คำขอ ตัวอย่าง cURL ตัวอย่าง SDK คู่มือการยืนยันตัวตน และรายละเอียดการจัดการข้อผิดพลาด"
weight: 40
ArticleTitle: "เพิ่มการแบ่งหน้าแนวตั้ง – Aspose.Cells Cloud API"
---

REST API นี้จะแทรกการแบ่งหน้าแนวตั้งลงในแผ่นงาน

## ความปลอดภัยและการยืนยันตัวตน
Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนแบบใช้โทเค็น JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### พารามิเตอร์ของคำขอ

| พารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
|-------------|-----------|---------|----------|
| name | string | path | ชื่อของสมุดงาน Excel |
| sheetName | string | path | ชื่อของแผ่นงานที่จะเพิ่มการแบ่งหน้า |
| cellname | string | query | การอ้างอิงเซลล์ (เช่น **A1**) ที่กำหนดตำแหน่งของการแบ่งหน้า |
| column | integer | query | ดัชนีของคอลัมน์ (เริ่มต้นที่ 0) ที่การแบ่งหน้าเริ่มต้น |
| row | integer | query | ดัชนีของแถว (เริ่มต้นที่ 0) ที่การแบ่งหน้าเริ่มต้น |
| startRow | integer | query | แถวแรกของช่วงการแบ่งหน้า |
| endRow | integer | query | แถวสุดท้ายของช่วงการแบ่งหน้า |
| folder | string | query | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานอยู่ |
| storageName | string | query | ชื่อของบริการพื้นที่จัดเก็บ |

**พารามิเตอร์ที่จำเป็น** – ต้องระบุ `cellname` **หรือ** `column` อย่างใดอย่างหนึ่ง เมื่อใช้ `column` คุณสามารถระบุ `row`, `startRow` และ `endRow` เพิ่มเติมเพื่อกำหนดช่วงได้ พารามิเตอร์อื่นๆ ทั้งหมดเป็นทางเลือก

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) นิยามอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบเปิดเผย และอนุญาตให้คุณดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

### ตัวอย่าง cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### คำตอบ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย | คำอธิบาย |
|------|-----------|----------|
| 200 | OK | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของ operation |
| 400 | Bad Request | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401 | Unauthorized | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย |
| 413 | Payload Too Large | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500 | Internal Server Error | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ และช่วยให้คุณมุ่งเน้นไปที่งานของโครงการของคุณ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}