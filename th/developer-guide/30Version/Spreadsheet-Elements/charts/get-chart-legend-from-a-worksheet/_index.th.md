---
title: "รับข้อมูลคำอธิบายแผนภูมิจากแผ่นงาน"
type: docs
url: /th/charts/legend/get/
aliases: [  /th/get-chart-legend-from-a-worksheet/ ]
weight: 80
keywords: "Aspose.Cells, คำอธิบายแผนภูมิ, REST API, Excel, SDK บนคลาวด์, รับข้อมูลคำอธิบายแผนภูมิ, แผ่นงาน, สเปรดชีต"
description: "ดึงข้อมูลคำอธิบายของแผนภูมิที่อยู่ในแผ่นงานของไฟล์สมุดงาน Excel โดยใช้ Aspose.Cells Cloud REST API (เวอร์ชัน 3.0) ประกอบด้วย endpoint, พารามิเตอร์, ตัวอย่าง cURL และโค้ดตัวอย่าง SDK"
---

การดำเนินการ **Get Chart Legend** จะส่งคืนข้อมูลคำอธิบายของแผนภูมิที่อยู่ในแผ่นงานของไฟล์สมุดงาน Excel จุดปลาย (endpoint) นี้เป็นส่วนหนึ่งของ **Aspose.Cells Cloud API เวอร์ชัน 3.0** และสามารถใช้เมื่อคุณต้องการอ่านคุณสมบัติของคำอธิบาย เช่น ตำแหน่ง แบบอักษร ขนาด และการจัดรูปแบบ

## **API ของ REST**

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### ความปลอดภัยและการยืนยันตัวตน

API ของ Aspose.Cells Cloud มีความปลอดภัยและต้องใช้การยืนยันตัวตนแบบ [โทเคน JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

### พารามิเตอร์ของคำขอ

| ชื่อพารามิเตอร์ | ประเภท    | ตำแหน่ง | คำอธิบาย                                         |
| ---------------- | -------- | -------- | ------------------------------------------------ |
| name             | string   | path     | ชื่อไฟล์สมุดงาน                                  |
| sheetName        | string   | path     | ชื่อแผ่นงาน                                      |
| chartIndex       | integer  | path     | ดัชนีของแผนภูมิ (เริ่มต้นที่ 0)                  |
| folder           | string   | query    | เส้นทางโฟลเดอร์ที่เก็บสมุดงาน                   |
| storageName      | string   | query    | ชื่อของพื้นที่จัดเก็บ (storage)                 |

### **คำตอบ**

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 0,
  "Status": "0"
}
```

**รหัสสถานะ HTTP**

| รหัส | ความหมาย                     | คำอธิบาย                                                                 |
|------|-------------------------------|--------------------------------------------------------------------------|
| 200  | OK                            | ใช้ตัวกรองเรียบร้อยแล้ว; คำตอบประกอบด้วยรายละเอียดของการดำเนินการ   |
| 400  | Bad Request                   | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น ไฟล์ที่ไม่รองรับ)                |
| 401  | Unauthorized                  | โทเคน JWT ไม่ถูกต้องหรือขาดหาย                                          |
| 413  | Payload Too Large             | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด                                       |
| 500  | Internal Server Error         | เกิดข้อผิดพลาดที่ไม่คาดคิดบนเซิร์ฟเวอร์                                |

## วิธีใช้ API GetWorksheetChartLegend ร่วมกับ SDK

### ข้อมูลจำเพาะ API GetWorksheetChartLegend

[ข้อมูลจำเพาะ OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartLegend) นิยามอินเทอร์เฟซการเขียนโปรแกรมที่สามารถเข้าถึงได้แบบสาธารณะ และช่วยให้คุณสามารถเรียกใช้การโต้ตอบ REST ผ่านเบราว์เซอร์ได้โดยตรง

คุณสามารถใช้เครื่องมือ cURL ผ่านคำสั่งใน command-line เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีการเรียกใช้ Cloud API ด้วย cURL

{{< tabs tabTotal="2" tabID="11" tabName11="คำขอ" tabName12="คำตอบ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Legend": {
    "Position": "Right",
    "LegendEntries": {
      "link": {
        "Href": "/legendEntries",
        "Rel": "self",
        "Title": null,
        "Type": null
      }
    },
    "Area": {
      "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "FillFormat": {
        "Type": "Automatic",
        "SolidFill": null,
        "PatternFill": null,
        "TextureFill": null,
        "GradientFill": null,
        "ImageData": null
      },
      "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "Formatting": "Automatic",
      "InvertIfNegative": false,
      "Transparency": 0.0
    },
    "AutoScaleFont": true,
    "BackgroundMode": "Automatic",
    "Border": {
      "BeginArrowLength": "Medium",
      "BeginArrowWidth": "Medium",
      "BeginType": "None",
      "CapType": "Flat",
      "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
      "CompoundType": "Single",
      "DashType": "Solid",
      "EndArrowLength": "Medium",
      "EndArrowWidth": "Medium",
      "EndType": "None",
      "GradientFill": null,
      "IsAuto": true,
      "IsAutomaticColor": true,
      "IsVisible": true,
      "JoinType": "Round",
      "Style": "Solid",
      "Transparency": 0.0,
      "Weight": "HairLine",
      "WeightPt": 0.0
    },
    "Font": {
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 10.0,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Arial",
      "Size": 10,
      "Underline": "None"
    },
    "IsAutomaticSize": true,
    "IsInnerMode": null,
    "Shadow": false,
    "ShapeProperties": null,
    "Width": 823,
    "Height": 1043,
    "X": 3125,
    "Y": 1466,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend",
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

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา SDK จะจัดการรายละเอียดระดับต่ำให้คุณ และช่วยให้คุณสามารถมุ่งเน้นไปที่งานหลักของโปรเจกต์ได้ โปรดตรวจสอบ [repository บน GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ของ Aspose.Cells Cloud ทั้งหมด

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells ด้วย SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartLegendFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartLegend-get-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "76b8d73d934c0f03675299687805040f" >}}

{{< /tab >}}

{{< /tabs >}}