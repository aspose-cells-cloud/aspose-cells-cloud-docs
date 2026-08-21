---
---
title: "รับข้อมูล AutoFilter"
description: "ดึงคำอธิบาย AutoFilter จากแผ่นงาน Excel โดยใช้ Aspose.Cells Cloud REST API"
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# ดึงคำอธิบาย AutoFilter จากแผ่นงาน

**เวอร์ชัน:** v3.0  
**จุดปลายทาง (Endpoint):** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **หมายเหตุ:** คำขอตัวอย่างทั้งหมดใช้ **HTTPS** ห้ามส่ง JWT token ผ่านการเชื่อมต่อที่ไม่ปลอดภัยเด็ดขาด

---

## ภาพรวม

**AutoFilter** ช่วยให้ผู้ใช้สามารถกรองแถวในแผ่นงานตามค่าคอลัมน์ สี หรือเกณฑ์ที่กำหนดเองได้ API นี้จะส่งคืนค่าการตั้งค่า AutoFilter ทั้งหมด รวมถึงคอลัมน์ที่กรอง ช่วงข้อมูล และรายละเอียดการเรียงลำดับ เพื่อให้คุณสามารถตรวจสอบหรือทำซ้ำการตั้งค่าตัวกรองด้วยโปรแกรมได้

---

## ข้อกำหนดเบื้องต้น

| ข้อกำหนด | คำอธิบาย |
|----------|----------|
| **การยืนยันตัวตน (Authentication)** | ต้องมี JWT token ที่ถูกต้อง ดูเพิ่มเติมได้ที่[คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) |
| **ตำแหน่งไฟล์** | สมุดงานต้องถูกจัดเก็บไว้ใน Aspose Cloud Storage (หรือในพื้นที่จัดเก็บภายนอกที่เชื่อมต่อไว้) |
| **รูปแบบที่รองรับ** | รูปแบบ Excel ใดก็ได้ที่ Aspose.Cells รองรับ (เช่น `.xlsx`, `.xls`, `.xlsm`) |
| **SDK (ไม่บังคับ)** | หากต้องการใช้ SDK ให้ติดตั้งแพ็กเกจที่เหมาะสม (เช่น `dotnet add package Aspose.Cells-Cloud` สำหรับ .NET) |

---

## คำขอ

### HTTP Request

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### พารามิเตอร์ใน Path

| พารามิเตอร์ | ประเภท | คำอธิบาย |
|-------------|--------|----------|
| `name`      | string | **จำเป็น** ชื่อไฟล์สมุดงาน รวมส่วนขยายด้วย |
| `sheetName` | string | **จำเป็น** ชื่อแผ่นงานที่ต้องการดึงข้อมูล AutoFilter |

### พารามิเตอร์ใน Query

| พารามิเตอร์   | ประเภท | คำอธิบาย |
|---------------|--------|----------|
| `folder`      | string | ไดเรกทอรีในพื้นที่จัดเก็บที่อยู่ของสมุดงาน |
| `storageName` | string | ชื่อของพื้นที่จัดเก็บที่ต้องการใช้งาน |

### ความปลอดภัย

API ใช้ **การยืนยันตัวตนด้วย JWT token** ให้ใส่ token ไว้ใน header `Authorization`:

```http
Authorization: Bearer <your_jwt_token>
```

---

## ตัวอย่างคำขอ (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## การตอบกลับ

บริการจะส่งคืน JSON object ซึ่งห่อหุ้มโมเดล `AutoFilter`

### โครงสร้างการตอบกลับที่สำเร็จ

```json
{
  "Status": "OK",
  "Code": 200,
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
          "MultipleFilterList": [
            {}
          ]
        },
        "ColorFilter": {
          "FilterByFillColor": "string",
          "Pattern": "string",
          "Color": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "ForegroundColorColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          },
          "BackgroundColor": {
            "Color": { "A": 0, "R": 0, "G": 0, "B": 0 },
            "ColorIndex": 0,
            "IsShapeColor": true,
            "ThemeColor": { "ColorType": "string", "Tint": 0 },
            "Type": "string"
          }
        },
        "CustomFilters": [
          { "FilterOperatorType": "string" }
        ],
        "DynamicFilter": { "DynamicFilterType": "string" },
        "IconFilter": { "IconId": 0, "IconSetType": "string" },
        "Top10Filter": {
          "Criteria": "string",
          "IsPercent": true,
          "IsTop": true,
          "Items": 0
        },
        "Visibledropdown": "string"
      }
    ],
    "Range": "string",
    "Sorter": {
      "CaseSensitive": true,
      "HasHeaders": true,
      "KeyList": [
        { "Key": 0, "SortOrder": "string", "CustomList": "string" }
      ],
      "SortLeftToRight": true
    }
  }
}
```

### ตัวอย่างการตอบกลับ

```json
{
  "Status": "OK",
  "Code": 200,
  "AutoFilter": {
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter",
      "Rel": "self",
      "Title": "AutoFilter",
      "Type": "application/json"
    },
    "FilterColumns": [
      {
        "FieldIndex": 1,
        "FilterType": "Custom",
        "MultipleFilters": {
          "MatchBlank": false,
          "MultipleFilterList": [
            {
              "Operator": "Equals",
              "Criteria": "Approved"
            }
          ]
        },
        "ColorFilter": null,
        "CustomFilters": [],
        "DynamicFilter": null,
        "IconFilter": null,
        "Top10Filter": null,
        "Visibledropdown": "true"
      }
    ],
    "Range": "A1:C100",
    "Sorter": {
      "CaseSensitive": false,
      "HasHeaders": true,
      "KeyList": [
        {
          "Key": 1,
          "SortOrder": "Ascending",
          "CustomList": null
        }
      ],
      "SortLeftToRight": false
    }
  }
}
```

---

**โค้ดสถานะ HTTP**

| โค้ด | ความหมาย                  | คำอธิบาย |
|------|---------------------------|---------|
| 200  | OK                        | ใช้การกรองสำเร็จ; การตอบกลับมีรายละเอียดของการดำเนินการ |
| 400  | Bad Request               | พารามิเตอร์ขาดหายหรือไม่ถูกต้อง (เช่น รูปแบบไฟล์ที่ไม่รองรับ) |
| 401  | Unauthorized              | JWT token ไม่ถูกต้องหรือขาดหาย |
| 413  | Payload Too Large         | ไฟล์ที่อัปโหลดมีขนาดเกินขีดจำกัด |
| 500  | Internal Server Error     | เกิดข้อผิดพลาดภายในเซิร์ฟเวอร์ที่ไม่คาดคิด |

---

## ตัวอย่าง SDK

การดำเนินการนี้มีให้ใช้งานใน SDK ของ Aspose.Cells Cloud ทุกตัว ด้านล่างนี้คือตัวอย่างโค้ดที่พร้อมรัน

| ภาษา | ตัวอย่าง |
|------|---------|
| **C#** | <details><summary>แสดงโค้ด</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>แสดงโค้ด</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>แสดงโค้ด</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>แสดงโค้ด</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>แสดงโค้ด</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>แสดงโค้ด</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>แสดงโค้ด</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>แสดงโค้ด</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

สำหรับรายชื่อ SDK ทั้งหมดและคำแนะนำในการติดตั้ง โปรดเยี่ยมชม [ที่เก็บ GitHub ของ Aspose.Cells Cloud](https://github.com/aspose-cells-cloud)

---

## ดูเพิ่มเติม

- [AutoFilter – OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [คู่มือการยืนยันตัวตน](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [การดำเนินการกับพื้นที่จัดเก็บ](https://docs.aspose.cloud/cells/storage/)  

---
---