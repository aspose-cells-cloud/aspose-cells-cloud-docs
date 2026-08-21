---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "远程电子表格结构获取 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "docs"
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, 结构获取, 电子表格, 结构"
description: "检索远程 Excel 工作簿的结构元数据，包括工作表、表格、数据透视表、图表、形状及其他核心信息。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的远程电子表格结构获取功能

将 Excel 工作簿的核心元数据、工作表、表格、数据透视表、图表、形状及其他信息，结构化转换为 JObject 类型的 JSON 对象，适用于数据导出、API 响应及日志记录等场景。

### Web API 端点

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|--------|------|----------------------------|------|
| name | string | Path | 电子表格文件的名称。 |
| folder | string | Query | 文件所在文件夹。（可选） |
| storageName | string | Query | （可选）若使用自定义云存储，则指定其名称；省略时使用默认存储。 |
| region | string | Query | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式化、日期解析及区域性特定行为。 |
| password | string | Query | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名 | 类型 | 描述 |
|--------|------|------|
| [TBD] | [TBD] | [TBD] |

### **响应**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK（成功） | 成功获取工作簿结构。 |
| 400 | Bad Request（错误请求） | 请求参数无效。 |
| 401 | Unauthorized（未授权） | 身份验证失败或缺少令牌。 |
| 413 | Payload Too Large（请求体过大） | 请求体超出允许的最大尺寸。 |
| 500 | Internal Server Error（内部服务器错误） | 服务器发生意外错误。 |

## 如何使用 SDK 调用远程电子表格结构获取功能

### 远程电子表格结构获取规范

[远程电子表格结构获取 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) 定义了公开可访问的编程接口，您可直接通过 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`
---