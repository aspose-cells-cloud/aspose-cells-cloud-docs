---
---
title: "รับค่า MinDataRow จากสมุดงาน Excel"
type: docs
url: /get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, Cloud SDK"
description: "ดึงดัชนีแถวข้อมูลแรกของชีตงานโดยใช้ Aspose.Cells Cloud API เวอร์ชัน 3.0 ได้แก่ รูปแบบคำขอ พารามิเตอร์ ตัวอย่าง cURL ตัวอย่างการตอบกลับ โค้ดสถานะ HTTP และตัวอย่าง SDK"
ArticleTitle: "รับค่า MinDataRow จากสมุดงาน Excel – Aspose.Cells Cloud API"
---

จุดปลายทาง **Get MinDataRow** ของ **Aspose.Cells Cloud API เวอร์ชัน 3.0** จะส่งคืนดัชนีของแถวแรกที่มีข้อมูลในชีตงานที่ระบุ การดำเนินการนี้ต้องใช้โทเคนการเข้าถึงที่ถูกต้อง (การยืนยันตัวตนแบบ Bearer) และพารามิเตอร์คิวรี `cellOrMethodName` ตั้งค่าเป็น `mindatarow`

**เวอร์ชัน API: 3.0**

### ตัวอย่าง cURL

คำขอใช้เมธอด HTTP GET แทนค่าตัวแปร `{fileName}` และ `{sheetName}` ด้วยชื่อสมุดงานและชีตงานจริง

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**พารามิเตอร์คำขอ**

| พารามิเตอร์         | ตำแหน่ง | ชนิดข้อมูล | จำเป็น | คำอธิบาย                                                    |
|---------------------|----------|------------|--------|-------------------------------------------------------------|
| `fileName`          | Path     | string     | ใช่    | ชื่อสมุดงาน Excel (รวมส่วนขยายไฟล์ด้วย)                   |
| `sheetName`         | Path     | string     | ใช่    | ชื่อของชีตงานภายในสมุดงาน                                |
| `cellOrMethodName`  | Query    | string     | ใช่    | ต้องตั้งค่าเป็น `mindatarow` เพื่อเรียกใช้การดำเนินการนี้ |

**ตัวอย่างการตอบกลับ**

```json
{
  "MinDataRow": 5
}
```

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                  | คำอธิบาย                                                     |
|-----|----------------------------|--------------------------------------------------------------|
| 200 | สำเร็จ (OK)               | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400 | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ไม่ครบหรือไม่ถูกต้อง (เช่น ชนิดไฟล์ที่ไม่รองรับ) |
| 401 | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือไม่มี                                      |
| 413 | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                  |
| 500 | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดในเซิร์ฟเวอร์                             |

### ตัวอย่าง SDK

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นที่ตรรกะของโปรเจกต์ของคุณ โปรดดูที่ <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">ที่เก็บ GitHub</a> เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม**

- [รับค่า MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [รับค่า MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [รับค่า MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)