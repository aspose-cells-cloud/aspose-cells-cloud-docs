---
title: "远程电子表格中删除字符"
ArticleTitle: "远程电子表格中删除字符 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "远程电子表格中删除字符"
type: docs
url: /zh/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, 删除字符, 文本处理"
description: "在选定的单元格范围内，从每个单元格中删除用户自定义字符、预定义符号集或任意子字符串，同时保留公式、格式和数据验证，适用于远程电子表格。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的远程电子表格中删除字符功能

在选定的单元格范围内，从每个单元格中删除用户自定义字符、预定义符号集或任意子字符串，同时保留公式、格式和数据验证，适用于远程电子表格。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需采用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称            | 类型    | 路径 / 查询字符串 / HTTP 请求体 | 描述                                                                                                                                                           |
|---------------------|---------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string  | 路径                          | （必填）要获取的电子表格工作簿文件名。                                                                                                                          |
| worksheet           | string  | 路径                          | 指定电子表格中的工作表名称。                                                                                                                                    |
| range               | string  | 路径                          | 指定电子表格中的工作表范围。                                                                                                                                    |
| removeTextMethod    | string  | 查询字符串                    | 指定文本删除方法类型。                                                                                                                                          |
| characterSets       | string  | 查询字符串                    | 指定要删除的字符集。                                                                                                                                            |
| removeCustomValue   | string  | 查询字符串                    | 指定要删除的自定义值。                                                                                                                                          |
| caseSensitive       | boolean | 查询字符串                    | 启用时影响 `Substring`（子字符串）模式及 `CustomChars`（自定义字符）模式。                                                                                      |
| folder              | string  | 查询字符串                    | （可选）工作簿所在文件夹路径，默认为 null。                                                                                                                     |
| storageName         | string  | 查询字符串                    | （可选）使用自定义云存储时指定存储名称；若省略则使用默认存储。                                                                                                   |
| region              | string  | 查询字符串                    | 电子表格区域/语言设置（如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式化、日期解析及本地化行为。                                                                   |
| password            | string  | 查询字符串                    | 打开电子表格文件所需的密码。                                                                                                                                    |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| *无*     | *无* | 此操作无需请求体。 |

### **响应示例**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "字符删除成功。",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**响应状态码说明**

| 状态码 | 含义       | 描述                                         |
|--------|------------|----------------------------------------------|
| 200    | OK（成功） | 字符删除成功，工作簿已更新。                 |
| 400    | Bad Request（错误请求） | 缺少或无效的参数。                          |
| 401    | Unauthorized（未授权） | 身份验证失败 — 缺少或无效的 JWT 令牌。      |
| 413    | Payload Too Large（请求体过大） | 请求大小超出允许限制。                    |
| 500    | Internal Server Error（服务器内部错误） | 服务器端发生意外错误。                  |

## 如何结合 SDK 使用“远程电子表格中删除字符”功能

### 远程电子表格中删除字符功能说明

[远程电子表格中删除字符 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) 定义了公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例演示如何使用 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "字符删除成功。",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 将底层细节抽象化，让您专注于项目核心任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码仓库</a> 了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`
---