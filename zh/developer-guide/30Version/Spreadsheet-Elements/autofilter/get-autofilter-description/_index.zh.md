---
---
title: "获取自动筛选器"
description: "使用 Aspose.Cells Cloud REST API 从 Excel 工作表中检索自动筛选器描述。"
keywords: "自动筛选器, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
type: docs
url: /zh/cells/autofilter/get/
aliases:
  - /zh/get-autofilter-description/
weight: 50
---

# 从工作表中检索自动筛选器描述

**版本：** v3.0  
**端点：** `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter`

> **注意：** 所有示例请求均使用 **HTTPS**。请勿通过不安全的连接发送 JWT 令牌。

---

## 概述

**自动筛选器（AutoFilter）** 允许用户根据列值、颜色、自定义条件等对工作表中的行进行筛选。此 API 返回完整的自动筛选器配置，包括筛选列、范围和排序详情，以便您以编程方式检查或复制筛选设置。

---

## 前提条件

| 要求 | 说明 |
|------|------|
| **身份验证** | 需要有效的 JWT 令牌。请参阅[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。 |
| **文件位置** | 工作簿必须存储在 Aspose Cloud 存储中（或已连接的外部存储中）。 |
| **支持的格式** | Aspose.Cells 支持的任何 Excel 格式（例如 `.xlsx`、`.xls`、`.xlsm`）。 |
| **SDK（可选）** | 如果您更倾向于使用 SDK，请安装相应的包（例如，.NET 使用 `dotnet add package Aspose.Cells-Cloud`）。 |

---

## 请求

### HTTP 请求

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter
```

### 路径参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `name` | string | **必需项。** 工作簿文件名（包含扩展名）。 |
| `sheetName` | string | **必需项。** 要从中检索自动筛选器的工作表名称。 |

### 查询参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `folder` | string | 工作簿所在存储中的文件夹路径。 |
| `storageName` | string | 要使用的存储名称。 |

### 安全性

API 使用 **基于 JWT 令牌的身份验证**。请在 `Authorization` 标头中包含令牌：

```http
Authorization: Bearer <your_jwt_token>
```

---

## 请求示例（cURL）

```bash
curl "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter?folder=MyFolder&storageName=MyStorage" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

---

## 响应

服务返回一个 JSON 对象，其中封装了 `AutoFilter` 模型。

### 成功响应模式

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

### 响应示例

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

**HTTP 状态码**

| 状态码 | 含义 | 说明 |
|--------|------|------|
| 200 | OK（成功） | 筛选器应用成功；响应包含操作详情。 |
| 400 | Bad Request（错误请求） | 缺少或无效的参数（例如，不支持的文件类型）。 |
| 401 | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413 | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。 |
| 500 | Internal Server Error（内部服务器错误） | 发生意外的服务器错误。 |

---

## SDK 示例

该操作在所有 Aspose.Cells Cloud SDK 中均可用。以下为可直接运行的代码片段。

| 语言 | 示例 |
|------|------|
| **C#** | <details><summary>显示代码</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new CellsApi();\nvar response = apiInstance.GetWorksheetAutoFilter("Book1.xlsx", "Sheet1", folder: "MyFolder", storageName: "MyStorage");\nConsole.WriteLine(response.AutoFilter);\n```</details> |
| **Java** | <details><summary>显示代码</summary>```java\nimport com.aspose.cells.cloud.api.CellsApi;\nimport com.aspose.cells.cloud.model.AutoFilterResponse;\n\nCellsApi api = new CellsApi();\nAutoFilterResponse resp = api.getWorksheetAutoFilter("Book1.xlsx", "Sheet1", "MyFolder", "MyStorage");\nSystem.out.println(resp.getAutoFilter());\n```</details> |
| **Python** | <details><summary>显示代码</summary>```python\nfrom asposecellscloud import CellsApi\n\napi = CellsApi()\nresp = api.get_worksheet_auto_filter(name='Book1.xlsx', sheet_name='Sheet1', folder='MyFolder', storage_name='MyStorage')\nprint(resp.auto_filter)\n```</details> |
| **Node.js** | <details><summary>显示代码</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi();\napi.getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', { folder: 'MyFolder', storageName: 'MyStorage' })\n  .then(resp => console.log(resp.autoFilter))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>显示代码</summary>```php\nuse Aspose\Cells\CellsApi;\nuse Aspose\Cells\Models\AutoFilterResponse;\n\n$api = new CellsApi();\n$response = $api->getWorksheetAutoFilter('Book1.xlsx', 'Sheet1', 'MyFolder', 'MyStorage');\nprint_r($response->getAutoFilter());\n```</details> |
| **Ruby** | <details><summary>显示代码</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new\nresp = api.get_worksheet_auto_filter('Book1.xlsx', 'Sheet1', folder: 'MyFolder', storage_name: 'MyStorage')\nputs resp.auto_filter\n```</details> |
| **Go** | <details><summary>显示代码</summary>```go\nimport (\n    \"fmt\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\napi := asposecellscloud.NewAPIClient()\nresp, _, err := api.CellsApi.GetWorksheetAutoFilter(context.Background(), \"Book1.xlsx\", \"Sheet1\", \"MyFolder\", \"MyStorage\")\nif err != nil { panic(err) }\nfmt.Println(resp.AutoFilter)\n```</details> |
| **Perl** | <details><summary>显示代码</summary>```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new();\nmy $resp = $api->get_worksheet_auto_filter(name=>'Book1.xlsx', sheet_name=>'Sheet1', folder=>'MyFolder', storage_name=>'MyStorage');\nprint $resp->{autoFilter};\n```</details> |

有关 SDK 的完整列表和安装说明，请访问 [Aspose.Cells Cloud GitHub 仓库](https://github.com/aspose-cells-cloud)。

---

## 另请参阅

- [自动筛选器 – OpenAPI 规范](https://apireference.aspose.cloud/cells/#/AutoFilter/GetWorksheetAutoFilter)  
- [身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [存储操作](https://docs.aspose.cloud/cells/storage/)  

---
---