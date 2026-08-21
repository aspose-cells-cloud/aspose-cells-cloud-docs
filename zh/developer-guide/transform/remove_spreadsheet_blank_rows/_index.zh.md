---
title: "删除电子表格中的空白行"
ArticleTitle: "删除电子表格中的空白行 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "删除电子表格中的空白行"
type: docs
url: /cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, 删除空白行, 电子表格, API"
description: "从电子表格文件中删除所有空白行。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的删除电子表格空白行功能

此方法用于删除电子表格中完全为空的行（即不包含任何数据或对象的行）。该方法会扫描所有工作表，并识别其中每个单元格均为空的行。操作直接在电子表格上执行，确保仅删除无内容的行。这有助于清理电子表格，移除不必要的空白行，使数据更加整洁、易于管理。用户在执行此操作前应确保已对电子表格进行备份，因为被删除的行无法恢复。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------------|--------|-----------------------------|------|
| Spreadsheet    | 文件   | FormData                    | 上传电子表格文件。 |
| outPath        | 字符串 | 查询字符串                  | （可选）工作簿所在文件夹路径，默认为 null。 |
| outStorageName | 字符串 | 查询字符串                  | 输出文件的存储名称。 |
| region         | 字符串 | 查询字符串                  | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。 |
| password       | 字符串 | 查询字符串                  | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称    | 类型 | 描述             |
| ----------- | ---- | ---------------- |
| Spreadsheet | 文件 | 上传电子表格文件。 |

### **响应**

```json
{
  "ResponseFile": "二进制文件流"
}
```

**响应状态码**

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | 成功 (OK)        | 返回已删除空白行的处理后电子表格文件。     |
| 400    | 错误请求 (Bad Request) | URL 或请求参数无效。                     |
| 401    | 未授权 (Unauthorized) | 身份验证失败或未提供凭据。               |
| 404    | 未找到 (Not Found) | 源文件无法访问。                         |
| 413    | 请求实体过大 (Payload Too Large) | 请求体超过允许大小。                   |
| 500    | 内部服务器错误 (Internal Server Error) | 电子表格在获取数据时发生异常。         |

## 如何使用 SDK 调用删除电子表格空白行功能

### 删除电子表格空白行规范

[删除电子表格空白行 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API：

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}
{< tab tabNum="1" >}
```bash
# 使用 HTTPS 保证连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=zh-CN&password=12345" \
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
  "ResponseFile": "二进制文件流"
}
```
{< /tab >}
{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`
---