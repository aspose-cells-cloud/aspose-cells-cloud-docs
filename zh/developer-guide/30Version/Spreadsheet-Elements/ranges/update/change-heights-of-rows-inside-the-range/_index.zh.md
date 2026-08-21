---
title: "在 Excel 中为指定范围设置行高 – Aspose.Cells Cloud API（v3.0）"
description: "使用 Aspose.Cells Cloud REST API 修改 Excel 工作表中特定范围内的行高。包含端点、参数、cURL 示例、响应示例以及多种编程语言的 SDK 代码片段。"
keywords: "Aspose.Cells, 行高, 范围, Excel, REST API, v3.0, SDK, cURL"
date: 2026-07-30
type: docs
weight: 76
aliases:
  - /change-heights-of-rows-inside-the-range/
---

# 在 Excel 中为指定范围设置行高

此操作用于更新存储于 Aspose Cloud 存储中的工作表上指定范围的行高。

## 前提条件 / 身份验证

您必须从 Aspose Cloud OAuth 服务获取一个带有 **Cells.ReadWrite** 作用域的 JWT 访问令牌。

在每个请求的 `Authorization` 请求头中包含该令牌：

```http
Authorization: Bearer <jwt token>
```

若您尚未获取令牌，请参考 **Aspose Cloud 身份验证指南** 申请一个。

## HTTP 请求

| 方法 | URI |
|------|-----|
| **POST** | `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight` |

### 路径参数

| 名称 | 类型 | 描述 |
|------|------|------|
| `name` | `string` | **必填。** 存储在云端的 Excel 文件名。 |
| `sheetName` | `string` | **必填。** 包含目标范围的工作表名称。 |

### 查询参数

| 名称 | 类型 | 是否必填 | 描述 |
|------|------|----------|------|
| `value` | `number` | **是** | 要应用于该范围的期望行高（单位：磅）。 |
| `folder` | `string` | 否 | 文件所在存储中的文件夹路径。 |
| `storageName` | `string` | 否 | 存储服务的名称（当配置了多个存储时）。 |

### 请求体（JSON）

请求体必须包含一个 **Range** 对象，用于定义受影响的行。

```json
{
  "FirstRow": 0,
  "RowCount": 1,
  "FirstColumn": 0,
  "ColumnCount": 0
}
```

#### Range JSON Schema（JSON 模式）

| 属性 | 类型 | 是否必填 | 描述 |
|------|------|----------|------|
| `FirstRow` | integer | **是** | 范围内第一行的零基索引。 |
| `RowCount` | integer | **是** | 要应用行高的行数。 |
| `FirstColumn` | integer | 否 | 范围内第一列的零基索引（仅用于行高操作时可选）。 |
| `ColumnCount` | integer | 否 | 范围所覆盖的列数（可选）。 |

仅上述属性用于行高操作；任何额外字段均会被忽略。

## 示例请求

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15&folder=Documents&storageName=MyStorage" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "RowCount": 1
      }'
```

### 示例响应（成功）

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP 状态码说明**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 行高已成功应用；响应包含操作详情。 |
| 400 | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。 |
| 401 | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413 | Payload Too Large（请求体过大） | 上传文件超过大小限制。 |
| 500 | Internal Server Error（服务器内部错误） | 发生意外服务器错误。 |

所有响应均包含数值型 `Code` 字段及可读的 `Status`（错误时可能为 `Message`）。发生错误时，可能还会返回额外的 `ErrorDetails` 字段。

## SDK 示例

以下代码片段展示了如何使用官方 Aspose.Cells Cloud SDK 调用 **为指定范围设置行高** 接口。

| 语言 | 示例 |
|------|------|
| **C#** | <details><summary>显示代码</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new RangesApi(configuration);\nvar range = new Range { FirstRow = 9, RowCount = 1 };\nawait api.PostWorksheetCellsRangeRowHeightAsync("test.xlsx", "Sheet1", range, 15);\n```</details> |
| **Java** | <details><summary>显示代码</summary>```java\nimport com.aspose.cloud.cells.api.RangesApi;\nimport com.aspose.cloud.cells.model.Range;\n\nRangesApi api = new RangesApi(config);\nRange range = new Range().firstRow(9).rowCount(1);\napi.postWorksheetCellsRangeRowHeight("test.xlsx", "Sheet1", range, 15.0, null, null);\n```</details> |
| **Python** | <details><summary>显示代码</summary>```python\nfrom asposecellscloud import RangesApi, ApiClient, Configuration\n\nconfig = Configuration()\nconfig.access_token = '<jwt token>'\napi = RangesApi(ApiClient(config))\nrange = {'FirstRow': 9, 'RowCount': 1}\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value=15)\n```</details> |
| **Node.js** | <details><summary>显示代码</summary>```javascript\nconst { RangesApi, Configuration } = require('asposecellscloud');\nconst config = new Configuration();\nconfig.accessToken = '<jwt token>';\nconst api = new RangesApi(config);\nconst range = { FirstRow: 9, RowCount: 1 };\napi.postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', range, 15)\n  .then(() => console.log('Row height set'))\n  .catch(err => console.error(err));\n```</details> |
| **PHP** | <details><summary>显示代码</summary>```php\nuse Aspose\Cells\Configuration;\nuse Aspose\Cells\Api\RangesApi;\n\n$config = new Configuration();\n$config->setAccessToken('<jwt token>');\n$api = new RangesApi($config);\n$range = ['FirstRow' => 9, 'RowCount' => 1];\n$api->postWorksheetCellsRangeRowHeight('test.xlsx', 'Sheet1', $range, 15);\n```</details> |
| **Ruby** | <details><summary>显示代码</summary>```ruby\nrequire 'aspose_cells_cloud'\nconfig = AsposeCellsCloud::Configuration.new\nconfig.access_token = '<jwt token>'\napi = AsposeCellsCloud::RangesApi.new\nrange = { 'FirstRow' => 9, 'RowCount' => 1 }\napi.post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', range, value: 15)\n```</details> |
| **Go** | <details><summary>显示代码</summary>```go\nimport (\n    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"\n    "context"\n)\n\ncfg := asposecellscloud.NewConfiguration()\ncfg.AccessToken = "<jwt token>"\napi := asposecellscloud.NewRangesApi(cfg)\nrangeBody := map[string]interface{}{ "FirstRow": 9, "RowCount": 1 }\n_, err := api.PostWorksheetCellsRangeRowHeight(context.Background(), "test.xlsx", "Sheet1", rangeBody, 15, nil, nil)\nif err != nil { panic(err) }\n```</details> |
| **Perl** | <details><summary>显示代码</summary>```perl\nuse AsposeCellsCloud::Api::RangesApi;\nmy $api = AsposeCellsCloud::Api::RangesApi->new({ access_token => '<jwt token>' });\nmy $range = { FirstRow => 9, RowCount => 1 };\n$api->post_worksheet_cells_range_row_height('test.xlsx', 'Sheet1', $range, 15);\n```</details> |

> **注意**：所有 SDK 在配置访问令牌后，将自动添加所需的 `Authorization: Bearer` 请求头。

## 参考链接

- **OpenAPI 规范** – 本接口的详细契约： <https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight>
- **Aspose.Cells Cloud SDK 代码仓库** – 源码及更多语言绑定： <https://github.com/aspose-cells-cloud>
- **身份验证指南** – 如何获取 JWT 令牌： <https://docs.aspose.cloud/cells/authentication/>