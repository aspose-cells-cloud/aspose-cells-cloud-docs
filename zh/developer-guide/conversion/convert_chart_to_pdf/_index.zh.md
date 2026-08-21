---
title: "将图表转换为 PDF"
ArticleTitle: "将图表转换为 PDF – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "ConvertChartToPdf"
type: docs
url: /cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, 图表转换"
description: "将本地磁盘上电子表格中的图表转换为 PDF。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的图表转 PDF 功能

该方法通过本地文件上传方式读取电子表格文件中的图表，将其转换为 PDF 格式，并返回转换后的结果。整个过程完全在云端服务器上执行，因此无需中间存储。源文件路径和目标格式必须正确，并且需要具备读取源文件的相应权限。缺失文件、访问问题或转换失败等错误将返回相应的 HTTP 错误响应。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|------------------|--------|-----------------------------|------|
| Spreadsheet      | 文件   | FormData                    | 上传电子表格文件。 |
| worksheet        | 字符串 | 查询参数                    | 电子表格中的工作表名称。 |
| chartIndex       | 整数   | 查询参数                    | 工作表中的图表索引。 |
| outPath          | 字符串 | 查询参数                    | （可选）工作簿存储的文件夹路径；默认为 null。 |
| outStorageName   | 字符串 | 查询参数                    | 输出文件的存储名称。 |
| fontsLocation    | 字符串 | 查询参数                    | 使用自定义字体。 |
| region           | 字符串 | 查询参数                    | 电子表格区域/语言设置（例如 `en-US`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。 |
| password         | 字符串 | 查询参数                    | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称   | 类型 | 描述         |
|------------|------|--------------|
| Spreadsheet | 文件 | 上传电子表格文件。 |

### **响应**

```json
{
  "ResponseFile": "二进制 PDF 文件流"
}
```

**响应状态码**

| 状态码 | 含义         | 描述 |
|--------|--------------|------|
| 200    | 成功 (OK)    | 图表成功转换为 PDF；返回二进制 PDF 文件。 |
| 400    | 请求错误 (Bad Request) | 请求参数无效或 URL 格式不正确。 |
| 401    | 未授权 (Unauthorized) | 身份验证失败或未提供凭据。 |
| 404    | 未找到 (Not Found) | 无法访问源文件。 |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件超过允许的大小限制。 |
| 500    | 内部服务器错误 (Internal Server Error) | 处理转换过程中发生错误。 |

## 如何使用 SDK 实现图表转 PDF 功能

### 图表转 PDF 规范说明

[图表转 PDF API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API：

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}
{< tab tabNum="1" >}
```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "二进制 PDF 文件流"
}
```
{< /tab >}
{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 将底层细节抽象化，使您能够专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`
---