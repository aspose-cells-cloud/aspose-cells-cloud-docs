---
title: "拆分表格"
ArticleTitle: "拆分表格 – Aspose.Cells Cloud API"
second_title: "文档"
linktype: "docs"
url: "/cells/split/table"
aliases: []
keywords: "Aspose.Cells, 拆分表格, API"
description: "通过列值拆分电子表格中表格的 API。"
weight: 1
---

## Aspose.Cells Cloud Web 服务的 SplitTable 方法

此方法根据指定列中的不同值对源表格进行拆分操作，将行按这些唯一值分组。每个数据组（对应一个唯一的拆分值）将作为独立的数据单元进行处理。导出目标由两个关键布尔参数控制：

- 控制工作簿结构：若为 `true`，则每个拆分单元保存为一个独立的工作簿文件；若为 `false`，则每个单元成为当前工作簿中的新工作表。
- 控制输出打包方式：当设为 `true` 并与 `toNewWorkbook` = `true` 配合使用时，该方法会生成多个独立文件，并以 ZIP 压缩包形式返回；若为 `false`，则将所有数据整合到单个文件中（可能是多工作表工作簿或根据其他设置生成的单文件）。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **安全与认证**

Aspose.Cells Cloud API 具备安全性，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型    | 路径/查询字符串/HTTP 请求体 | 描述                                                                                              |
|------------------|---------|----------------------------|---------------------------------------------------------------------------------------------------|
| Spreadsheet      | 文件    | FormData                   | 上传电子表格文件。                                                                                |
| worksheet        | 字符串  | 查询字符串                 | 包含目标表格的工作表。                                                                            |
| tableName        | 字符串  | 查询字符串                 | 需要拆分的数据表格。                                                                              |
| splitColumnName  | 字符串  | 查询字符串                 | 用于拆分的列名。                                                                                  |
| saveSplitColumn  | 布尔值  | 查询字符串                 | 是否保留拆分列中的数据。                                                                          |
| splitRowNumber   | 整数    | 查询字符串                 | [待定]                                                                                             |
| toNewWorkbook    | 布尔值  | 查询字符串                 | 导出目标控制：true — 创建包含拆分数据的新工作簿文件；false — 在当前工作簿中新增工作表。           |
| toMultipleFiles  | 布尔值  | 查询字符串                 | true — 将表格数据导出为 **多个独立文件**（以 ZIP 压缩包形式返回）；false — 所有数据存储于 **单个文件**（含多工作表）。默认值：false。 |
| outPath          | 字符串  | 查询字符串                 | （可选）工作簿保存的目标文件夹路径。默认为 null。                                                 |
| outStorageName   | 字符串  | 查询字符串                 | 输出文件的存储名称。                                                                              |
| fontsLocation    | 字符串  | 查询字符串                 | 使用自定义字体。                                                                                  |
| region           | 字符串  | 查询字符串                 | 电子表格区域/语言设置（例如 `zh-CN`、`fr-FR`）。影响数字格式化、日期解析及区域特定行为。          |
| password         | 字符串  | 查询字符串                 | 打开电子表格文件所需的密码。                                                                      |

### 请求体参数

| 参数名称   | 类型 | 描述             |
| ---------- | ---- | ---------------- |
| Spreadsheet | 文件 | 上传电子表格文件。 |

### **响应**

```json
{
  "file": "二进制流（根据参数不同为 ZIP 压缩包或工作簿）"
}
```

**响应状态码**

| 状态码 | 含义            | 描述                                       |
|--------|-----------------|--------------------------------------------|
| 200    | OK（成功）      | 拆分操作完成。响应中包含生成的文件（ZIP 压缩包或工作簿）。 |
| 400    | Bad Request（错误请求） | URL 或请求参数无效。                       |
| 401    | Unauthorized（未授权） | 认证失败或未提供凭据。                     |
| 404    | Not Found（未找到） | 源文件不可访问。                           |
| 413    | Payload Too Large（请求体过大） | 请求体大小超过限制。                     |
| 500    | Internal Server Error（内部服务器错误） | 电子表格在获取数据时发生异常。         |

## 如何通过 SDK 使用 SplitTable

### SplitTable 规范

[SplitTable API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何通过 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
# 使用 HTTPS 以确保安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "二进制流（根据参数不同为 ZIP 压缩包或工作簿）"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最快方式。SDK 封装了底层细节，使您能够专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Cloud Web 服务：
`[待定]`