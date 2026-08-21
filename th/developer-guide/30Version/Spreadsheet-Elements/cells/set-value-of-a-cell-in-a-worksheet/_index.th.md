---
title: "ตั้งค่าค่าในเซลล์ – คู่มืออ้างอิง API ของ Aspose.Cells Cloud (v3.0)"  
type: docs  
url: /th/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "API Aspose Cells ตั้งค่าค่าในเซลล์, อัปเดตเซลล์ Excel ผ่าน REST, ตัวอย่าง cURL ของ Aspose.Cells Cloud"  
description: "เรียนรู้วิธีการตั้งค่าค่าในเซลล์ที่กำหนดในสมุดงาน Excel ด้วย REST API ของ Aspose.Cells Cloud ซึ่งประกอบด้วยไวยากรณ์คำร้องขอ พารามิเตอร์ ตัวอย่าง cURL ผ่าน HTTPS และตัวอย่างโค้ด SDK"  
---  

API REST นี้ใช้ในการ **ตั้งค่าค่าในเซลล์** ของไฟล์ Excel  

## API REST  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## ความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้ [การยืนยันตัวตนแบบ JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  

**พารามิเตอร์ของคำร้องขอ**

| ชื่อพารามิเตอร์ | ประเภทข้อมูล | ตำแหน่ง | คำอธิบาย |
|------------------|-------------|---------|-----------|
| name             | string      | path    | ชื่อไฟล์ Excel (รวมนามสกุลด้วย) |
| sheetName        | string      | path    | ชื่อของแผ่นงาน (แยกแยะตัวพิมพ์เล็ก/ใหญ่) |
| cellName         | string      | path    | ที่อยู่เซลล์ในรูปแบบ A1 (เช่น `A1`) |
| value            | string      | query   | ค่าที่จะกำหนดให้กับเซลล์ |
| type             | string      | query   | ประเภทข้อมูลของค่า (`int`, `string`, `float` ฯลฯ) |
| formula          | string      | query   | สูตรที่จะใช้กับเซลล์ (ไม่บังคับ) |
| folder           | string      | query   | โฟลเดอร์ที่เก็บเอกสาร (ไม่บังคับ) |
| storageName      | string      | query   | ชื่อของพื้นที่จัดเก็บที่ไฟล์อยู่ (ไม่บังคับ) |

## **การตอบกลับ**

ส่งคืน CellResponse  

- **ภาพรวมฟิลด์ของการตอบกลับ**

| ชื่อฟิลด์         | ประเภทข้อมูล | คำอธิบาย |
|--------------------|-------------|----------|
| `Name`             | string      | ที่อยู่เซลล์ (เช่น `F341`) |
| `Row`              | integer     | ดัชนีแถวแบบเริ่มต้นที่ 0 |
| `Column`           | integer     | ดัชนีคอลัมน์แบบเริ่มต้นที่ 0 |
| `Value`            | string      | ค่าที่แสดงในเซลล์ |
| `Type`             | string      | ประเภทข้อมูลของเซลล์ (เช่น `IsString`) |
| `Formula`          | string      | ข้อความสูตรหากเซลล์มีสูตร |
| `IsFormula`        | bool        | ระบุว่าเซลล์มีสูตรหรือไม่ |
| `IsMerged`         | bool        | ระบุว่าเซลล์อยู่ในช่วงที่ถูกผนวกหรือไม่ |
| `IsArrayHeader`    | bool        | ระบุว่าเซลล์เป็นหัวตารางอาร์เรย์หรือไม่ |
| `IsInArray`        | bool        | ระบุว่าเซลล์อยู่ในอาร์เรย์หรือไม่ |
| `IsErrorValue`     | bool        | ระบุว่าเซลล์มีค่าข้อผิดพลาดหรือไม่ |
| `IsInTable`        | bool        | ระบุว่าเซลล์อยู่ในตารางหรือไม่ |
| `IsStyleSet`       | bool        | ระบุว่ามีการใช้รูปแบบให้กับเซลล์หรือไม่ |
| `HtmlString`       | string      | รูปแบบ HTML ของค่าในเซลล์ |
| `Style/link`       | object      | ลิงก์ไปยังทรัพยากรรูปแบบ |

```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                 | คำอธิบาย |
|------|---------------------------|----------|
| 200  | OK                        | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของOPERATION |
| 400  | Bad Request               | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ประเภทไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized              | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large         | ไฟล์ที่อัปโหลดเกินขีดจำกัดขนาด |
| 500  | Internal Server Error     | ข้อผิดพลาดของเซิร์ฟเวอร์ที่ไม่คาดคิด |

## วิธีใช้ API PostWorksheetCellSetValue ด้วย SDK

### ข้อมูลเฉพาะของ API PostWorksheetCellSetValue

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) นิยามอินเทอร์เฟซโปรแกรมที่เปิดเผยต่อสาธารณะ ซึ่งช่วยให้นักพัฒนาสามารถเรียกใช้ endpoint ของ REST API ได้โดยตรงจากเบราว์เซอร์หรือ HTTP client ใดก็ได้  

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเรียกใช้บริการเว็บของ Aspose.Cells ตัวอย่างต่อไปนี้แสดงวิธีการตั้งค่าค่าในเซลล์ด้วย cURL  

{{< tabs tabTotal="2" tabID="11" tabName11="คำร้องขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK จะช่วยเร่งการพัฒนาได้โดยจัดการรายละเอียดระดับต่ำให้คุณได้โฟกัสกับโปรเจกต์ของคุณ ดู [คลังข้อมูลบน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายการ SDK ของ Aspose.Cells Cloud อย่างครบถ้วน  

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}