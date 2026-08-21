---
title: "计算公式"
ArticleTitle: "计算公式 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "计算公式"
type: docs
url: /zh/cells/calculate/formula
aliases: []
keywords: "Aspose Cells, 计算公式, 电子表格, API"
description: "使用 Aspose.Cells Cloud API 在电子表格中计算指定公式。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的计算公式功能

计算上传的电子表格文件中指定工作表内的给定公式，并以文件流形式返回计算后的电子表格。该操作通过 **region** 参数支持本地化处理，并可打开受密码保护的文件。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------|------|----------------------------|------|
| Spreadsheet（电子表格） | 文件 | FormData（表单数据） | 上传电子表格文件。 |
| worksheet（工作表名称） | 字符串 | 查询参数 | 包含待计算公式的电子表格工作表名称。 |
| formula（公式） | 字符串 | 查询参数 | 待计算的公式（例如：`=SUM(A1:B2)`）。 |
| region（区域） | 字符串 | 查询参数 | 电子表格区域/语言设置（例如：`en-US`、`fr-FR`）。影响数字格式化、日期解析及本地化相关行为。 |
| password（密码） | 字符串 | 查询参数 | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
|----------|------|------|
| [TBD] | [TBD] | [TBD] |

### **响应**

```json
{
  "File": "<计算后电子表格的二进制流>"
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 计算成功；返回计算后的电子表格文件。 |
| 400 | Bad Request（错误请求） | 缺少或存在无效的请求参数。 |
| 401 | Unauthorized（未授权） | 身份验证失败，或 JWT 令牌缺失/无效。 |
| 413 | Payload Too Large（请求体过大） | 上传文件超过允许的大小限制。 |
| 500 | Internal Server Error（服务器内部错误） | 服务器发生意外错误。 |

## 如何通过 SDK 使用计算公式功能

### 计算公式规范

[计算公式 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=en-US&password=MyPassword" \
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
  "File": "<计算后电子表格的二进制流>"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 将底层细节抽象化，让您能够专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
 `[TBD]`
---