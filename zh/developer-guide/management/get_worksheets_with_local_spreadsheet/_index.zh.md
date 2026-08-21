---
title: "使用本地电子表格获取工作表"
ArticleTitle: "使用本地电子表格获取工作表 – Aspose.Cells Cloud"
second_title: "文档"
linktype: "docs"
url: /cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, 工作表, 本地电子表格, API"
description: "获取当前活动本地电子表格中所有工作表的完整列表。"
weight: 1000
---

## Aspose.Cells Cloud 网络服务的“使用本地电子表格获取工作表”功能

该端点通过互操作或本地 API 访问本地电子表格应用程序（例如 Excel），收集每个工作表的名称和类型（例如标准、图表、宏），并将集合以结构化的 JSON 数组形式返回。它通常用于填充工作表选择器 UI 或审计电子表格内容。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型   | 路径/查询字符串/HTTP 请求体 | 描述 |
|--------------|--------|-----------------------------|------|
| Spreadsheet  | 文件   | FormData（HTTP 请求体）     | 上传电子表格文件。 |
| region       | 字符串 | 查询参数                    | 电子表格区域/语言设置（例如 `en-US`、`fr-FR`）。影响数字格式化、日期解析和区域特定行为。*（可选）* |
| password     | 字符串 | 查询参数                    | 打开电子表格文件所需的密码。*（可选）* |

### 请求体参数

| 参数名称    | 类型 | 描述             |
|-------------|------|------------------|
| Spreadsheet | 文件 | 上传电子表格文件。 |

### **响应**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... 更多工作表
  ]
}
```

**响应状态码**

| 状态码 | 含义         | 描述 |
|--------|--------------|------|
| 200    | 成功         | 工作表列表已成功获取。 |
| 400    | 错误请求     | 请求无效（例如 URL 格式错误或缺少必需数据）。 |
| 401    | 未授权       | 身份验证失败或未提供凭据。 |
| 404    | 未找到       | 源文件无法访问。 |
| 413    | 请求实体过大 | 上传的文件大小超过允许的限制。 |
| 500    | 内部服务器错误 | 获取数据时电子表格出现异常。 |

## 如何使用 SDK 实现“使用本地电子表格获取工作表”功能

### “使用本地电子表格获取工作表”规范

[“使用本地电子表格获取工作表”API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
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
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... 更多工作表
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最快方法。SDK 将底层细节抽象化，使您能够专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Cloud 网络服务：
`[TBD]`