---
title: "Aspose.Cells Cloud – 合并、拆分与导入电子表格数据"
second_title: "文档"
ArticleTitle: "电子表格数据处理 – 合并、拆分与导入"
linktype: "数据处理"
type: docs
url: /zh/data-processing/
keywords: "Aspose.Cells Cloud, 电子表格数据处理, Excel 合并, Excel 拆分, CSV 导入, JSON 导入, API"
description: "通过 Aspose.Cells Cloud REST API 导入 CSV/JSON 数据、合并远程 Excel 工作簿及拆分大型电子表格的详细指南，包含请求/响应示例。"
weight: 30
---

**Aspose.Cells Cloud** 是一种 RESTful 服务，支持在云端以编程方式操作 Excel 文件。它支持从多种格式导入数据、合并工作簿以及拆分大型电子表格。

Aspose.Cells Cloud API 的 **数据处理** 功能模块使您能够以编程方式导入、合并和拆分电子表格数据。请使用以下端点处理 CSV/JSON 导入、合并工作簿或拆分大型文件为更易管理的片段。

## 数据导入与管理

- **[将 CSV、JSON、XML 数据导入 Excel 文件](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

导入操作接受 CSV、JSON 或 XML 格式的请求体，并在目标工作簿中创建新工作表（或更新已有工作表）。

**端点详情**

| HTTP 方法 | 端点 | 请求体 | 成功响应 |
|-----------|------|--------|----------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` 或 `text/csv`（取决于格式） | `200 OK`，返回包含更新后工作簿元数据的 JSON |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *无* | 返回已处理的工作簿文件 |

**示例 cURL 请求（CSV 导入）**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**示例 JSON 响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **前提条件**：需要 OAuth2 访问令牌。源文件必须位于 Aspose Cloud 存储中，或通过 multipart 上传方式提供。

## 文件合并操作

- **[将远程 Excel 文件合并到指定工作簿中](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[将多个 Excel 文件合并为单个工作簿](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[合并远程文件夹中符合匹配条件的 Excel 文件](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

合并操作将两个或多个工作簿合并为单个目标工作簿。API 支持显式文件列表合并，以及基于模式在存储文件夹内进行合并。

**端点详情**

| HTTP 方法 | 端点 | 参数 | 成功响应 |
|-----------|------|------|----------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files`（文件名数组），`target`（可选目标工作簿名称） | `200 OK`，返回描述已合并工作簿的 JSON |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`，`pattern`，`target` | `200 OK`，返回已合并工作簿的元数据 |

**示例 cURL 请求（合并显式文件列表）**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**示例 JSON 响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **前提条件**：所有源工作簿必须存储在同一云存储位置，且调用者需具备读/写权限。

## 文件拆分操作

- **[按工作表将 Excel 文件拆分为多个文件](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[按自定义规则拆分 Excel 文件](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

拆分操作将单个工作簿拆分为多个独立的工作簿文件，可按工作表、行或列进行拆分。

**端点详情**

| HTTP 方法 | 端点 | 参数 | 成功响应 |
|-----------|------|------|----------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy`（如 `worksheet`），`outputFolder` | `200 OK`，返回生成的文件 URL 列表 |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | 自定义规则 JSON（页大小、行范围等） | `200 OK`，返回拆分文件详情 |

**示例 cURL 请求（按工作表拆分）**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**示例 JSON 响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **前提条件**：源工作簿必须可被访问（位于 Aspose Cloud 存储中），且调用者需具备目标文件夹的写入权限。