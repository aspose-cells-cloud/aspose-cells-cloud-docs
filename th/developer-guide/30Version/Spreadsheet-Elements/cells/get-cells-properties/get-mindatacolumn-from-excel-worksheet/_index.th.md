---
title: "รับค่า MinDataColumn – เอกสารอ้างอิง API ของ Aspose.Cells Cloud (v3.0)"
type: docs
url: /th/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, แผ่นงาน Excel, REST API, เอกสารอ้างอิง API, v3.0, คอลัมน์ข้อมูล, cloud API"
description: "ดึงค่าดัชนีคอลัมน์ที่อยู่ทางซ้ายสุดที่มีข้อมูลในแผ่นงาน Excel ผ่าน Aspose.Cells Cloud REST API (v3.0) รวมถึงรายละเอียดการตรวจสอบสิทธิ์ ไวยากรณ์ของคำขอ ตัวอย่างการตอบกลับในรูปแบบ JSON รหัสข้อผิดพลาด และตัวอย่างโค้ด SDK"
ArticleTitle: "รับค่า MinDataColumn – เอกสารอ้างอิง API ของ Aspose.Cells Cloud (v3.0)"
---

ปลายทาง **`mindatacolumn`** จะส่งคืนดัชนีแบบ zero-based ของคอลัมน์ที่อยู่ทางซ้ายสุดซึ่งมีข้อมูลในเซลล์ใดๆ ของแผ่นงานที่ระบุ  
กล่าวอีกนัยหนึ่ง ปลายทางนี้จะบอกคุณว่าคอลัมน์ใดคือคอลัมน์แรกที่มีข้อมูลจริง

> **คำนิยาม** – `mindatacolumn`: คือดัชนี (เริ่มต้นที่ 0) ของคอลัมน์แรกที่มีข้อมูลในแผ่นงาน

**ข้อกำหนดเบื้องต้น**  
- ต้องมีโทเค็นการเข้าถึง OAuth2 ที่ถูกต้อง  
- ต้องอัปโหลดไฟล์ Excel ลงสู่พื้นที่จัดเก็บของ Aspose Cloud ก่อน

**พารามิเตอร์ของคำขอ**

| พารามิเตอร์               | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                      |
|---------------------------|------------|--------|-----------------------------------------------|
| `fileName`                | สายอักขระ  | ใช่    | ชื่อไฟล์ Excel ที่จัดเก็บอยู่ในพื้นที่จัดเก็บบนคลาวด์ |
| `sheetName`               | สายอักขระ  | ใช่    | ชื่อของแผ่นงานที่ต้องการดึงดัชนีคอลัมน์       |
| `Authorization` (ส่วนหัว) | สายอักขระ  | ใช่    | โทเค็นแบบ Bearer สำหรับการตรวจสอบสิทธิ์ OAuth2 |

- **ตัวอย่าง cURL**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                              |
|------|-------------------------------|-------------------------------------------------------|
| 200  | สำเร็จ (OK)                  | กรองข้อมูลเสร็จสิ้น; การตอบกลับประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)| โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                      |
| 413  | ข้อมูลส่วนหัวขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์ |

---

- ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้ ช่วยให้คุณสามารถมุ่งเน้นไปที่ตรรกะของโครงการของคุณได้ กรุณาตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}