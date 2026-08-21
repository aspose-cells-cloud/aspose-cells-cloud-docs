---
title: "将表格转换为 PDF"
ArticleTitle: "将表格转换为 PDF – Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "将表格转换为 PDF"
type: docs
url: /cells/convert/table/pdf
aliases: []
keywords: "将表格转换为 PDF, Aspose.Cells, API"
description: "使用 Aspose.Cells Cloud 将本地磁盘上的电子表格中的表格转换为 PDF 文件。"
weight: 1000
---

## Aspose.Cells Cloud Web 服务的表格转 PDF 功能

此操作从本地文件系统读取电子表格文件，将其指定的表格转换为 PDF 文档，并返回转换后的结果。整个过程完全在云端服务器上执行，因此无需先将文件上传至云存储。API 支持可选参数，包括输出位置、自定义字体、自动调整行/列宽、区域设置以及密码保护的工作簿。

### Web API 端点

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                                                                                                     |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | 文件   | FormData                    | 上传电子表格文件。                                                                                                                                         |
| worksheet        | 字符串 | 查询字符串                  | 电子表格的工作表名称。                                                                                                                                  |
| tableName        | 字符串 | 查询字符串                  | 表格名称。                                                                                                                                                      |
| outPath          | 字符串 | 查询字符串                  | （可选）工作簿保存的文件夹路径。默认为 null。                                                                                  |
| outStorageName   | 字符串 | 查询字符串                  | 输出文件的存储名称。                                                                                                                                       |
| fontsLocation    | 字符串 | 查询字符串                  | 使用自定义字体。                                                                                                                                               |
| AutoRowsFit      | 布尔值 | 查询字符串                  | （可选）自动调整工作表中所有行高。                                                                                                                    |
| AutoColumnsFit   | 布尔值 | 查询字符串                  | （可选）自动调整工作表中所有列宽。                                                                                                                 |
| region           | 字符串 | 查询字符串                  | 电子表格的区域/语言设置（例如 `zh-CN`、`en-US`、`fr-FR`）。影响数字格式化、日期解析以及区域特定行为。                         |
| password         | 字符串 | 查询字符串                  | 打开电子表格文件所需的密码。                                                                                                                      |

### 请求体参数

| 参数名称 | 类型 | 描述 |
|----------|------|------|
| *无*     | *无* | *无需 JSON 请求体；文件通过 multipart/form-data 方式发送。* |

### **响应**

```json
{
  "file": "<二进制 PDF 内容>"
}
```

**响应状态码**

| 状态码 | 含义         | 描述 |
|--------|--------------|------|
| 200    | 成功 (OK)    | 表格已成功转换为 PDF；响应体包含 PDF 文件流。 |
| 400    | 错误请求 (Bad Request) | 请求参数无效或 URL 格式错误。 |
| 401    | 未授权 (Unauthorized) | 身份验证失败或未提供凭据。 |
| 404    | 未找到 (Not Found) | 源文件不可访问，或工作表/表格未找到。 |
| 413    | 请求实体过大 (Payload Too Large) | 上传的电子表格超过允许的大小限制。 |
| 500    | 内部服务器错误 (Internal Server Error) | 转换电子表格为 PDF 时发生错误。 |

## 如何使用 SDK 实现表格转 PDF 功能

### 表格转 PDF 规范

[表格转 PDF API 规范](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 调用。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Cloud Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}

{< tab tabNum="1" >}

```bash
# 使用 HTTPS 以建立安全连接
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<二进制 PDF 内容>"
}
```

{< /tab >}

{< /tabs >}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最快方式。SDK 抽象了底层细节，让您能够专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Cloud Web 服务：

```csharp
// C# SDK 示例代码
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Java SDK 示例代码
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Python SDK 示例代码
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`