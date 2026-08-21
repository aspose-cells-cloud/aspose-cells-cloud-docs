---
title: "Excel 转 PNG"
second_title: "文档"
linktitle: "Excel 转 PNG"
type: docs
url: /zhconvert-excel-file-to-png-file/
keywords: "Excel 转 PNG, Aspose.Cells Cloud, REST API, 电子表格转换, PNG 格式"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 电子表格转换为 PNG 图像。支持多种 SDK，并提供多种编程语言的详细示例。"
weight: 90
---

此 REST API 可将电子表格文件转换为 PNG 格式。

## REST API 规范

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **安全与认证**

Aspose.Cells Cloud API 采用安全机制，需使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的认证</a>。

### **查询参数**

| 参数名称              | 类型   | 描述                                                         |
| --------------------- | ------ | ------------------------------------------------------------ |
| password              | string | 打开 Excel 文件所需的密码。                                  |
| storageName           | string | 文件所在的存储名称。                                         |
| checkExcelRestriction | bool   | 指定在修改单元格或相关对象时是否检查 Excel 文件限制。       |

### **请求体参数**

| 参数名称 | 类型      | 描述                                     |
| -------- | --------- | ---------------------------------------- |
| datafile | data file | multipart 请求第一部分中包含的电子表格文件。 |

### **响应**

API 返回一个 **FileInfo** 对象，其中包含生成的 PNG 文件。

| 字段            | 类型   | 描述                             |
| --------------- | ------ | -------------------------------- |
| **Filename**    | string | PNG 文件名（例如 `example.png`）。 |
| **FileSize**    | int    | 文件大小（单位：字节）。         |
| **FileContent** | string | PNG 文件的 Base64 编码内容。     |

[FileInfo](/cells/file-info/)


**HTTP 状态码**

| 状态码 | 含义            | 描述                                     |
|--------|-----------------|------------------------------------------|
| 200    | OK（请求成功）  | 过滤器应用成功；响应包含操作详细信息。   |
| 400    | Bad Request（请求错误） | 缺失或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                     |
| 413    | Payload Too Large（请求体过大） | 上传的文件超出大小限制。                 |
| 500    | Internal Server Error（服务器内部错误） | 意外的服务器错误。                       |

## 如何使用 SDK 调用 PostConvertWorkbookToPNG API

### PostConvertWorkbookToPNG API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) 定义了一个公开可访问的编程接口，可让您直接从网页浏览器发起 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells 网络服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 [GitHub 仓库](https://github.com/aspose-cells-cloud) 获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells 网络服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## 实现类似功能的其他 API

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – 将 Excel 文件保存为 CSV（或其他格式），支持额外设置并存储结果。
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – 将 Excel 文件转换为 CSV（或其他格式），支持可选参数，并在响应中返回结果。
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – 获取 Excel 文件，并可动态将其转换为 CSV（或其他格式）。