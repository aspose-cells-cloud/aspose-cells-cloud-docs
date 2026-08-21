---
title: "ยกเลิกการจัดกลุ่มแถวในสมุดงาน Excel"
second_title: "เอกสาร"
linktitle: "ยกเลิกการจัดกลุ่ม"
type: docs
url: /rows/ungroup/
aliases: [/ungroup-rows-in-excel-worksheet/]
keywords: "ยกเลิกการจัดกลุ่มแถว, Excel, Aspose.Cells Cloud, REST API, SDK, สเปรดชีต"
description: "เรียนรู้วิธีการยกเลิกการจัดกลุ่มแถวในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API และ SDK สำหรับภาษาโปรแกรมต่างๆ"
weight: 70
---

REST API นี้ใช้สำหรับยกเลิกการจัดกลุ่มแถวในสมุดงาน Excel

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | ----------------------------------------------------------- |
| name           | string  | path     | ชื่อสมุดงาน |
| sheetName      | string  | path     | ชื่อตารางงาน |
| firstIndex     | integer | query    | ดัชนีเริ่มต้นแบบศูนย์ (zero-based index) ของแถวแรกที่จะยกเลิกการจัดกลุ่ม |
| lastIndex      | integer | query    | ดัชนีสิ้นสุดแบบศูนย์ (zero-based index) ของแถวสุดท้ายที่จะยกเลิกการจัดกลุ่ม |
| isAll          | boolean | query    | หากเป็น **true** จะยกเลิกการจัดกลุ่มแถวทั้งหมดในช่วงที่ระบุ |
| folder         | string  | query    | โฟลเดอร์ที่เก็บสมุดงานไว้ |
| storageName    | string  | query    | ชื่อของพื้นที่จัดเก็บที่สมุดงานอยู่ |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้จากภายนอก และช่วยให้คุณสามารถดำเนินการโต้ตอบผ่าน REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ที่รันผ่านคำสั่งในบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียก API บนคลาวด์โดยใช้ cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
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

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณมุ่งเน้นไปที่งานของโครงการของคุณ โปรดตรวจสอบ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}