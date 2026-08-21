---
title: "การรับรูปแบบเซลล์จากเวิร์กชีต – Aspose.Cells Cloud API"
type: docs
url: /th/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, รูปแบบเซลล์, สเปรดชีต, SDK บนคลาวด์, เอกสาร API"
description: "เรียนรู้วิธีดึงรูปแบบของเซลล์เฉพาะในเวิร์กชีต Excel โดยใช้ Aspose.Cells Cloud REST API เวอร์ชัน 3 รวมตัวอย่าง cURL โครงสร้างการตอบกลับ รหัสสถานะ และตัวอย่างโค้ด SDK"
ArticleTitle: "การรับรูปแบบเซลล์จากเวิร์กชีตโดยใช้ Aspose.Cells Cloud API – คู่มือแบบละเอียด"
---

ใช้ REST API นี้เพื่อดึง **รูปแบบ** ของเซลล์ในเวิร์กชีต Excel

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **ความปลอดภัยและการยืนยันตัวตน**

Aspose.Cells Cloud APIs มีความปลอดภัยและต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนด้วย JWT token</a>

### พารามิเตอร์คำขอ


| ชื่อพารามิเตอร์ | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                           |
| ---------------- | -------- | ------- | ---------------------------------- |
| name             | string   | path    | ชื่อของเอกสาร Excel                |
| sheetName        | string   | path    | ชื่อของเวิร์กชีต                   |
| cellName         | string   | path    | ที่อยู่ของเซลล์ (เช่น A1)          |
| folder           | string   | query   | โฟลเดอร์ที่เก็บไฟล์                |
| storageName      | string   | query   | ชื่อของพื้นที่จัดเก็บที่จะใช้งาน    |


### **การตอบกลับ**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                                   |
|------|----------------------------|------------------------------------------------------------|
| 200  | สำเร็จ (OK)                | ใช้ตัวกรองเรียบร้อยแล้ว; การตอบกลับมีรายละเอียดของ оперation |
| 400  | คำขอไม่ถูกต้อง (Bad Request) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)     |
| 401  | ไม่ได้รับอนุญาต (Unauthorized) | JWT token ไม่ถูกต้องหรือขาดหาย                              |
| 413  | ข้อมูลในคำขอใหญ่เกินไป (Payload Too Large) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                           |
| 500  | ข้อผิดพลาดของเซิร์ฟเวอร์ภายใน (Internal Server Error) | ข้อผิดพลาดที่ไม่คาดคิดเกิดขึ้นในเซิร์ฟเวอร์                 |

**การตอบกลับข้อผิดพลาด**  
รูปแบบข้อผิดพลาดทั่วไปสำหรับปลายทางนี้เป็นไปตามรูปแบบข้อผิดพลาดมาตรฐานของ Aspose.Cells ตัวอย่างเช่น การตอบกลับ 400 Bad Request จะส่งคืน:

```json
{
  "Code": 400,
  "Message": "Invalid parameter 'cellName'.",
  "Description": "The cell name provided is not in a valid A1 format."
}
```

ในทำนองเดียวกัน การตอบกลับ 401 Unauthorized จะส่งคืน:

```json
{
  "Code": 401,
  "Message": "Authentication failed.",
  "Description": "The JWT token is missing or invalid."
}
```

## วิธีใช้ GetWorksheetCellStyle API ร่วมกับ SDKs

### ข้อกำหนดเฉพาะของ GetWorksheetCellStyle API

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) กำหนดอินเทอร์เฟซโปรแกรมที่เข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงจากเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่ง command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="การตอบกลับ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## โครงสร้างการตอบกลับ

| ฟิลด์                    | ชนิดข้อมูล | คำอธิบาย                                                                   |
| ------------------------ | ---------- | -------------------------------------------------------------------------- |
| **Style**                | object     | คอนเทนเนอร์สำหรับคุณสมบัติทั้งหมดที่เกี่ยวข้องกับรูปแบบของเซลล์            |
| Style.Font               | object     | การตั้งค่าฟอนต์ (ชื่อ ขนาด สี ป้ายกำกับรูปแบบ)                             |
| Style.Font.Color         | object     | ค่าสี RGBA ของฟอนต์                                                         |
| Style.Font.IsBold        | boolean    | เป็น `true` หากฟอนต์เป็นตัวหนา                                               |
| Style.Font.IsItalic      | boolean    | เป็น `true` หากฟอนต์เป็นตัวเอียง                                             |
| Style.Font.IsStrikeout   | boolean    | เป็น `true` หากฟอนต์มีขีดเส้นใต้                                             |
| Style.Font.IsSubscript   | boolean    | เป็น `true` หากฟอนต์เป็นตัวห้อย                                             |
| Style.Font.IsSuperscript | boolean    | เป็น `true` หากฟอนต์เป็นตัวยก                                               |
| Style.Font.Name          | string     | ชื่อครอบครัวของฟอนต์ (เช่น **Calibri**)                                   |
| Style.Font.Size          | number     | ขนาดฟอนต์เป็นจุด (points)                                                   |
| Style.Font.Underline     | string     | รูปแบบขีดเส้นใต้ (เช่น **Single**)                                         |
| Style.IsLocked           | boolean    | ระบุว่าเซลล์ถูกป้องกันจากการแก้ไขหรือไม่                                   |
| Style.IsTextWrapped      | boolean    | เป็น `true` หากเปิดใช้งานการตัดข้อความให้พอดีกับช่อง                         |
| Style.IsGradient         | boolean    | เป็น `true` หากมีการใช้การเติมแบบไล่สี (gradient)                           |
| Style.Pattern            | string     | ชื่อรูปแบบการเติม (เช่น **None**)                                          |
| Style.BorderCollection   | array      | รายการออบเจกต์เส้นขอบที่กำหนดรูปแบบเส้น สี และประเภทเส้นขอบ                 |
| Style.BackgroundColor    | object     | ค่า RGBA สำหรับพื้นหลังของเซลล์                                             |
| Style.ForegroundColor    | object     | ค่า RGBA สำหรับพื้นหน้าของเซลล์                                            |
| …                        | …          | _(ฟิลด์อื่น ๆ อยู่ในรูปแบบเดียวกันตามที่กำหนดไว้ในเอกสารอ้างอิง API)_   |

### ใช้ Aspose.Cells Cloud SDKs

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งความเร็วในการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ ทำให้คุณสามารถมุ่งเน้นไปที่งานโครงการของคุณได้ กรุณาดูที่ [GitHub repository](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่าง ๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม**  
- [ตั้งค่ารูปแบบเซลล์](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [รับค่าเซลล์](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---