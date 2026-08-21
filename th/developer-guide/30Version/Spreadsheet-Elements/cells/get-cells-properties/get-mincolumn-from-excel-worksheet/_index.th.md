---
title: "รับค่า MinColumn จากแผ่นงาน Excel"
type: docs
url: /get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Get MinColumn, Worksheet, SDK, Cloud API
description: ดึงดูดดัชนีคอลัมน์ที่น้อยที่สุดที่มีข้อมูลในแผ่นงานของไฟล์ Excel ผ่าน REST API ของ Aspose.Cells Cloud
ArticleTitle: "รับค่า MinColumn จากแผ่นงาน Excel - Aspose.Cells Cloud API"
---

REST API นี้จะส่งค่าดัชนีคอลัมน์ที่น้อยที่สุดที่มีข้อมูลในแผ่นงาน Excel เมื่อพารามิเตอร์ `cellOrMethodName` ถูกตั้งค่าเป็น `mincolumn`

- **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**รายละเอียดของคำขอ**

| พารามิเตอร์ | ประเภทข้อมูล | จำเป็น | คำอธิบาย |
|-----------|------|----------|-------------|
| `cellOrMethodName` | string | จำเป็น | ค่าคงที่ `mincolumn` เพื่อระบุการดำเนินการ |
| `folder` | string | ไม่จำเป็น | ตำแหน่งที่อยู่ของโฟลเดอร์ที่เก็บสมุดงาน (หากไม่ได้อยู่ในรูท) |
| `storageName` | string | ไม่จำเป็น | ชื่อพื้นที่จัดเก็บของ Aspose Cloud ที่จะใช้งาน |

**รายละเอียดของการตอบกลับ**

API จะส่งคืนวัตถุ JSON ที่มีคุณสมบัติเดียวคือ:

```json
{
  "MinColumn": integer   // ดัชนีของคอลัมน์ที่อยู่ทางซ้ายสุดที่มีข้อมูล (เริ่มนับจาก 0)
}
```

รหัสสถานะ HTTP ที่พบได้บ่อย:

- **200 OK** – คำขอสำเร็จ ส่งค่า `MinColumn` กลับมา  
- **401 Unauthorized** – ไม่มีหรือโทเค็นการยืนยันตัวตนไม่ถูกต้อง  
- **404 Not Found** – สมุดงาน แผ่นงาน หรือช่วงเซลล์ที่ระบุไม่มีอยู่จริง  
- **500 Internal Server Error** – เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์

- **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการพัฒนา SDK จะช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะของโปรเจกต์ของคุณได้ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}