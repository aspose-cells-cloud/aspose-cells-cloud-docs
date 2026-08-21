---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "TransposeData"
type: docs
url: /zh/cells/transpose
aliases: [  /zh/cells/transpose ]
keywords: "TransposeData, Aspose.Cells, 云 API, 电子表格, 转置"
description: "在电子表格中交换行和列。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务的 TransposeData 功能

在电子表格中交换行和列。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名           | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                     |
|------------------|--------|-----------------------------|----------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 文件   | FormData                    | 上传电子表格文件。                                                                                       |
| worksheet        | 字符串 | 查询参数                    | 工作表名称。                                                                                             |
| cellArea         | 字符串 | 查询参数                    | 指定的数据范围。                                                                                         |
| outPath          | 字符串 | 查询参数                    | （可选）工作簿存储的文件夹路径。默认为 null。                                                            |
| outStorageName   | 字符串 | 查询参数                    | 输出文件的存储名称。                                                                                     |
| region           | 字符串 | 查询参数                    | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式、日期解析及区域性相关行为。                 |
| password         | 字符串 | 查询参数                    | 打开电子表格文件所需的密码。                                                                             |

### 请求体参数

| 参数名 | 类型 | 描述 |
| ------ | ---- | ---- |
| [TBD]  | [TBD] | [TBD] |

### **响应**

```json
{
  "file": "转置后的电子表格二进制流"
}
```

**响应状态码**

| 状态码 | 含义         | 描述                           |
|--------|--------------|--------------------------------|
| 200    | OK（成功）   | 返回转置后的电子表格文件。     |
| 400    | Bad Request（错误请求） | 输入参数无效或请求格式错误。 |
| 401    | Unauthorized（未授权） | 身份验证失败或 JWT 令牌缺失/无效。 |
| 413    | Payload Too Large（请求体过大） | 上传文件超过允许大小限制。 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

## 如何使用 SDK 调用 TransposeData 功能

### TransposeData 规范

[TransposeData API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) 定义了一个公开可访问的编程接口，让您能够直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用云 API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=zh-CN&password=MyPassword" \
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
  "file": "转置后的电子表格二进制流"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，使您能够专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`
---