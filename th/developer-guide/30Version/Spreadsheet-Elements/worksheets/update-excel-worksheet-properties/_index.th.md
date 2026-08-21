---
title: "อัปเดตคุณสมบัติของแผ่นงาน – เอกสารอ้างอิง API Aspose.Cells Cloud (v3.0)"
second_title: "เอกสาร"
linktitle: "อัปเดต"
type: docs
url: /worksheets/update-properties/
aliases: [/update-excel-worksheet-properties/]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "worksheet",
    "update properties",
    "REST API",
    "cloud",
    "v3.0",
  ]
description: "เรียนรู้วิธีการอัปเดตคุณสมบัติพื้นฐาน (เช่น การแสดงค่าศูนย์, การแสดงเส้น rulers) ของแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API v3.0 รวมถึงตัวอย่างคำสั่ง cURL, ตัวอย่าง SDK, พารามิเตอร์ และการจัดการข้อผิดพลาด"
ArticleTitle: "อัปเดตคุณสมบัติของแผ่นงาน – เอกสารอ้างอิง API Aspose.Cells Cloud (v3.0)"
---

REST API นี้ใช้อัปเดตคุณสมบัติพื้นฐานของแผ่นงาน

## REST API

**ข้อกำหนดเบื้องต้น:** คุณต้องมีบัญชี Aspose Cloud ที่ถูกต้อง รับโทเค็น JWT เพื่อเข้าถึง และตรวจสอบให้แน่ใจว่าสมุดงานเป้าหมายถูกจัดเก็บไว้ในตำแหน่งที่จัดเก็บที่รองรับ คำขอทั้งหมดควรดำเนินการผ่าน **HTTPS**

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท   | เส้นทาง/สตริงการสอบถาม/เนื้อหา HTTP | คำอธิบาย                                                                                         |
| ---------------- | -------- | ------------------------------------ | ------------------------------------------------------------------------------------------------- |
| name             | string   | path                                 | ชื่อไฟล์สมุดงาน (รวมส่วนขยาย)                                                                   |
| sheetName        | string   | path                                 | ชื่อของแผ่นงานที่ต้องการอัปเดต                                                                  |
| sheet            | object   | body                                 | ออบเจกต์ JSON ที่มีคู่คีย์/ค่าของคุณสมบัติแผ่นงาน (เช่น `DisplayZeros`, `IsRulerVisible`)       |
| folder           | string   | query                                | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่สมุดงานตั้งอยู่                                               |
| storageName      | string   | query                                | ชื่อของพื้นที่จัดเก็บที่จะใช้                                                                     |

ออบเจกต์ **sheet** จะถูกส่งไปในเนื้อหาของคำขอในรูปแบบ JSON คุณสมบัติที่สามารถแก้ไขได้ได้แก่ `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible` และอื่นๆ ซึ่งกำหนดไว้ในข้อมูลจำเพาะของ API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการโต้ตอบแบบ REST โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
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

รหัสการตอบกลับทั่วไป:

- **200** – สำเร็จ คุณสมบัติของแผ่นงานได้รับการอัปเดตแล้ว
- **400** – คำขอไม่ถูกต้อง (เช่น JSON ผิดรูปแบบหรือขาดพารามิเตอร์ที่จำเป็น)
- **401** – ไม่ได้รับอนุญาต – ขาดโทเค็น JWT หรือโทเค็นไม่ถูกต้อง
- **404** – ไม่พบสมุดงานหรือแผ่นงาน
- **500** – ข้อผิดพลาดภายในเซิร์ฟเวอร์

| รหัส | ความหมาย |
|------|----------|
| 200 | สำเร็จ – คุณสมบัติของแผ่นงานได้รับการอัปเดตแล้ว |
| 400 | คำขอไม่ถูกต้อง – JSON ผิดรูปแบบหรือขาดพารามิเตอร์ที่จำเป็น |
| 401 | ไม่ได้รับอนุญาต – ขาดโทเค็น JWT หรือโทเค็นไม่ถูกต้อง |
| 404 | ไม่พบ – สมุดงานหรือแผ่นงานไม่มีอยู่จริง |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ |

## ชุดพัฒนาโปรแกรม (SDK) สำหรับคลาวด์

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานของโครงการของคุณได้ โปรดดูที่ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud อย่างสมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}