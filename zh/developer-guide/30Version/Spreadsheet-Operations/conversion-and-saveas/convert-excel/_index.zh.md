---
title: "将 Excel 文件转换为不同格式"
ArticleTitle: "将 Excel 文件转换为不同格式"
second_title: "文档"
linktype: "convert-excel"
type: docs
url: /convert-an-excel-file-to-different-formats/
aliases:
  [
    "/convert-excel-workbook-to-different-file-formats/",
    "/convert/excel-to-different-formats/",
  ]
keywords: "Aspose.Cells Cloud、Excel 转换、文件格式转换、REST API、SDK、CSV、PDF、HTML、JSON、Markdown"
description: "使用 Aspose.Cells Cloud REST API 将 Excel 工作簿转换为 CSV、PDF、HTML、JSON、Markdown 等多种格式。"
weight: 10
---

调用此接口前，请确保已获取有效的 JWT 令牌，并将源工作簿存储在受支持的存储位置（例如 Aspose Cloud 存储）。请将令牌置于 `Authorization` 请求头中；如有需要，还需指定 `storageName` 查询参数。

此 REST API 可将 Excel 文件转换为多种输出格式。

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

该请求为 HTTP **PUT** 请求，内容类型为 multipart（参见 [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) 或 [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。  
multipart 主体的第一部分包含**数据文件**，第二部分包含**保存选项**。

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 查询参数

| 参数名称                | 类型   | 描述                                                                 |
| ----------------------- | ------ | -------------------------------------------------------------------- |
| `format`                | string | 目标文件格式（例如：CSV、XLS、HTML、PDF、XML、TXT、TIFF、PNG、JPG、GIF、EMF、BMP、MD、Numbers、WMF、SVG 等）。 |
| `password`              | string | 打开源 Excel 文件所需的密码。                                        |
| `outPath`               | string | 单个输出文件的完整路径（含文件名及扩展名），或生成多个文件时的文件夹路径。 |
| `storageName`           | string | 源文件所在的存储名称。                                               |
| `checkExcelRestriction` | bool   | 若为 **true**，则在修改单元格或相关对象前验证 Excel 限制条件。       |
| `streamFormat`          | string | 输入文件流的格式。                                                   |
| `region`                | string | 应用于工作簿的区域设置。                                             |
| `pageWideFitOnPerSheet` | bool   | 转换为 PDF 时，按工作表调整页面宽度以适应内容。                      |
| `pageTallFitOnPerSheet` | bool   | 转换为 PDF 时，按工作表调整页面高度以适应内容。                      |
| `sheetName`             | string | 待转换的工作表名称。                                                 |
| `pageIndex`             | string | 待转换页面的索引（需配合 `sheetName` 使用）。                        |
| `onePagePerSheet`       | bool   | 若为 **true**，则每张工作表生成一页 PDF。                            |
| `AutoRowsFit`           | bool   | 自动调整工作簿中所有行高。                                           |
| `AutoColumnsFit`        | bool   | 自动调整工作簿中所有列宽。                                           |

### 请求体参数

| 参数名称   | 类型      | 描述                                 |
| ---------- | --------- | ------------------------------------ |
| `datafile` | data file | 放置于 multipart 主体第一部分的 Excel 文件。 |
| `SaveOptions` | object | 放置于 multipart 主体第二部分的保存选项。 |

### **响应**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP 状态码**

| 状态码 | 含义              | 描述                                               |
|--------|-------------------|----------------------------------------------------|
| 200    | OK（成功）        | 筛选操作成功；响应包含操作详情。                   |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如：不支持的文件类型）。         |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。                               |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。                            |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                             |

## 如何结合 SDK 使用 PutConvertWorkBook API

### PutConvertWorkBook API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) 定义了一个公开可访问的接口，允许直接从 Web 浏览器发起 REST 调用。

### cURL 示例

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可加速开发进程，其自动处理底层细节，让您专注于业务逻辑。完整的 Aspose.Cells Cloud SDK 列表请参见 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}