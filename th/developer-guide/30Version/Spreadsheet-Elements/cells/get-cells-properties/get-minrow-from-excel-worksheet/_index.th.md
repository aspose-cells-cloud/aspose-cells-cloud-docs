---
title: "รับค่า MinRow จากเวิร์กชีต Excel – ข้อมูลอ้างอิง API ของ Aspose.Cells Cloud"
type: docs
url: /get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, เวิร์กชีต Excel, REST API, ดัชนีแถวที่น้อยที่สุด, SDK บนคลาวด์"
description: "เรียนรู้วิธีดึงดัชนีแถวที่น้อยที่สุดของเวิร์กชีตโดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมถึงคำขอ cURL แบบเต็มรูปแบบพร้อมการตรวจสอบสิทธิ์ เครื่องมือแสดงโครงสร้างการตอบกลับ และตัวอย่าง SDK สำหรับหลายภาษา"
ArticleTitle: "รับค่า MinRow จากเวิร์กชีต Excel – ข้อมูลอ้างอิง API ของ Aspose.Cells Cloud"
---

API REST นี้จะส่งค่าดัชนีแถวที่น้อยที่สุดในเวิร์กชีต Excel เมื่อพารามิเตอร์ `cellOrMethodName` ถูกตั้งค่าเป็น `minrow` จุดปลายทางนี้สามารถใช้เพื่อกำหนดแถวแรกที่ไม่ว่างเปล่า (เริ่มนับจาก 0) ในเวิร์กชีตที่ระบุ

- **ตัวอย่าง cURL:**

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**คำขอ**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| คุณสมบัติ         | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                                |
|-------------------|------------|--------|----------------------------------------------------------|
| `fileName`        | สตริง      | ใช่    | ชื่อสมุดงาน (เช่น `myWorkbook.xlsx`)                     |
| `sheetName`       | สตริง      | ใช่    | เวิร์กชีตเป้าหมาย (เช่น `Sheet1`)                         |
| `cellOrMethodName`| สตริง      | ใช่    | ค่าคงที่คือ `minrow`                                      |
| `folder`          | สตริง      | ไม่บังคับ | เส้นทางโฟลเดอร์ในพื้นที่จัดเก็บบนคลาวด์                |
| `storageName`     | สตริง      | ไม่บังคับ | ชื่อพื้นที่จัดเก็บ หากใช้พื้นที่จัดเก็บที่ไม่ใช่ค่าเริ่มต้น |

**การตอบกลับ**

บริการจะส่งกลับวัตถุ JSON ที่มีคุณสมบัติ `MinRow` ซึ่งบ่งชี้ถึงดัชนีของแถวแรกที่ไม่ว่างเปล่า (เริ่มนับจาก 0)

| สถานะ HTTP | ความหมาย                                    |
|-------------|----------------------------------------------|
| 200         | สำเร็จ – มีข้อมูล JSON พร้อมค่า `MinRow`     |
| 401         | ไม่ได้รับอนุญาต – โทเคนไม่ถูกต้องหรือขาดหาย |
| 404         | ไม่พบสมุดงานหรือเวิร์กชีต                   |
| 500         | ข้อผิดพลาดภายในเซิร์ฟเวอร์                   |

ค่า `MinRow` มีประโยชน์เมื่อคุณต้องการค้นหาจุดเริ่มต้นของข้อมูลในชีตได้อย่างรวดเร็ว

- **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่โครงการของคุณได้ โปรดตรวจสอบ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">ที่เก็บบน GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ที่สมบูรณ์

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกบริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}