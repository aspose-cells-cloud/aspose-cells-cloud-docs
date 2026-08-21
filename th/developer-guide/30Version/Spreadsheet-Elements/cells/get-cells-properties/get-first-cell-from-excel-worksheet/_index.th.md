---
title: "รับเซลล์แรก (A1) จากแผ่นงาน Excel"
type: docs
url: /th/get-first-cell-from-excel-worksheet/
weight: 20
keywords: "Aspose.Cells Cloud, Excel, REST API, รับเซลล์แรก, แผ่นงาน, A1, API v3"
description: "เรียนรู้วิธีดึงค่าเซลล์แรก (A1) ของแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API เวอร์ชัน 3.0 รวมถึงตัวอย่างคำสั่ง cURL, โครงสร้าง JSON ของการตอบกลับ, ตัวอย่างข้อผิดพลาด และตัวอย่าง SDK สำหรับ C#, Java, PHP, Python และอื่นๆ"
ArticleTitle: "รับเซลล์แรก (A1) จากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud API"
---

REST API นี้แสดงวิธีการดึงค่า **เซลล์แรก** ในไฟล์ Excel เมื่อพารามิเตอร์ `cellOrMethodName` ถูกตั้งค่าเป็น `firstcell`

**จุดปลายทาง (Endpoint)**  
`GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{worksheet}/cells/firstcell`

- **ตัวอย่าง cURL**

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/firstcell" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**พารามิเตอร์**

| พารามิเตอร์         | ประเภท   | คำอธิบาย                                                     | จำเป็น |
|----------------------|----------|--------------------------------------------------------------|--------|
| `cellOrMethodName`   | string   | ต้องตั้งค่าเป็น `firstcell` เพื่อดึงค่าเซลล์แรก                | ใช่    |
| `fileName`           | string   | ชื่อไฟล์สมุดงาน (เช่น `myWorkbook.xlsx`)                      | ใช่    |
| `worksheet`          | string   | ชื่อแผ่นงาน (เช่น `Sheet1`)                                   | ใช่    |
| `Authorization`      | header   | Bearer token สำหรับการยืนยันตัวตน                            | ใช่    |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A1",
    "Row": 0,
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

**การตอบกลับข้อผิดพลาด**

- **401 ไม่ได้รับอนุญาต (Unauthorized)**

```json
{
  "Code": "401",
  "Message": "โทเคนการเข้าถึงไม่ถูกต้อง"
}
```

- **404 ไม่พบ (Not Found)**

```json
{
  "Code": "404",
  "Message": "สมุดงาน, แผ่นงาน หรือเซลล์ที่ระบุไม่มีอยู่จริง"
}
```

- **500 ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)**

```json
{
  "Code": "500",
  "Message": "เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                      | คำอธิบาย                                                |
|------|--------------------------------|----------------------------------------------------------|
| 200  | สำเร็จ (OK)                   | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ оперATION อยู่ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)  | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                            |
| 413  | ข้อมูลในคำขอมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนดไว้             |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                 |

{{< /tab >}}

{{< /tabs >}}

- **ครอบครัว SDK สำหรับคลาวด์**

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดตรวจสอบ [คลังข้อมูล GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

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
---