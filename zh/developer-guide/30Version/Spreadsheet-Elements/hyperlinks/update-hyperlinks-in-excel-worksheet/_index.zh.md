---
title: "更新 Excel 工作表中的超链接 — Aspose.Cells Cloud API 指南"
description: "了解如何使用 Aspose.Cells Cloud REST API（v3.0）更新 Excel 工作表中的超链接。内容包括端点、参数、请求体结构、cURL 示例、SDK 代码片段、错误处理、限流策略及前置条件。"
keywords:
  - "Aspose.Cells"
  - "超链接更新"
  - "Excel API"
  - "REST API"
  - "云电子表格"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# 更新 Excel 工作表中的超链接  

**API 版本：** v3.0  

**PostWorksheetHyperlink** 操作用于更新指定索引的工作表中已存在的超链接（索引为从零开始的整数）。

---

## 目录
1. [前置条件](#prerequisites)  
2. [限流策略](#rate-limiting)  
3. [端点](#endpoint)  
4. [参数](#parameters)  
   - [路径参数](#path-parameters)  
   - [查询参数](#query-parameters)  
   - [请求体结构](#request-body-schema)  
5. [响应](#responses)  
   - [成功响应](#success-response)  
   - [错误响应](#error-responses)  
6. [cURL 示例](#curl-example)  
7. [SDK 代码片段](#sdk-code-samples)  
8. [参见](#see-also)  

---

## 前置条件 <a name="prerequisites"></a>

| 要求 | 说明 |
|------|------|
| **身份验证** | 基于 JWT 令牌的身份验证。获取令牌的方法请参阅[身份验证指南](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。 |
| **存储** | 工作簿必须存储于受支持的 Aspose Cloud 存储中（默认为 **Default**）。 |
| **权限** | JWT 令牌必须具备对目标工作簿的读写权限。 |
| **请求头** | 所有请求均需包含 `Content-Type: application/json` 和 `Accept: application/json`。 |

---

## 限流策略 <a name="rate-limiting"></a>

Aspose.Cells Cloud 对每个访问令牌施加**每分钟最多 60 次请求**的限制。超出限制时将返回 HTTP **429 Too Many Requests（请求过多）**。当发生限流时，请实现指数退避机制，或依据响应头中的 `Retry-After` 字段进行重试。

---

## 端点 <a name="endpoint"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*更新文件 `name` 中工作表 `sheetName` 内索引为 `hyperlinkIndex` 的超链接。*

---

## 参数 <a name="parameters"></a>

### 路径参数 <a name="path-parameters"></a>

| 名称 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `name` | 字符串 | ✅ | Excel 文件名称（包含扩展名）。 |
| `sheetName` | 字符串 | ✅ | 包含该超链接的工作表名称。 |
| `hyperlinkIndex` | 整数 | ✅ | 待更新超链接的从零开始索引。 |

### 查询参数 <a name="query-parameters"></a>

| 名称 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `folder` | 字符串 | ❌ | 工作簿所在存储中的文件夹路径。 |
| `storageName` | 字符串 | ❌ | 存储服务名称（例如 `Default`）。 |

### 请求体结构 <a name="request-body-schema"></a>

请求体必须包含一个 **`hyperlink`** 对象。仅需提供您希望修改的字段；未提供的可选字段将保留其原有值。

| 字段 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `Address` | 字符串 | ✅ | 超链接的目标 URL。 |
| `Area` | 对象 | ✅ | 超链接所在的单元格区域。必须包含 `StartRow`、`StartColumn`、`EndRow`、`EndColumn`（均为从零开始的整数）。 |
| `ScreenTip` | 字符串 | ❌ | 鼠标悬停时显示的工具提示。 |
| `TextToDisplay` | 字符串 | ❌ | 单元格中显示的文本。 |
| `link` | 对象 | ❌ | 超媒体链接（`Href`、`Rel`、`Title`、`Type`）。通常在请求负载中省略。 |

**`Area` 对象定义**

| 子字段 | 类型 | 必填 | 说明 |
|--------|------|------|------|
| `StartRow` | 整数 | ✅ | 从零开始的起始行索引。 |
| `StartColumn` | 整数 | ✅ | 从零开始的起始列索引。 |
| `EndRow` | 整数 | ✅ | 从零开始的结束行索引。 |
| `EndColumn` | 整数 | ✅ | 从零开始的结束列索引。 |

---

## 响应 <a name="responses"></a>

### 成功响应 <a name="success-response"></a>

| 字段 | 类型 | 说明 |
|------|------|------|
| `Code` | 整数 | HTTP 状态码（成功时为 200）。 |
| `Status` | 字符串 | 文本状态（成功时为 `OK`）。 |
| `Hyperlink` | 对象（可选） | 更新后的超链接对象；仅当请求中明确要求返回 `link` 子对象时才会包含。 |

**示例 JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### 错误响应 <a name="error-responses"></a>

| HTTP 状态码 | 原因 | 示例响应体 |
|-------------|------|-------------|
| **400** | 请求无效 — 参数缺失或格式错误。 | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | 未授权 — 缺失或无效的 JWT 令牌。 | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | 未找到 — 工作簿、工作表或超链接不存在。 | `{ "Code":"404", "Message":"File not found." }` |
| **429** | 请求过多 — 超出速率限制。 | `{ "Code":"429", "Message":"Request limit exceeded. Retry later." }` |
| **500** | 内部服务器错误 — 服务器意外失败。 | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## cURL 示例 <a name="curl-example"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**响应**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*提示：可将 JSON 负载保存为文件（如 `payload.json`），并通过 `--data @payload.json` 引用，以便更清晰地复制粘贴。*

---

## SDK 代码片段 <a name="sdk-code-samples"></a>

以下代码片段演示如何使用官方 Aspose.Cells Cloud SDK 调用 **PostWorksheetHyperlink** 接口。请将占位符（`<YOUR_JWT_TOKEN>`、`<FILE_NAME>` 等）替换为实际值。

| 语言 | 示例代码 |
|------|----------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC homepage\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC homepage\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC homepage\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC homepage',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC homepage\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC homepage');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC homepage',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC homepage', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*所有 SDK 均为开源项目，可前往 [Aspose.Cells Cloud GitHub 仓库](https://github.com/aspose-cells-cloud) 获取。*

---

## 参见 <a name="see-also"></a>

- **身份验证** – [JWT 令牌入门](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **存储操作** – [上传文件](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **其他超链接操作** – [添加超链接](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [删除超链接](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **OpenAPI 规范** – 端点完整定义：<https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*文档最后更新时间：2026‑07‑30*