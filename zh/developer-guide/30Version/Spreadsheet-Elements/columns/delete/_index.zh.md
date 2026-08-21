---
title: "使用 Aspose.Cells Cloud API 删除 Excel 工作表中的列"
description: "了解如何通过 Aspose.Cells Cloud REST API 删除 Excel 工作表中的一列或多列。内容包括身份验证、请求语法、参数、响应、错误处理及 SDK 示例。"
keywords: ["Aspose.Cells", "删除列", "Excel API", "REST", "云", "工作表", "列"]
date: 2026-07-30
api_version: "v3.0"
---

# 使用 Excel 工作表删除列

**端点**：`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`  

该操作可从工作表中删除单列或多列。删除后，单元格引用（包括公式）可自动更新。

---

## 目录
1. [前提条件](#前提条件)  
2. [身份验证](#身份验证)  
3. [请求 URL 与 HTTP 方法](#请求-url-与-http-方法)  
4. [参数](#参数)  
   - [路径参数](#路径参数)  
   - [查询参数](#查询参数)  
5. [cURL 示例](#curl-示例)  
6. [响应](#响应)  
7. [错误代码](#错误代码)  
8. [SDK 示例](#sdk-示例)  
9. [附加说明](#附加说明)  

---

## 前提条件
- 通过 Aspose Cloud 身份验证流程获取的有效 **JWT 访问令牌**。  
- 工作簿 (`{name}`) 必须已上传至 Aspose Cloud 存储空间（或可通过 `folder`/`storageName` 查询参数访问）。  

---

## 身份验证
所有 Aspose.Cells Cloud 请求均需 **Bearer token** 身份验证。

```http
Authorization: Bearer <access_token>
```

有关获取 JWT 令牌的详细信息，请参阅[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

---

## 请求 URL 与 HTTP 方法
```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **`{name}`** – 工作簿文件名（例如 `test.xlsx`）。  
- **`{sheetName}`** – 工作表名称（例如 `Sheet1`）。  
- **`{columnIndex}`** – 要删除的第一列的从零开始的索引。  

---

## 参数

| 名称                | 位置 | 类型     | 必填 | 描述 |
|--------------------|------|----------|------|------|
| **name**           | path | string   | ✅ 是 | 工作簿文件名。 |
| **sheetName**      | path | string   | ✅ 是 | 工作表名称。 |
| **columnIndex**    | path | integer  | ✅ 是 | 要删除的第一列的从零开始的索引。 |
| **startColumn**    | query | integer | ❌ 否 | 删除操作的起始列索引（从零开始）。若省略，则默认为 `columnIndex`。 |
| **totalColumns**   | query | integer | ❌ 否 | 要删除的列数。若省略，则仅删除由 `columnIndex` 指定的单列。 |
| **updateReference** | query | boolean | ❌ 否 | 若为 `true`，删除后将自动更新整个工作簿中的单元格引用（包括公式）。 |
| **folder**         | query | string  | ❌ 否 | 包含该工作簿的文件夹路径。 |
| **storageName**    | query | string  | ❌ 否 | Aspose Cloud 存储服务的名称。 |

> **说明**：低层 API 规范中所示的 `columns` 参数已被更具表达力的 `startColumn` 与 `totalColumns` 查询参数取代。为保持向后兼容性，两种方式均被支持。

---

## cURL 示例

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=1&updateReference=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

### 说明
- 从 `test.xlsx` 的 `Sheet1` 中删除 **B 列**（`columnIndex = 1`）。  
- `startColumn=1` 和 `totalColumns=1` 指定仅删除一列。  
- `updateReference=true` 确保公式及其他引用被自动调整。

---

## 响应

| HTTP 状态码 | 描述 | 示例 |
|------------|------|------|
| **200** | 成功 – 列已被删除。 | `{ "Code": 200, "Status": "OK" }` |
| **400** | 错误请求 – 缺少或无效的参数。 | `{ "Code": 400, "Message": "无效的 totalColumns 值。" }` |
| **401** | 未授权 – 缺少或无效的 JWT 令牌。 | `{ "Code": 401, "Message": "身份验证失败。" }` |
| **404** | 未找到 – 工作簿或工作表不存在。 | `{ "Code": 404, "Message": "工作表 'Sheet1' 未找到。" }` |
| **500** | 服务器内部错误 – 服务器端发生意外情况。 | `{ "Code": 500, "Message": "发生意外错误。" }` |

响应体遵循通用的 **`CellsCloudResponse`** 模型。

---

**HTTP 状态码**

| 状态码 | 含义         | 描述                             |
|--------|--------------|----------------------------------|
| 200    | OK（成功）   | 筛选器应用成功；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（载荷过大） | 上传文件超出大小限制。 |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。 |
---

## SDK 示例

以下为最常用 SDK 的可直接运行代码片段。请将占位符（`<YOUR_ACCESS_TOKEN>`、`<WORKBOOK>` 等）替换为您的实际数据。

| 语言 | 示例 |
|------|------|
| **C#** | <details><summary>显示代码</summary> <br>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\nusing System;\n\nvar config = new Configuration { AccessToken = "<YOUR_ACCESS_TOKEN>", BaseUrl = "https://api.aspose.cloud" };\nvar api = new CellsApi(config);\n\nvar response = api.DeleteWorksheetColumns(name: "test.xlsx",\n                                         sheetName: "Sheet1",\n                                         columnIndex: 1,\n                                         startColumn: 1,\n                                         totalColumns: 1,\n                                         updateReference: true);\nConsole.WriteLine($"Status: {response.Status}");\n```</details> |
| **Java** | <details><summary>显示代码</summary> <br>```java\nimport com.aspose.cloud.cells.api.CellsApi;\nimport com.aspose.cloud.cells.model.CellsCloudResponse;\nimport com.aspose.cloud.cells.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_ACCESS_TOKEN>");\nconfig.setBaseUrl("https://api.aspose.cloud");\nCellsApi api = new CellsApi(config);\n\nCellsCloudResponse resp = api.deleteWorksheetColumns("test.xlsx", "Sheet1", 1, 1, 1, true, null, null);\nSystem.out.println("Status: " + resp.getStatus());\n```</details> |
| **Python** | <details><summary>显示代码</summary> <br>```python\nimport asposecellscloud\nfrom asposecellscloud.rest import ApiException\n\nconfig = asposecellscloud.Configuration()\nconfig.access_token = '<YOUR_ACCESS_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\napi_instance = asposecellscloud.CellsApi(asposecellscloud.ApiClient(config))\n\ntry:\n    resp = api_instance.delete_worksheet_columns(name='test.xlsx',\n                                                 sheet_name='Sheet1',\n                                                 column_index=1,\n                                                 start_column=1,\n                                                 total_columns=1,\n                                                 update_reference=True)\n    print('Status:', resp.status)\nexcept ApiException as e:\n    print('Exception when calling CellsApi->delete_worksheet_columns:', e)\n```</details> |
| **Node.js** | <details><summary>显示代码</summary> <br>```javascript\nconst { CellsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({\n    accessToken: '<YOUR_ACCESS_TOKEN>',\n    basePath: 'https://api.aspose.cloud'\n});\nlet api = new CellsApi(config);\n\napi.deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, {\n    startColumn: 1,\n    totalColumns: 1,\n    updateReference: true\n}).then(res => {\n    console.log('Status:', res.status);\n}).catch(err => {\n    console.error(err);\n});\n```</details> |
| **Go** | <details><summary>显示代码</summary> <br>```go\npackage main\n\nimport (\n    \"context\"\n    \"fmt\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_ACCESS_TOKEN>\"\n    cfg.BasePath = \"https://api.aspose.cloud\"\n    client := api.NewAPIClient(cfg)\n    resp, _, err := client.CellsApi.DeleteWorksheetColumns(context.Background(), \"test.xlsx\", \"Sheet1\", 1,\n        &api.DeleteWorksheetColumnsOpts{StartColumn: optional.NewInt32(1), TotalColumns: optional.NewInt32(1), UpdateReference: optional.NewBool(true)})\n    if err != nil {\n        fmt.Println(\"Error:\", err)\n        return\n    }\n    fmt.Println(\"Status:\", resp.Status)\n}\n```</details> |
| **Ruby** | <details><summary>显示代码</summary> <br>```ruby\nrequire 'aspose_cells_cloud'\n\nconfig = AsposeCellsCloud::Configuration.new do |c|\n  c.access_token = '<YOUR_ACCESS_TOKEN>'\n  c.host = 'https://api.aspose.cloud'\nend\napi = AsposeCellsCloud::CellsApi.new\n\nbegin\n  resp = api.delete_worksheet_columns('test.xlsx', 'Sheet1', 1,\n    start_column: 1,\n    total_columns: 1,\n    update_reference: true)\n  puts \"Status: #{resp.status}\"\nrescue AsposeCellsCloud::ApiError => e\n  puts \"Exception: #{e}\"\nend\n```</details> |
| **PHP** | <details><summary>显示代码</summary> <br>```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\\Cells\\Cloud\\Api\\CellsApi;\nuse Aspose\\Cells\\Cloud\\Configuration;\n\n$config = new Configuration();\n$config->setAccessToken('<YOUR_ACCESS_TOKEN>');\n$config->setHost('https://api.aspose.cloud');\n$apiInstance = new CellsApi($config);\n\ntry {\n    $result = $apiInstance->deleteWorksheetColumns('test.xlsx', 'Sheet1', 1, [\n        'startColumn' => 1,\n        'totalColumns' => 1,\n        'updateReference' => true\n    ]);\n    echo \"Status: \" . $result->getStatus();\n} catch (Exception $e) {\n    echo 'Exception when calling CellsApi->deleteWorksheetColumns: ', $e->getMessage();\n}\n?>\n```</details> |
| **Perl** | <details><summary>显示代码</summary> <br>```perl\n#!/usr/bin/perl\nuse strict;\nuse warnings;\nuse AsposeCellsCloud::Api::CellsApi;\nuse AsposeCellsCloud::Configuration;\n\nmy $config = AsposeCellsCloud::Configuration->new(\n    access_token => '<YOUR_ACCESS_TOKEN>',\n    host => 'https://api.aspose.cloud'\n);\nmy $api = AsposeCellsCloud::Api::CellsApi->new($config);\n\nmy $response = $api->delete_worksheet_columns(\n    name => 'test.xlsx',\n    sheet_name => 'Sheet1',\n    column_index => 1,\n    start_column => 1,\n    total_columns => 1,\n    update_reference => JSON::true\n);\nprint \"Status: \", $response->{Status}, \"\\n\";\n```</details> |

*所有 SDK 在配置 `access_token` 后将自动添加所需的 `Authorization` 请求头。*

---

## 附加说明

### 安全性请求头（生产环境推荐）
在提供文档页面时，建议添加以下 HTTP 响应头以增强安全性：

```
Content-Security-Policy: default-src 'self'; script-src 'self' https://www.googletagmanager.com https://menu-new.containerize.com; style-src 'self' 'unsafe-inline'; img-src 'self' data:;
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Referrer-Policy: strict-origin-when-cross-origin
```

### 性能优化建议
- 使用 `async` 属性加载第三方分析脚本（`gtag.js`、`containerize.js`），或在页面渲染完成后再加载。  
- 压缩自定义 JavaScript/CSS 捆包。  
- 若 SVG 图标为渲染阻塞资源，请预加载较小图标：

```html
<link rel="preload" href="/cells/icons/caret-down.svg" as="image" type="image/svg+xml">
```

### SEO 增强（JSON-LD）

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "使用 Aspose.Cells Cloud API 删除 Excel 工作表中的列",
  "description": "了解如何通过 Aspose.Cells Cloud REST API 删除 Excel 工作表中的一列或多列。",
  "author": { "@type": "Organization", "name": "Aspose" },
  "datePublished": "2023-01-01",
  "url": "https://docs.aspose.cloud/cells/columns/delete/",
  "keywords": ["Aspose.Cells", "删除列", "Excel", "REST API"]
}
```

将上述代码片段放入 HTML `<head>` 中的 `<script type="application/ld+json">` 区块。

### 可访问性
- 所有装饰性图像均使用 `alt=""`，或通过 `aria-hidden="true"` 隐藏。  
- Open Graph 图像的 `<meta>` 标签中已添加 `alt` 属性以完善可访问性支持。

---

## 参见
- [DeleteWorksheetColumns 的 OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns)  
- [身份验证概述](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [GitHub 上的 Aspose.Cells Cloud SDK](https://github.com/aspose-cells-cloud)  

---