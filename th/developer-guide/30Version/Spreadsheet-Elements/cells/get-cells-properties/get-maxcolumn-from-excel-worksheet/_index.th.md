---
title: "รับค่า MaxColumn จากสมุดงาน Excel"
type: docs
url: /th/get-maxcolumn-from-excel-worksheet/
weight: 60
keywords: "Aspose Cells API, maxcolumn, สมุดงาน Excel, REST, SDK"
description: "ดึงดัชนีคอลัมน์สูงสุดของแผ่นงานโดยใช้ Aspose.Cells Cloud API รวมถึงคำขอ cURL พร้อมการตรวจสอบสิทธิ์ เครื่องหมายรูปแบบการตอบกลับ พารามิเตอร์ รหัสข้อผิดพลาด และตัวอย่าง SDK (C#, Java, Python เป็นต้น)"
---

API นี้จะส่งคืนดัชนีคอลัมน์สูงสุดของแผ่นงานในสมุดงาน Excel เมื่อพารามิเตอร์ `cellOrMethodName` ถูกตั้งค่าเป็น `maxcolumn`


- **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxcolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxColumn": 15
}
```

{{< /tab >}}

{{< /tabs >}}


- **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้ ช่วยให้คุณมุ่งเน้นไปที่ตรรกะของโปรเจกต์ของคุณ โปรดดูที่ [ kho ithub ของ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxColumnWorksheet-get-max-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxColumnWorksheet-get-max-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- ตัวอย่าง Swift (ยังไม่มีให้ใช้งาน) -->

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3282f0b23cd22dbd0adee0f1fbd0bf2c" >}}

{{< /tab >}}

{{< /tabs >}}