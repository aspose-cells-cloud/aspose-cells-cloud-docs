---
title: "Aspose.Cells Cloud API – รับค่า MaxDataColumn ของแผ่นงาน Excel (v3.0)"
type: docs
url: /get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, รับค่า MaxDataColumn, แผ่นงาน Excel, REST API, v3.0, SDK"
description: "ดึงดัชนีคอลัมน์สูงสุดที่มีข้อมูลในแผ่นงานที่ระบุโดยใช้ Aspose.Cells Cloud REST API (v3.0) รวมรายละเอียดคำขอ ตัวอย่างการตอบกลับ และตัวอย่าง SDK"
ArticleTitle: "Aspose.Cells Cloud API – รับค่า MaxDataColumn ของแผ่นงาน Excel (v3.0)"
---

API นี้คืนค่าดัชนีคอลัมน์ข้อมูลสูงสุดในแผ่นงาน Excel เมื่อพารามิเตอร์ `cellOrMethodName` ตั้งค่าเป็น `maxdatacolumn`

## **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**รายละเอียดคำขอ**  
- **วิธี HTTP:** `GET`  
- **รูปแบบจุดปลาย (Endpoint):** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **พารามิเตอร์เส้นทาง (Path parameters):**  
  - `fileName` – ชื่อไฟล์ Excel (เช่น `myWorkbook.xlsx`)  
  - `sheetName` – ชื่อแผ่นงาน (เช่น `Sheet1`)  
- **เฮดเดอร์ (Headers):**  
  - `Authorization: Bearer <access_token>` (จำเป็น)  
  - `Accept: application/json` (แนะนำ)  

**พารามิเตอร์**

| พารามิเตอร์ | ตำแหน่ง | ประเภท | จำเป็น | คำอธิบาย |
|-------------|----------|--------|--------|----------|
| `fileName` | เส้นทาง | string | ใช่ | ชื่อไฟล์ Excel ที่เก็บไว้ในพื้นที่จัดเก็บบนคลาวด์ |
| `sheetName` | เส้นทาง | string | ใช่ | แผ่นงานที่ต้องการรับค่าคอลัมน์ข้อมูลสูงสุด |
| `cellOrMethodName` | เส้นทาง | string | ใช่ | ต้องตั้งค่าเป็น `maxdatacolumn` เพื่อเรียกใช้การดำเนินการนี้ |

**การตอบกลับ**

| โค้ดสถานะ | คำอธิบาย | ตัวอย่าง Payload |
|-----------|----------|-----------------|
| 200 | ความสำเร็จ – คืนค่าดัชนีคอลัมน์ข้อมูลสูงสุด | `{ "MaxDataColumn": 12 }` |
| 401 | ไม่ได้รับอนุญาต – access token ไม่ถูกต้องหรือขาดหาย | `{ "error": "Invalid authentication." }` |
| 404 | ไม่พบ – ไฟล์หรือแผ่นงานไม่มีอยู่จริง | `{ "error": "Resource not found." }` |
| 500 | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน – เงื่อนไขที่ไม่คาดคิด | `{ "error": "Server error." }` |

**การจัดการข้อผิดพลาด**  
หากคำขอล้มเหลว ให้ตรวจสอบโค้ดสถานะ HTTP และข้อความ `error` ในเนื้อหาการตอบกลับ ตรวจสอบให้แน่ใจว่า access token ถูกต้อง และไฟล์รวมถึงแผ่นงานที่ระบุมีอยู่ในพื้นที่จัดเก็บ Aspose Cloud ของคุณ

- **ใช้ Aspose.Cells Cloud SDKs**

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ช่วยให้คุณมุ่งเน้นไปที่งานในโครงการของคุณ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บ Aspose.Cells ผ่าน SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}