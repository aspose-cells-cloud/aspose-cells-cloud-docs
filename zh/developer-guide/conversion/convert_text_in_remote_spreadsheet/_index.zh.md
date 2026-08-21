---
title: "远程电子表格中的文本转换"
ArticleTitle: "远程电子表格中的文本转换 – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "远程电子表格中的文本转换"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, 文本转换, API"
description: "转换工作表指定区域内的文本，包括数字转换、字符替换、换行符处理以及带重音字符的标准化。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务中的远程电子表格文本转换功能

表示将存储为文本的数字转换为正确的数字格式，将不需要的字符和换行符替换为所需的字符，并将带重音的字符转换为等效的无重音字符。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|------------------|--------|-----------------------------|------|
| name             | string | 路径 |（必需）要检索的工作簿文件名称。 |
| worksheet        | string | 路径 | 指定电子表格中的工作表。 |
| range            | string | 路径 | 指定电子表格工作表的区域范围。 |
| convertTextType  | string | 查询 | 指定文本类型转换方式。（必需） |
| sourceCharacters | string | 查询 | 指定源字符。（可选） |
| targetCharacters | string | 查询 | 指定目标字符。（可选） |
| folder           | string | 查询 |（可选）工作簿所在文件夹路径，默认为 null。 |
| storageName      | string | 查询 |（可选）若使用自定义云存储，则指定其名称；省略则使用默认存储。 |
| region           | string | 查询 | 电子表格区域/语言设置（如 `zh-CN`、`fr-FR`），影响数字格式、日期解析及区域特定行为。（可选） |
| password         | string | 查询 | 打开电子表格文件所需的密码。（可选） |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| - | - | - |

### **响应**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "文本转换成功完成。",
  "Data": {
    // 转换结果详情（如更新的单元格数量）可在此处添加。
  }
}
```

**响应状态码说明**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 文本转换操作成功完成。 |
| 400 | Bad Request（错误请求） | 请求格式错误或缺少必需参数。 |
| 401 | Unauthorized（未授权） | 身份验证失败，或 JWT 令牌缺失/无效。 |
| 413 | Payload Too Large（请求体过大） | 请求体超过允许的最大尺寸限制。 |
| 500 | Internal Server Error（服务器内部错误） | 服务器发生意外错误。 |

## 如何结合 SDK 使用远程电子表格文本转换功能

### 远程电子表格文本转换 API 规范

[远程电子表格文本转换 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) 定义了公开可访问的编程接口，支持您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "文本转换成功完成。",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "数字已转换、字符已替换、换行符已标准化。"
  }
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 抽象了底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose Cells Cloud Web 服务：
`[待补充]`
---