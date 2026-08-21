---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /zh/cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, 电子表格结构, API"
description: "将 Excel 工作簿的核心元数据、工作表、表格、数据透视表、图表、形状及其他信息结构化转换为 JObject 类型的 JSON 对象。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务的 GetSpreadsheetStructure

将 Excel 工作簿的核心元数据、工作表、表格、数据透视表、图表、形状及其他信息结构化转换为 JObject 类型的 JSON 对象，适用于数据导出、API 响应及日志记录等场景。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **安全性与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名       | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
|--------------|--------|-----------------------------|----------------------------------------------------------------------|
| Spreadsheet  | 文件   | FormData（请求体）           | 上传电子表格文件。                                                   |
| region       | 字符串 | 查询字符串                   | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式化、日期解析及区域性相关行为。 |
| password     | 字符串 | 查询字符串                   | 打开电子表格文件所需的密码。                                         |

### 请求体参数

| 参数名      | 类型 | 描述             |
| ----------- | ---- | ---------------- |
| Spreadsheet | 文件 | 上传电子表格文件。 |

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
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**响应状态码**

| 状态码 | 含义             | 描述                               |
|--------|------------------|------------------------------------|
| 200    | OK（成功）       | 成功获取电子表格结构。             |
| 400    | Bad Request（错误请求） | 请求参数无效或文件格式不正确。     |
| 401    | Unauthorized（未授权） | 身份验证失败或缺失 JWT 令牌。      |
| 413    | Payload Too Large（载荷过大） | 上传文件超出允许的大小限制。       |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。               |

## 如何使用 GetSpreadsheetStructure 配合 SDK

### GetSpreadsheetStructure 规范

[GetSpreadsheetStructure API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=zh-CN&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
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
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，使您能专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[TBD]`
---