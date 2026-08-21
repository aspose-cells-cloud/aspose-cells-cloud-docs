---
title: "在 Excel 文件中搜索和替换文本内容"
second_title: "文档"
linktype: "搜索与替换"
type: docs
url: /zh/search-and-replace/
aliases: [  /zh/working-with-text/ , /zh/text/ ]
description: "了解如何使用 Aspose.Cells Cloud REST API 在 Excel 工作簿和工作表中搜索并替换文本。包含请求格式、.NET、Java、Python 的示例代码及错误处理。"
keywords: "Aspose.Cells Cloud, Excel, 搜索与替换, REST API, .NET, Java, Python"
weight: 20
ArticleTitle: "使用 Aspose.Cells Cloud API 在 Excel 文件中搜索与替换文本"
---

对 Excel 文件执行文本操作属于复杂流程，处理过程中需考虑多种因素。Aspose.Cells Cloud 提供了一种可靠的方式，用于在各种电子表格格式中搜索并替换文本。

在 Excel 工作簿中处理文本时，通常需要定位特定字符串，并在多个工作表中更新它们。Aspose.Cells Cloud API 通过提供统一的**搜索与替换**操作，简化了该任务，该操作适用于所有受支持的电子表格格式。

## 概述

搜索与替换功能可让您在工作簿或特定工作表中定位指定字符串，并将其替换为新值。该操作适用于 Aspose.Cells Cloud 支持的所有格式，例如 **XLS、XLSX、XLSM、XLSB、ODS、CSV** 等。借助**搜索与替换**功能，您可以快速清理数据、修正重复拼写错误，或在整个工作簿中批量应用命名规范。

## 前提条件

- 拥有有效的 **Client‑Id** 和 **Client‑Secret** 的活跃 Aspose.Cloud 账户。
- 通过 OAuth 2.0 认证流程获取的访问令牌。
- 目标工作簿必须存储于 Aspose Cloud 存储空间中，或可通过公开 URL 访问。
- 已安装所需 SDK（如 Aspose.Cells‑Cloud for .NET、Java 或 Python）。

## API 参考

**方法：** `POST`  
**端点**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| 参数             | 类型    | 必填项 | 描述                                                                   |
| ---------------- | ------- | ------ | ---------------------------------------------------------------------- |
| `fileName`       | string  | 是     | 工作簿名称（含扩展名）。                                               |
| `folder`         | string  | 否     | 云存储文件夹路径。                                                     |
| `storage`        | string  | 否     | 存储空间名称（非默认时）。                                             |
| `sheetName`      | string  | 否     | 特定工作表名称；若省略，则操作将应用于整个工作簿。                     |
| `searchString`   | string  | 是     | 要搜索的文本。                                                         |
| `replaceString`  | string  | 是     | 用于替换已找到内容的文本。                                             |
| `ignoreCase`     | boolean | 否     | 设置为 `true` 以执行不区分大小写的搜索。                              |
| `matchWholeCell` | boolean | 否     | 设置为 `true` 以仅替换整格匹配项。                                    |

**请求头**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**请求体（JSON）**

```json
{
  "searchString": "OldValue",
  "replaceString": "NewValue",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Sheet1"
}
```

**成功响应（JSON）**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## 支持的格式

| 格式                     | 扩展名                    |
| ------------------------ | ------------------------- |
| Excel 工作簿             | .xls、.xlsx、.xlsm、.xlsb |
| OpenDocument 电子表格    | .ods                      |
| CSV                    | .csv                      |
| 其他（由 Aspose.Cells 支持） | —                         |

## 代码示例

以下为三个主流 SDK 的最小化示例。请将 `{clientId}`、`{clientSecret}` 及其他占位符替换为您的实际值。这些示例展示了如何以编程方式执行**搜索与替换**操作。

## 错误处理与边界情况

| HTTP 状态码 | 含义                             | 建议操作                                               |
| ----------- | -------------------------------- | ------------------------------------------------------ |
| 400         | 请求错误 — 缺少或无效参数        | 核实必填字段及其数据类型。                             |
| 401         | 未授权 — 无效或已过期的令牌      | 刷新访问令牌。                                         |
| 404         | 未找到 — 工作簿或工作表不存在    | 检查文件名、文件夹路径及 `sheetName`。                |
| 415         | 不支持的媒体类型 — 文件格式无效  | 确保上传的文件为受支持的 Excel 或 CSV 格式。           |
| 202         | 已接受 — 请求已提交处理          | 若使用异步处理，请轮询操作状态。                       |
| 204         | 无内容 — 操作成功但无响应体      | 替换已应用，未返回额外数据。                           |
| 500         | 内部服务器错误 — 意外失败        | 稍后重试；若问题持续，请联系 Aspose 支持团队。         |

**备注：**  
- 较大的工作簿可能超出请求大小限制；建议先将文件上传至云存储。  
- 当 `ignoreCase` 设为 `true` 时，请注意区域设置相关的大小写映射可能影响结果。  
- 若对包含公式的单元格使用 `matchWholeCell`，不会替换公式文本中的部分匹配项。

## Excel 文件中的搜索与替换操作

- [如何从 Excel 工作簿中获取文本项](/cells/workbook/get-text-items/)  
- [如何从 Excel 工作表中获取文本项](/cells/worksheets/get-text-items/)  
- [如何从 Excel 工作簿中查找文本](/cells/workbook/find-text/)  
- [如何从 Excel 工作表中查找文本](/cells/worksheets/find-text/)  
- [如何在不上传文件的情况下从 Excel 文件中查找文本](/cells/search/)  
- [如何从 Excel 工作簿中替换文本](/cells/workbook/replace-text/)  
- [如何从 Excel 工作表中替换文本](/cells/worksheets/replace-text/)  
- [如何在不上传文件的情况下从 Excel 文件中替换文本](/cells/replace/)  

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "使用 Aspose.Cells Cloud API 在 Excel 文件中搜索与替换文本",
  "description": "Aspose.Cells Cloud 搜索与替换端点的文档，包含请求格式、参数、示例及错误处理。",
  "url": "https://docs.aspose.cloud/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, 搜索与替换, API, REST"
}
</script>