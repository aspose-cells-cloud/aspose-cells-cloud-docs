---
title: "将 CSV 数据导入电子表格"
ArticleTitle: "将 CSV 数据导入电子表格 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "docs"
url: /zh/cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, CSV 导入, 电子表格, API"
description: "使用 Aspose.Cells Cloud API 将 CSV 数据文件导入本地电子表格。"
weight: 100
---

## Aspose.Cells Cloud Web 服务的将 CSV 数据导入电子表格功能

将 CSV 数据文件导入本地电子表格。该方法解析 CSV 文件，将数据映射到电子表格的单元格结构中，并将结果文件保存到本地。支持的电子表格格式包括 .xlsx 和 .ods。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称             | 类型     | 路径/查询字符串/HTTP 正文 | 描述                                                                 |
|----------------------|----------|---------------------------|----------------------------------------------------------------------|
| datafile             | 文件     | FormData                  | 上传数据文件。                                                       |
| Spreadsheet          | 文件     | FormData                  | 上传电子表格文件。                                                   |
| worksheet            | 字符串   | 查询字符串                | 需要将 CSV 数据导入的工作表。（必填）                               |
| startcell            | 字符串   | 查询字符串                | 数据导入的起始位置。（必填）                                         |
| insert               | 布尔值   | 查询字符串                | 控制插入行为。true：插入数据；false：覆盖现有数据。默认值：true（可选） |
| convertNumericData   | 布尔值   | 查询字符串                | 是否将文本文件中的字符串转换为数值数据。默认值：true（可选）         |
| splitter             | 字符串   | 查询字符串                | 用于拆分 CSV 字段的分隔符。默认值：","（可选）                        |
| outPath              | 字符串   | 查询字符串                | （可选）工作簿存储的文件夹路径。默认为 null（可选）                  |
| outStorageName       | 字符串   | 查询字符串                | 输出文件的存储名称。（可选）                                         |
| fontsLocation        | 字符串   | 查询字符串                | 使用自定义字体。（可选）                                             |
| region               | 字符串   | 查询字符串                | 电子表格区域/语言设置（例如：`zh-CN`、`en-US`、`fr-FR`）。影响数字格式化、日期解析和区域特定行为。（可选） |
| password             | 字符串   | 查询字符串                | 打开电子表格文件所需的密码。（可选）                                 |

### 请求正文参数

| 参数名称 | 类型 | 描述 |
| -------- | ---- | ---- |
| [待定]   | [待定] | [待定] |

### **响应**

```json
{
  "file": "<生成的电子表格的二进制流>"
}
```

**响应状态码**

| 状态码 | 含义           | 描述                                     |
|--------|----------------|------------------------------------------|
| 200    | 成功 (OK)      | CSV 数据导入成功，并返回生成的电子表格文件。 |
| 400    | 请求错误 (Bad Request) | 请求参数无效或 URL 格式错误。             |
| 401    | 未授权 (Unauthorized) | 身份验证失败，或未提供凭据。              |
| 404    | 未找到 (Not Found) | 源文件无法访问。                         |
| 413    | 载荷过大 (Payload Too Large) | 上传的文件超出允许的大小限制。           |
| 500    | 内部服务器错误 (Internal Server Error) | 电子表格在获取数据时发生异常。           |

## 如何使用 SDK 导入 CSV 数据到电子表格

### 导入 CSV 数据到电子表格的规范说明

[导入 CSV 数据到电子表格 API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) 定义了一个公开可访问的编程接口，使您能够直接通过 Web 浏览器执行 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以确保连接安全
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<生成的电子表格的二进制流>"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 代码仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose Cells Cloud Web 服务：
`[待定]`
---