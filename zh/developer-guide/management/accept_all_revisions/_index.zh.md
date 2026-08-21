---
title: "接受所有修订"
ArticleTitle: "接受所有修订 – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "接受所有修订"
type: docs
url: /zh/cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, 电子表格, 修订"
description: "使用 Aspose.Cells Cloud API 接受电子表格文件中的所有修订。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的 AcceptAllRevisions 功能

接受上传的电子表格文件中的所有修订，并返回已处理的工作簿。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------------|--------|-----------------------------|------|
| Spreadsheet    | 文件   | FormData（HTTP 请求体）     | 上传电子表格文件。 |
| outPath        | 字符串 | 查询参数                    | （可选）工作簿存储的文件夹路径。默认为 null。 |
| outStorageName | 字符串 | 查询参数                    | 输出文件的存储名称。 |
| fontsLocation  | 字符串 | 查询参数                    | 使用自定义字体。 |
| region         | 字符串 | 查询参数                    | 电子表格区域/语言设置（例如 `en-US`、`fr-FR`）。影响数字格式、日期解析和特定区域的行为。 |
| password       | 字符串 | 查询参数                    | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称   | 类型 | 描述             |
| ---------- | ---- | ---------------- |
| Spreadsheet | 文件 | 上传电子表格文件。 |

### **响应**

```json
{
  "File": "已处理电子表格的二进制流"
}
```

**响应状态码**

| 状态码 | 含义           | 描述 |
|--------|----------------|------|
| 200    | OK（成功）     | 修订已成功接受，并返回已处理的文件。 |
| 400    | Bad Request（错误请求） | 请求无效（例如，缺少必需文件或参数错误）。 |
| 401    | Unauthorized（未授权） | 身份验证失败或 JWT 令牌缺失/无效。 |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过允许的大小限制。 |
| 500    | Internal Server Error（服务器内部错误） | 服务器上发生意外错误。 |

## 如何使用 SDK 调用 AcceptAllRevisions

### AcceptAllRevisions 规范

[AcceptAllRevisions API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "已处理电子表格的二进制流"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 抽象了底层细节，让您能够专注于项目任务。请查阅 <a href="[TBD]" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Cloud Web 服务：
 `[TBD]`
---