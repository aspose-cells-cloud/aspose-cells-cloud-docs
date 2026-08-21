---
title: "将 XML 数据导入电子表格"
ArticleTitle: "将 XML 数据导入电子表格 – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "将 XML 数据导入电子表格"
type: docs
url: /zh/cells/import/data/xml
aliases: []
keywords: "导入 XML, Aspose.Cells, API"
description: "使用 Aspose.Cells Cloud 将 XML 数据文件导入本地电子表格。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务的将 XML 数据导入电子表格功能

使用 Aspose.Cells Cloud 将 XML 数据文件导入本地电子表格。该方法解析 XML，将数据映射到电子表格的单元格结构，并将文件保存至本地。支持的电子表格格式包括 .xlsx 和 .ods。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **安全与身份验证**

Aspose.Cells Cloud API 安全可靠，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                   |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile         | 文件    | FormData                    | 上传数据文件。                                                                                                                         |
| Spreadsheet      | 文件    | FormData                    | 上传电子表格文件。                                                                                                                     |
| worksheet        | 字符串  | 查询参数                    | 需要将 XML 数据导入的工作表名称。                                                                                                      |
| startcell        | 字符串  | 查询参数                    | 数据导入的起始位置。                                                                                                                   |
| insert           | 布尔值  | 查询参数                    | 控制插入行为：true 表示插入数据；false 表示覆盖已有数据。默认值：**true**                                                             |
| outPath          | 字符串  | 查询参数                    | （可选）工作簿保存的文件夹路径。默认为 null。                                                                                         |
| outStorageName   | 字符串  | 查询参数                    | 输出文件的存储名称。                                                                                                                   |
| fontsLocation    | 字符串  | 查询参数                    | 使用自定义字体。                                                                                                                       |
| region           | 字符串  | 查询参数                    | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。                                              |
| password         | 字符串  | 查询参数                    | 打开电子表格文件所需的密码。                                                                                                           |

### 请求体参数

| 参数名称 | 类型 | 描述 |
|----------|------|------|
| *无*     | -    | -    |

### **响应**

```json
{
  "file": "<更新后的电子表格的二进制流>"
}
```

**响应状态码**

| 状态码 | 含义              | 描述                                                                                     |
|--------|-------------------|------------------------------------------------------------------------------------------|
| 200    | 成功 (OK)         | XML 数据导入成功，并返回已更新的电子表格文件。                                           |
| 400    | 请求错误 (Bad Request) | 请求 URL 无效或缺少必需参数。                                                            |
| 401    | 未授权 (Unauthorized)  | 身份验证失败，或未提供凭据。                                                             |
| 404    | 未找到 (Not Found)     | 源文件不可访问。                                                                         |
| 413    | 请求实体过大 (Payload Too Large) | 上传文件大小超出允许限制。                                                              |
| 500    | 内部服务器错误 (Internal Server Error) | 电子表格在获取数据时发生异常。                                                          |

## 如何使用 SDK 调用将 XML 数据导入电子表格功能

### 将 XML 数据导入电子表格 API 规范

[将 XML 数据导入电子表格 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器发起 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API：

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<更新后的电子表格的二进制流>"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最快方式。SDK 封装了底层细节，让您专注于项目任务本身。请查看 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[待定]`
---