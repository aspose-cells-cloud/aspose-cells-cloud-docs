---
title: "ยกเลิกการจับช่วงข้อมูลในแผ่นงาน Excel"
second_title: "เอกสาร"
linktitle: "ยกเลิกการจับช่วงข้อมูล"
type: docs
url: /th/worksheets/panes/unfreeze/
aliases:
  - /unfreeze-panes-in-excel-worksheet/
  - /worksheets/unfreeze-panes/
keywords: "ยกเลิกการจับช่วงข้อมูล, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Python, Node.js, Go, Swift, Android, Ruby, Perl"
description: "เรียนรู้วิธีการยกเลิกการจับช่วงข้อมูลในแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) พร้อมตัวอย่าง cURL และตัวอย่างโค้ด SDK สำหรับ C#, Java, Python และอื่นๆ อีกมากมาย"
weight: 200
---

คำสั่ง REST API นี้ **ยกเลิกการจับช่วงข้อมูล** (ลบการจับช่วงข้อมูลที่ถูกจับไว้) ในแผ่นงาน Excel

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                        |
| ---------------- | --------- | -------- | ------------------------------------------------ |
| `name`           | string    | path     | ชื่อไฟล์ Excel                                   |
| `sheetName`      | string    | path     | ชื่อแผ่นงาน                                     |
| `folder`         | string    | query    | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บที่ไฟล์ตั้งอยู่   |
| `storageName`    | string    | query    | ชื่อของพื้นที่จัดเก็บ Aspose Cloud              |

_ไม่จำเป็นต้องมีพารามิเตอร์คิวรีเพิ่มเติม (เช่น row, column, frozenRows หรือ frozenColumns) สำหรับการดำเนินการยกเลิกการจับช่วงข้อมูล_

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetFreezePanes) กำหนดอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้โดยสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงเว็บเซอร์วิสของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes" \
-X DELETE \
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

## ครอบครัว SDK สำหรับคลาวด์

การใช้งาน SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับล่างให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [GitHub Repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้เว็บเซอร์วิสของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsDeleteWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnfreezePanes-unfreeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-DeleteWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-unfreeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnfreezePanesInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnfreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnfreezePanes-unfreeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnfreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "23052de16f4f1cd75542ce4ae9b3ada8" >}}

{{< /tab >}}

{{< /tabs >}}