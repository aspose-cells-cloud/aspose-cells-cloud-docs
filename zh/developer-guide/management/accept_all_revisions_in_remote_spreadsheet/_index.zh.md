---
title: "接受远程电子表格中的所有修订"
ArticleTitle: "接受远程电子表格中的所有修订 – Aspose.Cells Cloud"
second_title: "文档"
linktype: "docs"
url: /zh/cells/accept-all-revisions
aliases: [  /zh/cells/accept-all-revisions ]
keywords: "Aspose.Cells, AcceptAllRevisions, 远程电子表格"
description: "接受远程电子表格中的所有修订，并返回更新后的工作簿文件。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务的接受远程电子表格中的所有修订功能

接受存储在远程存储中的指定工作簿中所有被跟踪的更改（修订）。该操作可选择性地将更新后的工作簿写入其他位置或存储，并以二进制流形式返回更新后的文件。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------|------|-----------------------------|------|
| name | string | 路径 | 存储在远程存储中的工作簿文件名。 |
| folder | string | 查询字符串 | （可选）工作簿所在的存储文件夹。 |
| storageName | string | 查询字符串 | （可选）若使用自定义云存储，则指定存储名称；省略则使用默认存储。 |
| outPath | string | 查询字符串 | （可选）应保存更新后工作簿的文件夹路径；默认为 null。 |
| outStorageName | string | 查询字符串 | （可选）输出文件的存储名称。 |
| fontsLocation | string | 查询字符串 | （可选）自定义字体路径。 |
| region | string | 查询字符串 | （可选）电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式化、日期解析和本地化相关行为。 |
| password | string | 查询字符串 | （可选）打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| *无* | *无* | 此操作不需要请求体。 |

### **响应**

```json
{
  "File": "以响应体形式返回的更新后工作簿的二进制流（例如 .xlsx）。"
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 包含已接受所有修订的工作簿的二进制文件流。 |
| 400 | Bad Request（错误请求） | 缺少必需参数或请求格式无效。 |
| 401 | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413 | Payload Too Large（请求实体过大） | 请求超出允许的大小限制。 |
| 500 | Internal Server Error（服务器内部错误） | 服务器发生意外错误。 |

## 如何使用 SDK 调用接受远程电子表格中的所有修订功能

### 接受远程电子表格中的所有修订 API 规范

[接受远程电子表格中的所有修订 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "更新后工作簿的二进制流（例如 .xlsx）。"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，使您能专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[待补充]`
---