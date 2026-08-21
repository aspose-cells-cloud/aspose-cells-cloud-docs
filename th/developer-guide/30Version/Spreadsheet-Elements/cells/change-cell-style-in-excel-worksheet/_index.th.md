---
title: "เปลี่ยนรูปแบบเซลล์ในสมุดงาน Excel"
type: docs
url: /change-cell-style-in-excel-worksheet/
weight: 30
keywords:
  - Aspose.Cells
  - Aspose.Cells Cloud
  - Excel
  - Cell Style (รูปแบบเซลล์)
  - REST API
  - Cloud SDK
  - cURL
  - cell style update (การอัปเดตรูปแบบเซลล์)
  - Excel API
description: "เรียนรู้วิธีการอัปเดตรูปแบบของเซลล์เฉพาะในสมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API ซึ่งรวมถึงตัวอย่างคำขอ คำตอบ และโค้ดตัวอย่าง SDK"
ArticleTitle: "เปลี่ยนรูปแบบเซลล์ในสมุดงาน Excel – คู่มือ API ของ Aspose.Cells Cloud"
---

REST API นี้ใช้สำหรับการอัปเดต **รูปแบบเซลล์** ของไฟล์ Excel

## PostUpdateWorksheetCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **การรักษาความปลอดภัยและการตรวจสอบสิทธิ์**

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การตรวจสอบสิทธิ์แบบ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">โทเค็น JWT</a>

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท   | ตำแหน่ง | คำอธิบาย                                         |
|----------------|--------|----------|--------------------------------------------------|
| name           | string | path     | ชื่อไฟล์สมุดงาน                                |
| sheetName      | string | path     | ชื่อของแผ่นงาน                                 |
| cellName       | string | path     | เซลล์เป้าหมาย (เช่น **A1**)                    |
| style          | object | body     | ออบเจกต์ JSON ที่กำหนดการตั้งค่ารูปแบบที่จะใช้กับเซลล์ |
| folder         | string | query    | โฟลเดอร์ที่เก็บสมุดงาน                        |
| storageName    | string | query    | ชื่อพื้นที่จัดเก็บที่สมุดงานถูกเก็บไว้         |

### **คำตอบ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                   | คำอธิบาย                                          |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK (สำเร็จ)                | ตัวกรองถูกใช้งานเรียบร้อย; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ |
| 400  | Bad Request (คำขอไม่ถูกต้อง) | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized (ไม่ได้รับอนุญาต) | โทเค็น JWT ไม่ถูกต้องหรือขาดหาย                  |
| 413  | Payload Too Large (ข้อมูลหนักเกินไป) | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัดที่กำหนด         |
| 500  | Internal Server Error (ข้อผิดพลาดภายในเซิร์ฟเวอร์) | เกิดข้อผิดพลาดที่ไม่คาดคิดภายในเซิร์ฟเวอร์      |

## วิธีใช้ PostUpdateWorksheetCellStyle API ผ่าน SDK

### ข้อมูลจำเพาะของ PostUpdateWorksheetCellStyle API

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetCellStyle) นิยามอินเทอร์เฟซโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถโต้ตอบกับ REST ได้โดยตรงผ่านเว็บเบราว์เซอร์

คุณสามารถใช้เครื่องมือบรรทัดคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย โดยแทนที่ `<jwt token>` ด้วยโทเค็นการเข้าถึง OAuth 2.0 ที่ถูกต้องที่ได้รับจากจุดสิ้นสุดการตรวจสอบสิทธิ์ของ Aspose Cloud

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
-d '{ "BackgroundThemeColor": { "ColorType": "Text2", "Tint": 1 } }' \
-X POST \
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
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "None"
    },
    "Name": null,
    "CultureCustom": null,
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
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "BottomBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalDown" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalUp" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Horizontal" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "LeftBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "RightBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "TopBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Vertical" }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style",
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

### ใช้ SDK ของ Aspose.Cells Cloud

การใช้ SDK เป็นวิธีที่เร็วที่สุดในการพัฒนาแอปพลิเคชันที่เชื่อมต่อกับ API SDK จะช่วยซ่อนรายละเอียดระดับต่ำ ทำให้คุณสามารถมุ่งเน้นไปที่ตรรกะทางธุรกิจของคุณได้ โปรดตรวจสอบ [คลังข้อมูล GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**ดูเพิ่มเติม:**  
- [Get Cell Style](https://docs.aspose.cloud/cells/get-cell-style/) – ดึงข้อมูลรูปแบบเซลล์ปัจจุบัน  
- [Update Multiple Cells Style](https://docs.aspose.cloud/cells/update-multiple-cells-style/) – ใช้รูปแบบให้กับช่วงของเซลล์ในคำขอกรายเดียว  
---