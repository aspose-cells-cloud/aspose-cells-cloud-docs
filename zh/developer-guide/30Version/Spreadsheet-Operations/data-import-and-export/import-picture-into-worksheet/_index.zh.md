---
title: "将图片导入 Excel 工作表"
ArticleTitle: "将图片导入 Excel 工作表 – Aspose.Cells Cloud API 指南"
second_title: "文档"
linktitle: "导入图片"
type: docs
url: /import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "导入图片, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "了解如何使用 Aspose.Cells Cloud REST API v3.0 将图片导入 Excel 工作表。包含多部分请求示例、SDK 代码示例和错误处理指南。按照清晰的步骤快速上手。"
weight: 19
---

将图片导入 Excel 工作表，可为电子表格增添视觉内容，例如公司徽标、图表或示意图。本指南介绍如何使用 Aspose.Cells Cloud 的 **ImportPicture** 操作、所需请求格式以及如何处理响应。

**前置条件：** 调用导入操作前，您必须拥有有效的 JWT 认证令牌，并且已将工作簿存储在 Aspose Cloud 存储中。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### 安全性与身份验证

Aspose.Cells Cloud API 采用安全机制，需使用基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

该请求为 HTTP **POST** 请求，内容类型为 **multipart/related**（参见 [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。

- **第一部分** 包含一个名为 **ImportPictureOption** 的 JSON 对象，用于描述图片应放置的位置及方式。
- **第二部分** 携带图片文件（或其 Base64 编码数据）。

### ImportPictureOption 定义

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` 为 **布尔型**：`true` 表示插入新图片，`false` 表示替换已有图片。_

### 关键参数说明

**ImportPictureOption**

| 参数名称              | 类型        | 描述                                                                                                                                                                    |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UpperLeftRow          | int         | 图片左上角所在行索引。                                                                                                                                                   |
| UpperLeftColumn       | int         | 图片左上角所在列索引。                                                                                                                                                   |
| LowerRightRow         | int         | 定义图片右下角位置的行索引。                                                                                                                                             |
| LowerRightColumn      | int         | 定义图片右下角位置的列索引。                                                                                                                                             |
| Filename              | string      | 图片文件名称。                                                                                                                                                           |
| Data                  | string      | 图片的 Base64 编码二进制数据（若图片已作为第二部分上传则此项可选）。                                                                                                     |
| DestinationWorksheet  | string      | 将插入图片的目标工作表名称。                                                                                                                                             |
| **IsInsert**          | **boolean** | `true` 表示插入新图片；`false` 表示替换已有图片。                                                                                                                        |
| ImportDataType        | string      | 待导入数据类型（例如：`Picture`、`IntArray`、`DoubleArray`、`StringArray`、`TwoDimensionIntArray`、`TwoDimensionDoubleArray`、`TwoDimensionStringArray`、`BatchData`、`csvData`）。 |
| Source                | FileSource  | 当 `BatchData` 参数为空时，指示数据文件的位置。                                                                                                                          |

### 响应

成功请求返回 **HTTP 200**，JSON 负载示例如下：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

可能的状态码：

| 状态码 | 含义                     |
|--------|--------------------------|
| 200    | 导入成功                 |
| 400    | 请求错误 — 缺少或数据无效 |
| 401    | 未授权 — 令牌无效或缺失   |
| 500    | 服务器内部错误            |

## 如何结合 SDK 使用 PostImportData API

### PostImportData API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器发起 REST 请求。

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最优方式。SDK 会自动处理底层细节，让您专注于项目核心任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}