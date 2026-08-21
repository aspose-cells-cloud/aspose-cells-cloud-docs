---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "获取远程工作表中的合并单元格 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "获取远程工作表中的合并单元格"
type: docs
url: /zh/cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, 获取合并单元格, 远程工作表, API"
description: "从电子表格中的远程工作表获取所有合并单元格区域。"
weight: 10
---

## Aspose.Cells Cloud Web 服务的 GetMergedCellsInRemotedWorksheet

从远程电子表格工作表中获取所有合并单元格区域。

### Web API 端点

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称 | 类型 | 路径/查询字符串/HTTP 请求体 | 描述 |
|----------|------|----------------------------|------|
| name | string | 路径 | 电子表格文件名 |
| worksheet | string | 路径 | 工作表名称 |
| folder | string | 查询 | 电子表格在云存储中的路径。 |
| storageName | string | 查询 | （可选）若使用自定义云存储，则指定其名称；省略则使用默认存储。 |
| region | string | 查询 | 电子表格的区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`），影响数字格式化、日期解析及本地化行为。 |
| password | string | 查询 | 打开电子表格文件所需的密码。 |

### 请求体参数

| 参数名称 | 类型 | 描述 |
|----------|------|------|
| — | — | *无* |

### **响应**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**响应状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | 成功 | 请求成功，返回合并单元格区域列表。 |
| 400 | 请求错误 | URL 无效或请求参数格式错误。 |
| 401 | 未授权 | 身份验证失败，或未提供凭据。 |
| 413 | 请求实体过大 | 请求体超出允许的最大尺寸。 |
| 500 | 服务器内部错误 | 电子表格在获取数据时发生异常。 |

## 如何结合 SDK 使用 GetMergedCellsInRemotedWorksheet

### GetMergedCellsInRemotedWorksheet 规范

[GetMergedCellsInRemotedWorksheet API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) 定义了公开可访问的编程接口，使您能直接通过 Web 浏览器执行 REST 交互。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API：

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 保证连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加快开发速度的最快方式。SDK 封装了底层细节，让您专注于项目核心任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose Cells Cloud Web 服务：
`[TBD]`