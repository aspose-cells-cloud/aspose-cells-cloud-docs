---
title: "รับคุณสมบัติของเซลล์"
type: docs
url: /th/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, Worksheet, Cell Properties, Get Cells Properties"
description: "เรียนรู้วิธีใช้ REST API ของ Aspose.Cells Cloud เพื่อดึงคุณสมบัติของเซลล์ที่ระบุหรือเมธอดที่กำหนดไว้ล่วงหน้าของเซลล์ในไฟล์ Excel"
---

API REST นี้แสดงวิธีการดึงข้อมูลเซลล์ที่ระบุจากไฟล์ Excel

## API REST

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## การรักษาความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนแบบใช้โทเคน JWT](https://docs.aspose.cloud/th/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์คำขอ


| ชื่อพารามิเตอร์     | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                                                                                                                                                              |
| -------------------- | -------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | string   | path     | ชื่อของเอกสาร Excel                                                                                                                                                                   |
| **sheetName**        | string   | path     | ชื่อของชีตที่มีเซลล์                                                                                                                                                                  |
| **cellOrMethodName** | string   | path     | ชื่อเซลล์หรือชื่อเมธอดที่กำหนดไว้ล่วงหน้า (เช่น `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`) |
| **folder**           | string   | query    | โฟลเดอร์ที่จัดเก็บเอกสารไว้                                                                                                                                                            |
| **storageName**      | string   | query    | ชื่อของบริการจัดเก็บข้อมูล                                                                                                                                                            |

## **การตอบกลับ**

ส่งคืน CellResponse

- **ภาพรวมฟิลด์ของการตอบกลับ**

| ฟิลด์           | ชนิดข้อมูล | คำอธิบาย                                             |
| --------------- | --------- | ----------------------------------------------------- |
| `Name`          | string    | ที่อยู่ของเซลล์ (เช่น `F341`)                         |
| `Row`           | integer   | ดัชนีแถวแบบเริ่มต้นที่ 0                             |
| `Column`        | integer   | ดัชนีคอลัมน์แบบเริ่มต้นที่ 0                         |
| `Value`         | string    | ค่าที่แสดงของเซลล์                                   |
| `Type`          | string    | ชนิดข้อมูลของเซลล์ (เช่น `IsString`)                 |
| `Formula`       | string    | ข้อความสูตร หากเซลล์มีสูตร                                           |
| `IsFormula`     | bool      | ระบุว่าเซลล์มีสูตรหรือไม่                             |
| `IsMerged`      | bool      | ระบุว่าเซลล์เป็นส่วนหนึ่งของช่วงที่ถูกผนวกหรือไม่                 |
| `IsArrayHeader` | bool      | ระบุว่าเซลล์เป็นหัวตารางอาเรย์หรือไม่                       |
| `IsInArray`     | bool      | ระบุว่าเซลล์อยู่ในอาเรย์หรือไม่                           |
| `IsErrorValue`  | bool      | ระบุว่าเซลล์มีค่าผิดพลาดหรือไม่                            |
| `IsInTable`     | bool      | ระบุว่าเซลล์อยู่ภายในตารางหรือไม่                          |
| `IsStyleSet`    | bool      | ระบุว่ามีการใช้รูปแบบกับเซลล์หรือไม่                         |
| `HtmlString`    | string    | การแสดงค่าของเซลล์ในรูปแบบ HTML-encoding            |
| `Style.link`    | object    | ลิงก์ไปยังทรัพยากรรูปแบบ                               |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                    | คำอธิบาย                                                 |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองสำเร็จ; การตอบกลับมีรายละเอียดของOPERATION |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                               |
| 413  | ข้อมูลส่งไปมีขนาดใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                |
| 500  | ข้อผิดพลาดภายในเซิร์ฟเวอร์ (Internal Server Error) | เกิดข้อผิดพลาดที่ไม่คาดคิดของเซิร์ฟเวอร์                           |

## วิธีใช้ GetWorksheetCell API ด้วย SDK

### ข้อกำหนดเฉพาะของ API GetWorksheetCell

[ข้อกำหนด OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) กำหนดอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้โดยสาธารณะ และช่วยให้คุณสามารถดำเนินการ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านบรรทัดคำสั่งเพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่มีประสิทธิภาพที่สุดในการเร่งการพัฒนา SDK ช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่งานของโปรเจกต์ของคุณได้ โปรดตรวจสอบ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ทั้งหมดของ Aspose.Cells Cloud

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

### วิธีการดึงข้อมูลเซลล์ที่ระบุ

- [ดึงข้อมูลเซลล์จากชีตงาน](/th/cells/get-cell-data-from-a-worksheet/)
- [ดึงเซลล์แรกจากชีตงาน Excel](/th/cells/get-first-cell-from-excel-worksheet/)
- [ดึงเซลล์สุดท้ายของชีตงาน Excel](/th/cells/get-last-cell-of-excel-worksheet/)
- [ดึง MaxRow จากชีตงาน Excel](/th/cells/get-maxrow-from-excel-worksheet/)
- [ดึง MaxDataRow จากชีตงาน Excel](/th/cells/get-maxdatarow-from-excel-worksheet/)
- [ดึง MaxColumn จากชีตงาน Excel](/th/cells/get-maxcolumn-from-excel-worksheet/)
- [ดึง MaxDataColumn จากชีตงาน Excel](/th/cells/get-maxdatacolumn-from-excel-worksheet/)
- [ดึง MinRow จากชีตงาน Excel](/th/cells/get-minrow-from-excel-worksheet/)
- [ดึง MinDataRow จากชีตงาน Excel](/th/cells/get-mindatarow-from-excel-worksheet/)
- [ดึง MinColumn จากชีตงาน Excel](/th/cells/get-mincolumn-from-excel-worksheet/)
- [ดึง MinDataColumn จากชีตงาน Excel](/th/cells/get-mindatacolumn-from-excel-worksheet/)