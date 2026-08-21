---
title: "ซ่อนแผ่นงานใน Excel"
second_title: "เอกสาร"
linktype: "ซ่อน"
type: docs
url: /th/worksheets/hide/
aliases: [  /th/hide-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, Excel, ซ่อนแผ่นงาน, REST API, สเปรดชีต"
description: "คู่มือทีละขั้นตอนในการซ่อนแผ่นงานในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API พร้อมรายละเอียดคำขอ ตัวอย่าง cURL และโค้ดตัวอย่าง SDK สำหรับภาษาต่างๆ"
weight: 50
---

REST API นี้ใช้ในการซ่อนแผ่นงาน

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **พารามิเตอร์ของคำขอ**

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                                                 |
| ---------------- | --------- | -------- | ------------------------------------------------------------------------ |
| name             | string    | path     | ชื่อไฟล์สมุดงาน Excel                                                   |
| sheetName        | string    | path     | ชื่อแผ่นงานที่ต้องการแก้ไข                                              |
| isVisible        | boolean   | query    | ตัวบ่งชี้สถานะการมองเห็น (`true` สำหรับแสดงผล, `false` สำหรับซ่อน)     |
| folder           | string    | query    | เส้นทางโฟลเดอร์ที่เก็บสมุดงาน                                           |
| storageName      | string    | query    | ชื่อของบริการจัดเก็บข้อมูล                                               |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่เข้าถึงได้แบบเปิดเผย และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=false" \
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

## ครอบครัว Cloud SDK

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-HideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-HideWorksheet-hide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideExcelWorkSheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-HideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-HideWorksheet-hide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-HideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "cb5a1656cea2f870f0a5ef6d066525ef" >}}

{{< /tab >}}

{{< /tabs >}}