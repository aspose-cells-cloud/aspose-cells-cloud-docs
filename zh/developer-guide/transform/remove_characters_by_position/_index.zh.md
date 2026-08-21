---
title: "按位置删除字符"
ArticleTitle: "按位置删除字符 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "按位置删除字符"
type: docs
url: /zh/cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, 删除字符, API"
description: "在电子表格中按位置从单元格中删除字符。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的按位置删除字符功能

按位置（前/后 N 个字符、指定子字符串之前/之后，或两个分隔符之间）从目标范围内的每个单元格中删除字符，同时保留公式、格式和数据验证。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称                  | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
|---------------------------|---------|-----------------------------|----------------------------------------------------------------------|
| Spreadsheet               | 文件    | FormData                    | 上传电子表格文件。                                                   |
| theFirstNCharacters       | 整数    | 查询参数                    | 指定从所选单元格中删除前 N 个字符。可选。                            |
| theLastNCharacters        | 整数    | 查询参数                    | 指定从所选单元格中删除后 N 个字符。可选。                            |
| allCharactersBeforeText   | 字符串  | 查询参数                    | 删除位于指定子字符串之前的所有字符。可选。                           |
| allCharactersAfterText    | 字符串  | 查询参数                    | 删除位于指定子字符串之后的所有字符。可选。                           |
| caseSensitive             | 布尔值  | 查询参数                    | 启用时影响 `Substring` 模式与 `CustomChars`。可选。                  |
| worksheet                 | 字符串  | 查询参数                    | 指定电子表格的工作表名称。可选。                                     |
| range                     | 字符串  | 查询参数                    | 指定电子表格的工作表范围（例如 `A1:B10`）。可选。                    |
| outPath                   | 字符串  | 查询参数                    | （可选）工作簿保存的文件夹路径。默认为 null。可选。                  |
| outStorageName            | 字符串  | 查询参数                    | 输出文件的存储名称。可选。                                           |
| region                    | 字符串  | 查询参数                    | 电子表格区域/语言设置（例如 `en-US`、`fr-FR`）。可选。               |
| password                  | 字符串  | 查询参数                    | 打开电子表格文件所需的密码。可选。                                   |

### 请求体参数

| 参数名称   | 类型 | 描述             |
|------------|------|------------------|
| Spreadsheet | 文件 | 上传电子表格文件。 |

### **响应**

```json
{
  "status": "OK",
  "message": "字符已成功删除。",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**响应状态码**

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | OK（成功）       | 操作成功完成，并返回已处理的文件。         |
| 400    | Bad Request（错误请求） | 请求格式错误或包含无效参数。               |
| 401    | Unauthorized（未授权） | 身份验证失败，或 JWT 令牌缺失/无效。       |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出允许的大小限制。             |
| 500    | Internal Server Error（服务器内部错误） | 服务器端发生意外错误。                     |

## 如何结合 SDK 使用按位置删除字符功能

### 按位置删除字符规范

[按位置删除字符 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "字符已成功删除。",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 将底层细节抽象化，使您能专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`
---