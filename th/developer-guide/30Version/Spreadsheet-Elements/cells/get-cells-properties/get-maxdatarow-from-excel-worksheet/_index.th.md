---
title: "รับค่า MaxDataRow จากแผ่นงาน Excel"
type: docs
url: /th/get-maxdatarow-from-excel-worksheet/
weight: 50
keywords: "Excel, Aspose.Cells Cloud, REST API, รับค่า MaxDataRow, แผ่นงาน"
description: "ดึงดูดดัชนีของแถวสุดท้ายที่มีข้อมูลในแผ่นงานที่ระบุของสมุดงาน Excel โดยใช้ REST API ของ Aspose.Cells Cloud"
ArticleTitle: "Aspose.Cells Cloud API – รับค่า MaxDataRow จากแผ่นงาน Excel"
---

REST API นี้จะคืนค่าดัชนีแถวข้อมูลสูงสุดในไฟล์ Excel เมื่อพารามิเตอร์ `cellOrMethodName` ถูกตั้งค่าเป็น `maxdatarow`

- **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatarow" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

*หมายเหตุ: คำขอต้องส่งผ่าน **HTTPS** และต้องมีโทเคน bearer OAuth2 ที่ถูกต้อง*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataRow": 57
}
```

**โค้ดสถานะ HTTP ที่เป็นไปได้**

| โค้ด | คำอธิบาย |
|------|-------------|
| 200 | สำเร็จ – คืนค่าดัชนีแถวข้อมูลสูงสุด |
| 401 | ไม่ได้รับอนุญาต – โทเคนการยืนยันตัวตนไม่ถูกต้องหรือขาดหายไป |
| 403 | ถูกปฏิเสธการเข้าถึง – สิทธิ์ไม่เพียงพอในการเข้าถึงสมุดงาน |
| 404 | ไม่พบ – สมุดงานหรือแผ่นงานที่ระบุไม่มีอยู่จริง |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิดของเซิร์ฟเวอร์ |

{{< /tab >}}

{{< /tabs >}}


- **ใช้ SDK ของ Aspose.Cells Cloud**

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำ ช่วยให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ กรุณาดูที่ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อรับรายการ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7b834250a25feb5b8a30500cf62cf7a9" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม**

- <a href="https://docs.aspose.cloud/cells/th/get-maxrow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">รับค่า MaxRow จากแผ่นงาน Excel</a>  
- <a href="https://docs.aspose.cloud/cells/th/get-maxcolumn-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">รับค่า MaxColumn จากแผ่นงาน Excel</a>  
- <a href="https://docs.aspose.cloud/cells/th/get-mindatarow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">รับค่า MinDataRow จากแผ่นงาน Excel</a>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Aspose.Cells Cloud Get MaxDataRow",
  "description": "คืนค่าดัชนีของแถวสุดท้ายที่มีข้อมูลในแผ่นงานที่ระบุ",
  "url": "https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatarow",
  "method": "GET",
  "documentation": "https://docs.aspose.cloud/cells/th/get-maxdatarow-from-excel-worksheet/",
  "input": [
    {
      "name": "fileName",
      "valueRequired": true,
      "description": "ชื่อของสมุดงาน Excel"
    },
    {
      "name": "sheetName",
      "valueRequired": true,
      "description": "ชื่อของแผ่นงาน"
    }
  ],
  "output": {
    "@type": "DataType",
    "name": "MaxDataRow",
    "description": "ดัชนีแบบเริ่มต้นที่ 0 ของแถวสุดท้ายที่มีข้อมูล"
  }
}
</script>

*อัปเดตล่าสุด: 30 กรกฎาคม 2026*