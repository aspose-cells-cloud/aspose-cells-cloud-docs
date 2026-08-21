---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "docs"
url: /zh/cells/{name}/search/content/all-textitems
aliases: []
keywords: "搜索, 文本项, Aspose.Cells"
description: "使用 Aspose.Cells Cloud 在远程电子表格中搜索所有文本项。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的 SearchAllTextItemsInRemoteSpreadsheet 方法

此方法用于在远程电子表格文件中搜索所有文本项。它支持遍历工作簿中的所有工作表和单元格，定位搜索词的出现位置。该操作在云端执行，无需本地存储空间。请确保您具备读取源文件的必要权限。如果无法访问源文件，或在搜索过程中发生错误（例如不支持的文件格式），将抛出相应的异常。根据具体实现细节，该方法可能返回匹配项的位置信息（例如工作表名称、单元格坐标等）。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------|------|-----------------------------|------|
| name | string | Path | 工作簿文件的名称。 |
| folder | string | Query | 工作簿所在的文件夹路径。 |
| storageName | string | Query | （可选）若使用自定义云存储，则指定其名称；若省略，则使用默认存储。 |
| region | string | Query | 电子表格区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`）。影响数字格式化、日期解析以及区域特定行为。 |
| password | string | Query | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| [待定] | | [待定] |

### **响应**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | 成功 | 请求成功，响应中包含电子表格中找到的所有文本项。 |
| 400 | 请求错误 | URL 或请求参数无效。 |
| 401 | 未授权 | 身份验证失败，或未提供凭据。 |
| 404 | 未找到 | 源文件不可访问。 |
| 413 | 请求实体过大 | 请求负载超出允许大小。 |
| 500 | 服务器内部错误 | 电子表格在获取数据时发生异常。 |

## 如何结合 SDK 使用 SearchAllTextItemsInRemoteSpreadsheet 方法

### SearchAllTextItemsInRemoteSpreadsheet 规范

[SearchAllTextItemsInRemoteSpreadsheet API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Sheet1",
      "CellAddress": "A1",
      "Text": "示例文本"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，使您能够专注于项目任务本身。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[待定]`
---