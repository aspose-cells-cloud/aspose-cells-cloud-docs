---
title: "Excel 转 Docx"
second_title: "文档"
linktitle: "Excel 转 Docx"
type: docs
url: convert-excel-file-to-docx-file/
keywords: "Excel 转 Docx 转换、Aspose.Cells Cloud、REST API、电子表格转换、文档生成"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 电子表格转换为 DOCX 文档。支持多种 SDK 和编程语言，实现无缝集成。"
weight: 90
---

该 REST API 可将电子表格文件转换为 DOCX 格式文件。

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

**查询参数**

| 参数名称              | 类型   | 描述                                                                 |
| --------------------- | ------ | -------------------------------------------------------------------- |
| password              | string | 打开 Excel 文件所需的密码。                                          |
| storageName           | string | 文件所在的存储空间名称。                                             |
| checkExcelRestriction | bool   | 指示用户修改单元格相关对象时是否检查 Excel 文件的限制。             |

**请求体参数**

| 参数名称 | 类型      | 描述                                     |
| -------- | --------- | ---------------------------------------- |
| datafile | data file | 多部分请求体第一部分中保存的数据文件。   |

**响应**

API 返回一个 **FileInfo** 对象，其中包含生成的 Word 文件。

| 字段            | 类型   | 描述                              |
| --------------- | ------ | --------------------------------- |
| **Filename**    | string | Word 文件的名称（例如：`example.docx`）。 |
| **FileSize**    | int    | 文件大小（单位：字节）。          |
| **FileContent** | string | Word 文件内容的 Base64 编码字符串。 |

[FileInfo](/cells/file-info/)

**HTTP 状态码**

| 状态码 | 含义            | 描述                                       |
|--------|-----------------|--------------------------------------------|
| 200    | OK（成功）      | 筛选器应用成功；响应包含操作详细信息。     |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如：不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                      |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超出大小限制。                 |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                    |

## 如何使用 SDK 调用 PostConvertWorkbookToDocx API

### PostConvertWorkbookToDocx API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) 定义了一个公开可访问的编程接口，允许您直接从网页浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.docx",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 实现此功能的其他 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 将 Excel 文件另存为 DOCX 文件，并支持额外设置，结果存储于指定存储空间中。

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 将 Excel 文件转换为 DOCX 文件，支持可选设置，并将结果返回于响应中。

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – 获取 Excel 工作簿，并根据可选参数将其转换为 DOCX 文件。

---