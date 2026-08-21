---
title: "ดึงข้อมูลเซลล์จากเวิร์กชีต"
type: docs
url: /th/get-cell-data-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells Cloud, ดึงข้อมูลเซลล์, Excel API, REST API, ค่าเซลล์, worksheet API, ตัวอย่าง Aspose API"
description: "ดึงค่า ชนิด และรูปแบบของเซลล์เดียวจากเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ประกอบด้วยตัวอย่าง cURL, SDK, พารามิเตอร์ และการจัดการข้อผิดพลาด"
---

REST API นี้จะดึงข้อมูลเซลล์จากเวิร์กชีต Excel เมื่อพารามิเตอร์ **`cellOrMethodName`** กำหนดชื่อเซลล์ (รูปแบบที่อยู่แบบ A1 เช่น `A3`)

- **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="คำร้องขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**พารามิเตอร์**

| พารามิเตอร์          | ชนิดข้อมูล | คำอธิบาย                                                      | จำเป็น |
|----------------------|------------|---------------------------------------------------------------|--------|
| `cellOrMethodName`   | string     | ต้องกำหนดเป็น `firstcell` เพื่อดึงข้อมูลเซลล์แรก             | ใช่    |
| `fileName`           | string     | ชื่อไฟล์สมุดงาน (เช่น `myWorkbook.xlsx`)                      | ใช่    |
| `worksheet`          | string     | ชื่อเวิร์กชีต (เช่น `Sheet1`)                                 | ใช่    |
| `Authorization`      | header     | Bearer token สำหรับการยืนยันตัวตน                            | ใช่    |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

- **ใช้ SDK ของ Aspose.Cells Cloud**

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}