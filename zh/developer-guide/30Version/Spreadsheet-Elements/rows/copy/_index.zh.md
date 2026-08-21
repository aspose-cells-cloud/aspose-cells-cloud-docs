---
title: "复制 Excel 工作表中的行"
description: "使用 Aspose.Cells Cloud REST API (v3.0) 复制 Excel 工作表中特定整行的数据和格式。包含身份验证、请求/响应详情、错误处理及 SDK 示例。"
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# 复制 Excel 工作表中的行 <span style="float:right;">v3.0</span>

复制工作表中特定整行的数据和格式。

---

## 前置条件

| # | 要求 |
|---|------|
| 1 | 有效的 **JWT** 令牌。请参阅[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。 |
| 2 | 工作簿 (`{name}`) 必须已存在于指定的 **文件夹** / **存储** 中。 |
| 3 | 目标工作表 (`{sheetName}`) 必须存在于该工作簿中。 |
| 4 | （可选）若文件不在默认位置，请确认 **文件夹** 和 **storageName**。 |

---

## 接口端点

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*所有路径参数均区分大小写。*

### 路径参数

| 参数 | 类型 | 必填 | 描述 |
|------|------|------|------|
| `name` | string | ✅ | 工作簿文件名（例如 `test.xlsx`）。 |
| `sheetName` | string | ✅ | 工作表名称（例如 `Sheet1`）。 |

### 查询参数

| 参数 | 类型 | 必填 | 描述 |
|------|------|------|------|
| `sourceRowIndex` | integer | ✅ | 源行的从零开始的索引。 |
| `destinationRowIndex` | integer | ✅ | 目标行的从零开始的索引（即复制到的位置）。 |
| `rowNumber` | integer | ✅ | 要复制的行数。 |
| `worksheet` | string | ❌ | 工作表标识符；通常与 **sheetName** 相同。 |
| `folder` | string | ❌ | 包含工作簿的文件夹路径。 |
| `storageName` | string | ❌ | 存储服务的名称。 |

---

## 请求示例（cURL）

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **注意**  
> 请将 `<jwt token>` 替换为从身份验证服务获取的有效 JWT 令牌。

---

## 成功响应

| 状态码 | 描述 |
|--------|------|
| **200** | 行复制成功。 |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

响应体为 `CellsCloudResponse` 类型的实例。

---

## 错误处理

| HTTP 状态码 | 含义 | 示例响应体 |
|-------------|------|------------|
| **400** | 请求错误 — 缺少或无效的参数。 | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401** | 未授权 — 无效或缺失 JWT 令牌。 | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404** | 未找到 — 工作簿或工作表不存在。 | `{ "Code": 404, "Message": "File not found." }` |
| **500** | 服务器内部错误 — 意外的服务器状态。 | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**错误处理建议**

* **400** — 检查所有必需的查询参数是否齐全且格式正确。  
* **401** — 重新生成或刷新 JWT 令牌。  
* **404** — 确认工作簿和工作表名称正确，并验证文件是否存在于指定的文件夹/存储中。  
* **500** — 稍后重试；若问题持续存在，请联系 Aspose 支持团队。  

---

## SDK 示例

以下代码片段展示了如何使用官方 Aspose.Cells Cloud SDK 调用 **复制行（Copy Rows）** 操作。

| 语言 | 示例 |
|------|------|
| **C#** | <details><summary>显示代码</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi("clientId", "clientSecret");\nawait api.PostCopyWorksheetRowsAsync(name: "test.xlsx", sheetName: "Sheet1", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>显示代码</summary>```java\nCellsApi api = new CellsApi("clientId", "clientSecret");\napi.postCopyWorksheetRows("test.xlsx", "Sheet1", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>显示代码</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>显示代码</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>显示代码</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>显示代码</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>显示代码</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>显示代码</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*完整源代码文件可在 [Aspose‑Cells‑Cloud GitHub 仓库](https://github.com/aspose-cells-cloud) 中获取。*

---

## 参考阅读

- [在 Excel 工作表中插入行](/rows/add/)  
- [在 Excel 工作表中删除行](/rows/delete/)  
- [在 Excel 工作表中更新行](/rows/update/)  

--- 

*页面生成时间：**{{DATE}}**。如需查看该 API 的最新版本，请参考 [OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows)。*