---
title: "将 Excel 转换为 PDF — Aspose.Cells Cloud API"
ArticleTitle: "将 Excel 转换为 PDF — Aspose.Cells Cloud API"
second_title: "文档"
linktype: "docs"
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, 转换, 云 API"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 Excel 工作簿转换为 PDF。包含 cURL 示例、SDK 示例（C#、Java、Python）以及身份验证指南。"
weight: 80
---

此 REST API 可将电子表格文件转换为 PDF 格式文件。**前提条件：** 获取有效的 JWT 访问令牌，确保源 Excel 文件已存储在受支持的存储中，并具备调用转换端点的相应权限。

## PostConvertWorkbookToPDF API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **查询参数**

| 参数名称              | 类型   | 描述                                                             |
| :-------------------- | :----- | :--------------------------------------------------------------- |
| password              | string | 打开 Excel 文件所需的密码。                                       |
| storageName           | string | 文件所在的存储名称。                                             |
| checkExcelRestriction | bool   | 在修改单元格相关对象时是否强制执行 Excel 文件限制。             |

若省略 `checkExcelRestriction`，其默认值为 `false`。

### **请求体参数**

| 参数名称 | 类型 | 描述                                             |
| :------- | :--- | :----------------------------------------------- |
| datafile | file | 作为多部分内容的第一部分上传的数据文件。         |

### **响应**

[FileInfo](/cells/file-info/)

响应返回一个包含文件元数据的 JSON 对象。PDF 文件本身可通过提供的 `FileContent`（Base64 编码字符串）或 `FileInfo` 链接下载。API 返回类型为 **FileInfo** 的 JSON 对象：

- **FileInfo** —— 包含生成的 **PDF** 文件的文件名、大小及 Base64 编码内容的对象。

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 过滤器成功应用；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺失或无效的参数（例如不支持的文件类型）。     |
| 401    | Unauthorized（未授权） | 无效或缺失的 JWT 令牌。                         |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                      |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                         |

## 如何使用 SDK 调用 PostConvertWorkbookToPDF API

### PostConvertWorkbookToPDF API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) 定义了一个公开可访问的编程接口，可让您直接从网页浏览器执行 REST 交互。

**请求头**

| 请求头        | 类型   | 描述                                           |
| :------------ | :----- | :--------------------------------------------- |
| Authorization | string | 通过 JWT 身份验证获取的 Bearer 令牌。           |
| Content-Type  | string | 文件上传时必须为 `multipart/form-data`。       |
| Accept        | string | 接收响应元数据时为 `application/json`。        |

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells 网络服务。在 `Authorization` 请求头中包含访问令牌，然后运行以下请求：

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可以简化开发流程，屏蔽底层细节。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，了解 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells 网络服务：
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 实现相同功能的其他 API

| **API**        | **类型** | **描述**                                                     | **Swagger 链接**                                                                            |
| :------------- | :------- | :----------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT      | 将请求体中的工作簿转换为指定格式。                          | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API 可将 MS Excel 文件另存为 PDF，并支持额外设置，同时将结果存储在云存储中。

此 REST API 可将 Excel 文件转换为 PDF。

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API 可将 MS Excel 文件转换为 PDF，并支持额外设置，同时将结果以响应体返回。

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API 可将 MS Excel 文件转换为 PDF，并支持额外设置，同时将结果以响应体返回。

上述 [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)、[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) 和 [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API 定义了一个公开可访问的编程接口，允许您直接从网页浏览器执行 REST 交互。

如需了解其他转换选项，请参阅 [保存选项](/cells/save-options/) 页面。