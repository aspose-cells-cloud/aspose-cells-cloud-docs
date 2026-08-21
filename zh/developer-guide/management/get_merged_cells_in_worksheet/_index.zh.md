---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "获取工作表中的合并单元格 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "GetMergedCellsInWorksheet"
type: docs
url: /zh/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, 合并单元格, 工作表, API"
description: "从本地电子表格工作表中获取所有合并单元格区域。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务的“获取工作表中的合并单元格”功能

从本地电子表格工作表中获取所有合并单元格区域。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名 | 类型 | 路径/查询字符串/HTTP 正文 | 描述 |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | 文件 | FormData | 上传电子表格文件。 |
| worksheet | 字符串 | 查询 | 工作表名称。 |
| region | 字符串 | 查询 | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。 |
| password | 字符串 | 查询 | 打开电子表格文件所需的密码。 |

### 请求正文参数

| 参数名 | 类型 | 描述 |
| -------------- | ---- | ----------- |
| N/A | N/A | 此操作不接受 JSON 正文；电子表格文件通过 `multipart/form-data` 发送。 |

### **响应**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|------|---------|-------------|
| 200 | OK（成功） | 成功获取合并单元格区域。 |
| 400 | Bad Request（错误请求） | 一个或多个请求参数无效或缺失。 |
| 401 | Unauthorized（未授权） | 身份验证失败 — JWT 令牌无效或缺失。 |
| 413 | Payload Too Large（载荷过大） | 上传的电子表格超出允许的大小限制。 |
| 500 | Internal Server Error（服务器内部错误） | 服务器发生意外错误。 |

## 如何使用 SDK 调用“获取工作表中的合并单元格”功能

### “获取工作表中的合并单元格”规范说明

[“获取工作表中的合并单元格”API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=zh-CN&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
 `[TBD]`
---