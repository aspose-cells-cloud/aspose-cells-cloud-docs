---
title: "将工作表转换为 HTML 表格"
ArticleTitle: "将工作表转换为 HTML 表格 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "ConvertWorksheetToHtmlTable"
type: docs
url: /cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, HTML 表格, API"
description: "使用 Aspose.Cells Cloud 将本地驱动器上的电子表格工作表转换为 HTML 表格文件。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的“将工作表转换为 HTML 表格”功能

此操作从本地文件系统读取电子表格文件，将其指定工作表转换为 HTML 表格，并以文件流形式返回转换结果。转换完全在云端服务器上执行，因此无需先将文件上传至云存储。该功能支持可选的区域设置及密码保护的电子表格文件。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------|--------|-----------------------------|------|
| Spreadsheet | 文件 | FormData                    | 上传电子表格文件。 |
| worksheet   | 字符串 | 查询字符串                  | 电子表格的工作表名称。（必填） |
| region      | 字符串 | 查询字符串                  | 电子表格的区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。 |
| password    | 字符串 | 查询字符串                  | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| *无* | *无* | *无需 JSON 请求体；文件以 multipart/form-data 形式发送。* |

### **响应**

```json
{
  "File": "生成的 HTML 表格的二进制流"
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | 成功 | 工作表已成功转换为 HTML 表格，并以文件流形式返回。 |
| 400 | 请求错误 | 请求 URL 无效或缺少必需参数。 |
| 401 | 未授权 | 身份验证失败或未提供凭据。 |
| 404 | 未找到 | 源文件无法访问。 |
| 500 | 内部服务器错误 | 电子表格在获取转换数据时发生异常。 |
| 413 | 请求实体过大 | 上传文件超出允许的大小限制。 |

## 如何使用 SDK 调用“将工作表转换为 HTML 表格”功能

### Convert Worksheet To Html Table 规范说明

[Convert Worksheet To Html Table API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API：

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 保证安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "生成的 HTML 表格的二进制流"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您能够专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Cloud Web 服务：
`[待补充]`