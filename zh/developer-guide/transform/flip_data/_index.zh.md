---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "FlipData"
type: docs
url: /cells/flip
aliases: []
keywords: "FlipData, 转置, Aspose.Cells"
description: "对电子表格文件中指定的数据范围进行转置操作。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的 FlipData 功能

该 API 可翻转给定数据矩阵的方向。例如，一个 3 行 × 2 列的区域（3 行 2 列）在输出中将变为 2 行 × 3 列（2 行 3 列）。该功能常用于重新组织数据，以满足不同图表、报表或数据模型的输入要求。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **安全性与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称       | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------------|--------|-----------------------------|------|
| Spreadsheet    | 文件   | FormData                    | 上传电子表格文件。 |
| worksheet      | 字符串 | 查询参数                    | 工作表名称。 |
| cellArea       | 字符串 | 查询参数                    | 指定的数据区域。 |
| Horizontal     | 布尔值 | 查询参数                    | 水平/垂直翻转。默认值：true |
| outPath        | 字符串 | 查询参数                    | （可选）工作簿存储的文件夹路径。默认为 null。 |
| outStorageName | 字符串 | 查询参数                    | 输出文件的存储名称。 |
| region         | 字符串 | 查询参数                    | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式化、日期解析及区域性特定行为。 |
| password       | 字符串 | 查询参数                    | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| *无*     | *不适用* | *无需额外 JSON 请求体；文件以 multipart/form-data 形式发送。* |

### **响应**

```json
{
  "File": "<转换后工作簿的二进制流>"
}
```

**响应状态码**

| 状态码 | 含义         | 描述 |
|--------|--------------|------|
| 200    | 成功         | 操作成功完成，并返回转换后的电子表格文件。 |
| 400    | 请求错误     | 缺失或无效的一个或多个必需参数。 |
| 401    | 未授权       | 身份验证失败 — 缺失或无效的 JWT 令牌。 |
| 413    | 请求实体过大 | 上传的文件超出允许的大小限制。 |
| 500    | 服务器内部错误 | 服务器上发生意外错误。 |

## 如何在 SDK 中使用 FlipData

### FlipData 规范

[FlipData API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=zh-CN&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<转换后工作簿的二进制流>"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，使您能专注于项目任务本身。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[TBD]`
---