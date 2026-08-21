---
title: "ดึงข้อมูลเซลล์จากช่วงที่ตั้งชื่อไว้"
second_title: "เอกสาร"
linktype: "ค่า"
type: docs
url: /th/ranges/get/values/
aliases: [  /th/get-cells-data-based-on-named-range/ ]
keywords: "Aspose.Cells, คลาวด์, REST API, Excel, ช่วงที่ตั้งชื่อไว้, ค่าเซลล์, ชีตงาน"
description: "ดึงค่าเซลล์จากช่วงที่ตั้งชื่อไว้ในชีตงาน Excel โดยใช้ Aspose.Cells Cloud REST API บริการนี้สามารถใช้งานได้ผ่าน SDK หลากหลายภาษา (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) และรองรับแพลตฟอร์มการพัฒนาที่หลากหลาย"
weight: 20
ArticleTitle: "ดึงข้อมูลเซลล์จากช่วงที่ตั้งชื่อไว้ – Aspose.Cells Cloud API"
---

**ข้อกำหนดเบื้องต้น**

- โทเคน JWT ที่ถูกต้องและมีขอบเขตที่เหมาะสม  
- ต้องอัปโหลดสมุดงานลงในที่จัดเก็บข้อมูลบนคลาวด์ของ Aspose Cloud (หรือโฟลเดอร์ที่ระบุไว้)  
- ต้องระบุชื่อที่จัดเก็บข้อมูลเป้าหมาย หากใช้ที่จัดเก็บข้อมูลที่ไม่ใช่ค่าเริ่มต้น

REST API นี้จะส่งคืนรายการเซลล์ภายในช่วงที่ระบุด้วยชื่อช่วง หรือด้วยดัชนีแถวและคอลัมน์

การดำเนินการนี้ช่วยให้นักพัฒนาสามารถดึงค่าเซลล์ที่อยู่ในช่วงที่ตั้งชื่อไว้เฉพาะในชีตงาน Excel ได้อย่างเป็นโปรแกรม โดยการส่ง `namedRange` หรือดัชนีแถวและคอลัมน์ที่ระบุ API จะส่งคืนรายการเซลล์โดยละเอียด ประกอบด้วยที่อยู่ แถว คอลัมน์ ค่า ประเภทข้อมูล และข้อมูลรูปแบบ การตอบกลับสามารถนำไปใช้ขับเคลื่อนแอปพลิเคชันที่ขับเคลื่อนด้วยข้อมูล สร้างรายงาน หรือดำเนินการคำนวณเพิ่มเติมบนเซิร์ฟเวอร์ Aspose.Cells Cloud รองรับภาษาการเขียนโปรแกรมต่างๆ ผ่าน SDK ทำให้สามารถบูรณาการได้อย่างราบรื่นไม่ว่าจะใช้แพลตฟอร์มการพัฒนาใด การใช้ HTTPS รับประกันการส่งข้อมูลอย่างปลอดภัย และ API ปฏิบัติตามหลักการแบบ RESTful โดยส่งรหัสสถานะ HTTP มาตรฐานสำหรับกรณีความสำเร็จและข้อผิดพลาด

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **พารามิเตอร์คำขอ**

| ชื่อพารามิเตอร์ | ประเภท | ตำแหน่ง | คำอธิบาย |
| -------------- | ------- | -------- | ------------------------------------------------------------------------------------------ |
| name           | string  | path     | ชื่อไฟล์สมุดงาน |
| sheetName      | string  | path     | ชื่อชีตงานภายในสมุดงาน |
| namedRange     | string  | query    | ช่วงที่ตั้งชื่อไว้ที่ต้องการดึงข้อมูล เช่น `A1:B2` หรือ `range_name1` |
| firstRow       | integer | query    | ดัชนีแถวแรกของช่วงแบบเริ่มต้นที่ 0 (ใช้เมื่อไม่ได้ระบุ `namedRange`) |
| firstColumn    | integer | query    | ดัชนีคอลัมน์แรกของช่วงแบบเริ่มต้นที่ 0 (ใช้เมื่อไม่ได้ระบุ `namedRange`) |
| rowCount       | integer | query    | จำนวนแถวที่รวมอยู่ในช่วง |
| columnCount    | integer | query    | จำนวนคอลัมน์ที่รวมอยู่ในช่วง |
| folder         | string  | query    | โฟลเดอร์ที่เก็บสมุดงานไว้ |
| storageName    | string  | query    | ชื่อที่จัดเก็บข้อมูลบนคลาวด์ที่สมุดงานนั้นอยู่ |

[สเปค OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ผ่านเว็บเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL บรรทัดคำสั่งเพื่อเรียกใช้บริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างด้านล่างแสดงวิธีการขอค่าเซลล์จากช่วงที่ตั้งชื่อไว้

{{< tabs tabTotal="2" tabID="1" tabName1="คำขอ" tabName2="การตอบกลับ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**หมายเหตุด้านความปลอดภัย:** ควรใช้ HTTPS เสมอเมื่อเรียกใช้ API บริการนี้ไม่รองรับ HTTP แบบไม่เข้ารหัส การใช้ HTTPS รับประกันว่าคำขอนั้นถูกเข้ารหัสและเป็นไปตามแนวทางปฏิบัติที่ดีด้านความปลอดภัย

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย |
|------|-----------------------------|--------------------------------------------------|
| 200  | สำเร็จ (OK)                          | ใช้ตัวกรองเรียบร้อยแล้ว การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | คำขอไม่ถูกต้อง (Bad Request)                 | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized)                | โทเคน JWT ไม่ถูกต้องหรือขาดหาย |
| 413  | ข้อมูลส่งข้อมูลใหญ่เกินไป (Payload Too Large)           | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error)       | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์ |

**ตัวอย่างการตอบกลับข้อผิดพลาด (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "พารามิเตอร์ 'namedRange' ขาดหายหรือไม่ถูกต้อง"
}
```

> **คำแนะนำ:** API ใช้ดัชนีแบบเริ่มต้นที่ 0 สำหรับ `firstRow` และ `firstColumn` ตัวอย่างเช่น แถวแรกของชีตงานคือ `0`

## ครอบครัว SDK บนคลาวด์

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK ซ่อนรายละเอียดระดับต่ำ ช่วยให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจ ดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}