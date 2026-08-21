---
title: "Excel 转 CSV"
second: "文档"
linktitle: "Excel 转 CSV"
type: docs
url: convert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel 转 CSV、Aspose.Cells Cloud、REST API、电子表格转换、CSV 文件、文件转换"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 电子表格转换为 CSV 格式。支持多种 SDK 和编程语言，便于集成。"
weight: 90
---

该 REST API 可将电子表格文件转换为 CSV 格式文件。

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 查询参数

| 参数名称                | 类型   | 描述                                                         |
| ----------------------- | ------ | ------------------------------------------------------------ |
| `password`              | string | 打开 Excel 文件所需的密码。                                   |
| `storageName`           | string | 文件所在的存储名称。                                          |
| `checkExcelRestriction` | bool   | 用户修改单元格相关对象时，是否检查 Excel 文件限制。          |

### 请求体参数

| 参数名称 | 类型      | 描述                                         |
| -------- | --------- | -------------------------------------------- |
| `datafile` | 数据文件 | 多部分请求体第一部分中包含的数据文件。        |

### 响应

API 返回一个 **FileInfo** 对象，其中包含生成的 CSV 文件。

| 字段            | 类型   | 描述                                 |
| --------------- | ------ | ------------------------------------ |
| **Filename**    | string | CSV 文件名称（例如 `example.csv`）。 |
| **FileSize**    | int    | 文件大小（以字节为单位）。           |
| **FileContent** | string | CSV 文件的 Base64 编码内容。         |

[FileInfo](/cells/file-info/)

**HTTP 状态码**

| 状态码 | 含义             | 描述                                             |
| ------ | ---------------- | ------------------------------------------------ |
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。               |
| 400    | Bad Request（错误请求） | 缺少或无效参数（例如不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                             |
| 413    | Payload Too Large（请求实体过大） | 上传的文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 服务器发生意外错误。                             |

## 如何使用 SDK 调用 PostConvertWorkbookToCSV API

### PostConvertWorkbookToCSV API 规范

[OpenAPI 规范](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) 定义了一个公开可访问的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

您可以使用 **cURL** 命令行工具访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发速度最快的途径。SDK 处理底层细节，让您专注于项目本身。查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

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