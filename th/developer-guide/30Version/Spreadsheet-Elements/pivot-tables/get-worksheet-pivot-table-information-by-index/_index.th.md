---
title: "รับข้อมูลตารางไข่ข้าว (Pivot Table) ในแผ่นงาน Excel"
second_title: "เอกสาร"
linktype: "Get"
type: docs
url: "/pivot-tables/get/"
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells, pivot table, Excel, REST API, รับข้อมูลตารางไข่ข้าวในแผ่นงาน"
description: "ดึงข้อมูลตารางไข่ข้าวจากแผ่นงาน Excel ผ่าน Aspose.Cells Cloud REST API รวมถึงไคลเอนต์คำสั่งร้องขอ พารามิเตอร์ การยืนยันตัวตน โครงสร้างคำตอบ การจัดการข้อผิดพลาด และตัวอย่าง SDK"
weight: 10
ArticleTitle: "รับข้อมูลตารางไข่ข้าว (Pivot Table) ในแผ่นงาน Excel"
---

API นี้ของ REST ใช้ดึงข้อมูล **ตารางไข่ข้าว (pivot table)** จากแผ่นงานโดยใช้ดัชนีของตารางไข่ข้าวนั้น

### **ความปลอดภัยและการยืนยันตัวตน**

API ของ Aspose.Cells Cloud มีความปลอดภัยและจำเป็นต้องใช้ <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">การยืนยันตัวตนแบบ JWT token</a>

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### พารามิเตอร์คำร้องขอ

| ชื่อพารามิเตอร์    | ชนิดข้อมูล | ตำแหน่ง | คำอธิบาย                                           |
| ------------------- | ---------- | -------- | --------------------------------------------------- |
| **name**            | string     | path     | ชื่อไฟล์ Excel                                     |
| **sheetName**       | string     | path     | ชื่อแผ่นงานที่มีตารางไข่ข้าว                      |
| **pivottableIndex** | integer    | path     | ดัชนีของตารางไข่ข้าวในแผ่นงาน (เริ่มต้นที่ 0)     |
| **folder**          | string     | query    | โฟลเดอร์ที่จัดเก็บเอกสารไว้                       |
| **storageName**     | string     | query    | ชื่อของพื้นที่จัดเก็บข้อมูลบน Aspose Cloud       |

คุณสามารถใช้เครื่องมือคำสั่ง **cURL** เพื่อเข้าถึงบริการเว็บของ Aspose.Cells ได้อย่างง่ายดาย ตัวอย่างต่อไปนี้แสดงวิธีเรียกใช้ API ด้วย cURL

{{< tabs tabTotal="2" tabID="1" tabName1="คำร้องขอ" tabName2="คำตอบ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**โครงสร้างคำตอบ**

| ฟิลด์          | ชนิดข้อมูล | คำอธิบาย                                         |
|----------------|------------|--------------------------------------------------|
| Status         | string     | ข้อความสถานะของการดำเนินการ (เช่น “OK”)        |
| PivotFilters   | array      | ชุดนิยามของตัวกรองตารางไข่ข้าว                 |
| └─ AutoFilter  | object     | รายละเอียดของการกรองอัตโนมัติที่ใช้กับตารางไข่ข้าว |
|    └─ link     | object     | ข้อมูลลิงก์สำหรับตัวกรอง                       |
|    └─ FilterColumns | array | การตั้งค่าตัวกรองสำหรับแต่ละคอลัมน์          |
|    └─ Range    | string     | ช่วงเซลล์ที่ใช้ตัวกรอง                         |
|    └─ Sorter   | object     | การตั้งค่าการเรียงลำดับข้อมูลที่กรองแล้ว       |
| (ฟิลด์ย่อยเพิ่มเติมมีโครงสร้างตามตัวอย่าง JSON ที่แสดงไว้) |

{{< /tab >}}

{{< /tabs >}}

### การจัดการข้อผิดพลาด

API นี้ใช้รหัสสถานะ HTTP มาตรฐาน ซึ่งผลลัพธ์ที่พบบ่อยมีดังนี้:

| รหัสสถานะ | ความหมาย                                                         | ตัวอย่าง JSON (ข้อผิดพลาด)                        |
|-----------|-------------------------------------------------------------------|---------------------------------------------------|
| 200       | สำเร็จ – ตารางไข่ข้าวถูกส่งกลับมา                               | —                                                 |
| 401       | ไม่ได้รับอนุญาต – token ไม่ถูกต้องหรือขาดหาย                   | `{"code":401,"message":"Invalid access token."}`  |
| 404       | ไม่พบ – ไฟล์ แผ่นงาน หรือดัชนีตารางไข่ข้าวไม่มีอยู่จริง         | `{"code":404,"message":"Pivot table not found."}` |
| 500       | ข้อผิดพลาดของเซิร์ฟเวอร์ – เงื่อนไขที่ไม่คาดคิด                   | `{"code":500,"message":"Internal server error."}` |

**หมายเหตุ:** API นี้รองรับไฟล์ Excel ขนาดสูงสุด 150 MB และรองรับรูปแบบ Excel 2007–2021 โปรดตรวจสอบให้แน่ใจว่าชื่อแผ่นงานต้องระบุตัวพิมพ์เล็ก/ใหญ่ให้ถูกต้อง

## ชุด SDK สำหรับ Cloud

การใช้ SDK เป็นวิธีที่ดีที่สุดในการเร่งกระบวนการพัฒนา โดย SDK จะจัดการรายละเอียดระดับต่ำให้คุณสามารถมุ่งเน้นไปที่งานในโครงการของคุณได้ โปรดดูที่ [ที่เก็บ GitHub](https://github.com/aspose-cells-cloud) เพื่อดูรายชื่อ SDK ทั้งหมดของ Aspose.Cells Cloud

ตัวอย่างโค้ดต่อไปนี้แสดงวิธีการเรียกใช้บริการเว็บของ Aspose.Cells โดยใช้ SDK ต่างๆ:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}