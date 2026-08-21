---
title: "将 Excel 转换为 Markdown"
second_title: "文档"
linktitle: "Excel 转 Markdown"
type: docs
url: /zh/convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, 转换, Aspose.Cells Cloud, REST API, Excel 转 Markdown, Aspose Cells Markdown API, Excel 导出为 Markdown"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 工作表转换为 Markdown 格式——包含 cURL 示例、SDK 代码片段、所需参数及身份验证详情。"
weight: 100
ArticleTitle: "将 Excel 转换为 Markdown – Aspose.Cells Cloud API 文档"
---

此 REST API 可将电子表格文件转换为 Markdown 格式文件。

## 安全与身份验证
Aspose.Cells Cloud API 采用安全机制，需要使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

### 查询参数


| 参数名称              | 类型   | 位置   | 描述                                                                                     |
| --------------------- | ------ | ------ | ---------------------------------------------------------------------------------------- |
| password              | string | query  | 打开 Excel 文件所需的密码。                                                              |
| storageName           | string | query  | 文件所在的存储空间名称。                                                                 |
| checkExcelRestriction | bool   | query  | 指定在修改单元格或相关对象时是否强制执行 Excel 特定限制。                               |
| datafile              | file   | body   | 作为 multipart 内容第一部分上传的 Excel 文件。                                          |

### 响应

API 返回一个类型为 **FileInfo** 的 JSON 对象：

- **FileInfo** —— 包含生成的 Markdown 文件的文件名、大小及 base64 编码内容的对象。

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### 错误响应

| HTTP 状态码 | 描述                                   | 示例 JSON 请求体                                |
| ----------- | -------------------------------------- | ----------------------------------------------- |
| 401         | 未授权——缺少或无效的令牌。             | `{"error":"Invalid access token."}`             |
| 400         | 请求错误——缺少必需参数或文件格式无效。 | `{"error":"The 'datafile' field is required."}` |
| 500         | 服务器内部错误——意外的服务器问题。     | `{"error":"An unexpected error occurred."}`     |



## 如何使用 PostConvertWorkbookToMarkdown API（配合 SDK）

### PostConvertWorkbookToMarkdown API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) 定义了一个公开可访问的编程接口，允许您直接通过 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的方式。SDK 会处理底层细节，使您能专注于业务逻辑。请参阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 实现此功能的其他 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** —— 将 Excel 文件另存为 HTML，并附带额外设置，结果将被存储。
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** —— 将 Excel 文件转换为 HTML，并附带额外选项，结果返回至响应体中。
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** —— 获取 Excel 文件，并可选地将其转换为 HTML。