---
title: "在远程工作表中搜索断开的链接"
ArticleTitle: "在远程工作表中搜索断开的链接 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "docs"
url: /zh/cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, 搜索断开的链接, 远程工作表"
description: "搜索远程电子表格中工作表内的断开链接。"
weight: 100
---

## Aspose.Cells Cloud Web 服务中的在远程工作表中搜索断开的链接

该方法用于搜索存储于远程云存储中的电子表格文件中某个工作表内的断开链接。它会扫描所有工作表和单元格，以识别不再指向有效目标的超链接，例如失效的 URL 或缺失的外部引用。整个操作在云环境中远程执行，无需将文件下载到本地机器。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需通过 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------|------|----------------------------|------|
| name | string | Path | 要搜索的电子表格文件名称。 |
| worksheet | string | Path | 指定要进行查找的工作表名称。 |
| folder | string | Query | 存储电子表格的文件夹路径。（可选） |
| storageName | string | Query | （可选）若使用自定义云存储，则指定其名称；省略时使用默认存储。 |
| region | string | Query | 电子表格的区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`）。影响数字格式、日期解析及区域特定行为。 |
| password | string | Query | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| — | — | 本操作无需请求体。 |

### **响应**

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | OK | 成功获取断开链接的列表。 |
| 400 | Bad Request | 请求参数无效或 URL 格式错误。 |
| 401 | Unauthorized | 身份验证失败或未提供凭据。 |
| 404 | Not Found | 源文件不可访问。 |
| 413 | Payload Too Large | 请求实体过大。 |
| 500 | Internal Server Error | 电子表格在获取数据时发生异常。 |

## 如何使用 SDK 在远程工作表中搜索断开的链接

### 在远程工作表中搜索断开的链接规范

[在远程工作表中搜索断开的链接 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`