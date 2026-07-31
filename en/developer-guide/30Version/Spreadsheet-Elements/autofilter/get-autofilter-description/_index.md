---
title: "Get AutoFilter"
description: "Retrieve the AutoFilter description from an Excel worksheet using Aspose.Cells Cloud REST API."
keywords: "AutoFilter, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /cells/autofilter/get/
aliases:
  - /get-autofilter-description/
weight: 50
---

# Retrieve AutoFilter Description from a Worksheet

**Version:** v3.0  
**Endpoint:** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **Note:** All sample requests use **HTTPS**. Never send JWT tokens over an insecure connection.

---

## Overview

An **AutoFilter** allows users to filter rows in a worksheet based on column values, colors, custom criteria, and more. This API returns the full AutoFilter configuration—including filter columns, range, and sorting details—so you can inspect or replicate the filter settings programmatically.

---

## Prerequisites

| Requirement | Description |
|-------------|-------------|
| **Authentication** | A valid JWT token is required. See the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **File location** | The workbook must be stored in Aspose Cloud Storage (or a connected external storage). |
| **Supported formats** | Any Excel format supported by Aspose.Cells (e.g., `.xlsx`, `.xls`, `.xlsm`). |
| **SDK (optional)** | If you prefer using an SDK, install the appropriate package (e.g., `dotnet add package Aspose.Cells-Cloud` for .NET). |

---

## Request

### HTTP Request

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### Path Parameters

| Parameter | Type   | Description |
|-----------|--------|-------------|
| `name`      | string | **Required.** Workbook file name, including extension. |
| `sheetName` | string | **Required.** Worksheet name from which to retrieve the AutoFilter. |

### Query Parameters

| Parameter   | Type   | Description |
|-------------|--------|-------------|
| `folder`      | string | Folder path in storage where the workbook is located. |
| `storageName` | string | Name of the storage to use. |

### Security

The API uses **JWT token‑based authentication**. Include the token in the `Authorization` header:

```http
Authorization: Bearer <your_jwt_token>
```

---

## Request Example (cURL)

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## Response

The service returns a JSON object that wraps the `AutoFilter` model.

### Successful Response Schema

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

### Response Example

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

## HTTP Status Codes

| Code | Meaning | Description |
|------|---------|-------------|
| **200** | OK | AutoFilter retrieved successfully. |
| **400** | Bad Request | Missing or invalid parameters (e.g., unsupported file type). |
| **401** | Unauthorized | Invalid or missing JWT token. |
| **413** | Payload Too Large | Uploaded file exceeds the allowed size limit. |
| **500** | Internal Server Error | Unexpected server error. |

---

## SDK Examples

The operation is available in all Aspose.Cells Cloud SDKs. Below are ready‑to‑run snippets.

| Language | Example |
|----------|---------|
| **C#** | <details><summary>Show code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter(\"Book1.xlsx\", \"Sheet1\", folder: \"MyFolder\", storageName: \"MyStorage\");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>Show code</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter(\"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>Show code</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>Show code</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>Show code</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>Show code</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>Show code</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>Show code</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

For a complete list of SDKs and installation instructions, visit the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).

---

## See Also

- [AutoFilter – OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Storage operations](https://docs.aspose.cloud/cells/storage/)  

---