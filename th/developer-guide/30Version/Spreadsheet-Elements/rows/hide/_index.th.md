---
title: "ซ่อนแถวในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "ซ่อน"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "ซ่อนแถว, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "เรียนรู้วิธีการซ่อนแถวเดียวหรือหลายแถวในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมตัวอย่าง cURL, โค้ดตัวอย่าง SDK, พารามิเตอร์, การยืนยันตัวตน, รายละเอียดการตอบกลับ และการจัดการข้อผิดพลาด"
weight: 40
ArticleTitle: "ซ่อนแถวในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้ซ่อนแถวในสมุดงาน Excel

**ข้อกำหนดเบื้องต้น:** โทเค็น JWT Bearer ที่ถูกต้องซึ่งได้รับจากปลายทาง OAuth ของ Aspose Cloud, สมุดงานที่เก็บไว้ในพื้นที่จัดเก็บของ Aspose Cloud และชื่อของเวิร์กชีตที่มีแถวที่ต้องการซ่อน API นี้ใช้ได้กับไฟล์ Excel ในรูปแบบ XLS, XLSX และรูปแบบอื่นๆ ที่รองรับ

## API PostHideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วยโทเค็น JWT Bearer</a>

### พารามิเตอร์คำขอ

| พารามิเตอร์       | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                 |
| ----------------- | ---------- | -------- | ------------------------------------------------------------------------ |
| **name**          | string     | path     | ชื่อไฟล์สมุดงาน                                                         |
| **sheetName**     | string     | path     | ชื่อของเวิร์กชีตที่มีแถวที่ต้องการซ่อน                                  |
| **startrow**      | integer    | query    | ดัชนีแบบเริ่มต้นที่ 0 ของแถวแรกที่จะถูกซ่อน                             |
| **totalRows**     | integer    | query    | จำนวนแถวต่อเนื่องที่จะถูกซ่อน โดยเริ่มจาก **startrow**                  |
| **folder**        | string     | query    | โฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานตั้งอยู่                               |
| **storageName**   | string     | query    | ชื่อของบริการพื้นที่จัดเก็บ                                             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) ให้ส่วนติดต่อโปรแกรมที่เข้าถึงได้แบบสาธารณะ ซึ่งช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเรียกใช้บริการเว็บของ Aspose.Cells ซึ่ง API นี้ต้องใช้โทเค็น JWT Bearer ที่ได้รับจากปลายทาง OAuth ของ Aspose Cloud โดยต้องระบุในส่วนหัว `Authorization` ตัวอย่างด้านล่างแสดงวิธีการซ่อนแถวโดยใช้ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
  -X POST \
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

**โค้ดสถานะการตอบกลับ**

| โค้ด | คำอธิบาย                                     |
|-----|---------------------------------------------|
| 200 | สำเร็จ – แถวถูกซ่อน                         |
| 400 | คำขอผิดพลาด – พารามิเตอร์ไม่ถูกต้อง        |
| 401 | ไม่ได้รับอนุญาต – ไม่มีหรือโทเค็น JWT ไม่ถูกต้อง |
| 404 | ไม่พบ – สมุดงานหรือเวิร์กชีตไม่มีอยู่จริง  |
| 500 | ข้อผิดพลาดของเซิร์ฟเวอร์ – การประมวลผลภายในล้มเหลว |

การเรียกที่สำเร็จจะส่งคืนวัตถุ JSON ที่มีฟิลด์ `Code` และ `Status` กรณีที่เกิดข้อผิดพลาด การตอบกลับจะประกอบด้วยฟิลด์เพิ่มเติม เช่น `Message` และโค้ดสถานะ HTTP ที่เหมาะสม (เช่น 400, 401, 404, 500)

**หมายเหตุ:** ตรวจสอบให้แน่ใจว่าค่า `startrow` อยู่ในช่วงของแถวของเวิร์กชีต มิฉะนั้น API จะส่งคืนข้อผิดพลาด 400 ดัชนีของแถวเป็นแบบเริ่มต้นที่ 0 ดังนั้น `startrow=0` หมายถึงแถวแรก

## ครอบครัว SDK สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการผสานรวมฟังก์ชันนี้เข้ากับแอปพลิเคชันของคุณ SDK จะจัดการรายละเอียดระดับต่ำ ให้คุณสามารถมุ่งเน้นที่ตรรกะทางธุรกิจได้ ดู [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการซ่อนแถวโดยใช้ SDK ต่างๆ (ชื่อไฟล์ตัวอย่างอ้างอิงถึง “Unhide” เนื่องจากชื่อเดิม แต่โค้ดภายใน gist แต่ละอันดำเนินการซ่อนแถวจริง)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}