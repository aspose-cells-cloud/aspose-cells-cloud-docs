---
title: "搜索电子表格中所有文本项"
ArticleTitle: "搜索电子表格中所有文本项 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "搜索电子表格中所有文本项"
type: docs
url: /cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, 搜索, 文本项, API"
description: "使用 Aspose.Cells Cloud API 搜索电子表格文件中的所有文本项。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的搜索电子表格中所有文本项

此方法用于搜索本地电子表格文件中的所有文本项。它支持遍历工作簿的所有工作表和单元格，识别搜索词的出现位置。该操作在云端执行，无需使用云存储。请确保您具有读取源文件的必要权限。如果无法访问源文件，或在搜索过程中发生错误（例如文件格式不受支持），将抛出相应的异常。根据具体实现，该方法可能会返回匹配项的位置（例如工作表名称、单元格坐标）。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|--------|------|-----------------------------|------|
| Spreadsheet | 文件 | FormData | 上传电子表格文件。 |
| region | 字符串 | 查询字符串 | 电子表格区域/语言设置（例如 `en-US`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。 |
| password | 字符串 | 查询字符串 | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名 | 类型 | 描述 |
| ------ | ---- | ---- |
| [待定] | [待定] | [待定] |

### **响应**

```json
{
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "示例文本"
    }
    // ... 更多项
  ],
  "TotalCount": 42
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | 成功 | 请求成功，响应中包含所有找到的文本项。 |
| 400 | 错误请求 | URL 无效或请求参数格式错误。 |
| 401 | 未授权 | 身份验证失败，或未提供凭据。 |
| 404 | 未找到 | 源文件无法访问。 |
| 413 | 请求体过大 | 上传的文件超出允许的大小限制。 |
| 500 | 内部服务器错误 | 电子表格在获取数据时发生异常。 |

## 如何使用 SDK 实现搜索电子表格中所有文本项功能

### 搜索电子表格中所有文本项 API 规范

[搜索电子表格中所有文本项 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器进行 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 保证安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=zh-CN&password=myPassword" \
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
  "SearchResults": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Text": "示例文本"
    }
    // ... 更多项
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最快方式。SDK 将底层细节抽象化，使您能够专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Cloud Web 服务：
`[待定]`
---