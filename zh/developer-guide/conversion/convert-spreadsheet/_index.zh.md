---
title: "Aspose.Cells Cloud Web API — 将电子表格转换为其他格式的免费在线工具"
second title: "文档"
articleTitle: "如何将电子表格转换为其他格式：分步指南"
linkTitle: "转换电子表格"
type: docs
url: /zh/convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, 电子表格转换, Excel 转 PDF, Excel API, 云端文件转换"
description: "使用 Aspose.Cells Cloud API 将电子表格文件转换为其他格式。"
weight: 100
---

使用 Aspose.Cells Cloud Web API 将本地电子表格/Excel 文件转换为其他格式。

## **电子表格转换 API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### **请求参数**

| 参数名称         | 类型   | 路径/查询字符串/HTTP 请求体 | 描述                                                                 |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------- |
| Spreadsheet    | 文件   | FormData                   | 上传需转换的电子表格文件。                                           |
| format         | 字符串 | 查询字符串                  | （必需）期望的输出格式（例如：“XLSX”、“PDF”、“CSV”）。               |
| outPath        | 字符串 | 查询字符串                  | （可选）存放转换后工作簿的文件夹路径，默认为 null。                  |
| outStorageName | 字符串 | 查询字符串                  | 指定输出文件的存储名称。                                             |
| fontsLocation  | 字符串 | 查询字符串                  | 为电子表格指定自定义字体路径。                                       |
| region         | 字符串 | 查询字符串                  | 指定电子表格的区域设置。                                             |
| password       | 字符串 | 查询字符串                  | 如果电子表格受密码保护，则提供解密密码。                             |

### **响应**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**成功状态码**

- **200 OK** – 转换成功，响应体包含转换后的文件流。
- `Content-Type` 响应头反映所请求输出格式的 MIME 类型（例如，PDF 格式为 `application/pdf`）。

**HTTP 状态码**

| 状态码 | 含义               | 描述                                                 |
| ---- | ------------------- | ---------------------------------------------------- |
| 200  | OK（成功）          | 操作成功；响应体包含操作详情。                        |
| 400  | Bad Request（错误请求） | 参数缺失或无效（例如，文件类型不支持）。               |
| 401  | Unauthorized（未授权） | JWT 令牌无效或缺失。                                   |
| 413  | Payload Too Large（请求体过大） | 上传文件大小超出限制。                               |
| 500  | Internal Server Error（服务器内部错误） | 服务器发生意外错误。                                |

## 支持的输出格式

| **输出格式**                                                                                           | **说明**                                                                                          |
| :----------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------ |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | Excel 95/5.0 - 2003 工作簿。                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | Office Open XML 电子表格文件格式。                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | Excel 二进制工作簿。                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | 支持宏的 Excel 工作簿。                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | Excel 97 - 2003 模板。                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | Excel 模板。                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | 支持宏的 Excel 模板。                                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | Excel 宏启用加载项文件，用于为 Excel 添加新函数。                                                 |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | CSV（逗号分隔值）文件。                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | TSV（制表符分隔值）文件。                                                                         |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | 分隔符分隔的纯文本文件。                                                                          |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | HTML 格式。                                                                                       |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | MHTML 文件。                                                                                      |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ODS（OpenDocument 电子表格）。                                                                    |
| SpreadsheetML                                                                                          | Excel 2003 XML 文件。                                                                             |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | 由 Apple 的“Numbers”应用程序创建的文档，该程序是 macOS 和 iOS 上 iWork 套件的一部分。            |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | JavaScript 对象表示法。                                                                           |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | 数据交换格式（Data Interchange Format）。                                                         |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | 带有 .dbf 扩展名的数据库文件，用于 dBASE 数据库管理系统。                                         |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | Adobe 可移植文档格式。                                                                            |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | XML 纸张规范格式。                                                                                |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | 可缩放矢量图形格式。                                                                              |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | 标记图像文件格式。                                                                                |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | 便携式网络图形格式。                                                                              |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | 位图图像格式。                                                                                    |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | 增强型图元文件格式。                                                                              |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG 是一种采用有损压缩算法保存的图像格式。                                                       |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | 图形交换格式。                                                                                    |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | Markdown 文档。                                                                                   |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | OpenOffice 和 StarOffice 使用的基于 XML 的格式。                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | 以扁平 XML 形式存储的 Open Document 格式。                                                        |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | Microsoft Word 文档的知名格式，结合了 XML 和二进制文件。                                          |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | PPTX 格式基于 Microsoft PowerPoint Open XML 演示文稿文件格式。                                   |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | 结构化查询语言（SQL）。                                                                           |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML 是一种基于 XML 标记语言的文本格式，是对 HTML 4.0 的重新表述。                               |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | 带有 .epub 扩展名的文件是一种电子书格式，为出版商和消费者提供标准的数字出版物。                    |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML（可扩展标记语言）是一种类似 HTML 的标记语言，但使用标签定义对象。                             |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | Open Document 模板电子表格（OTS）文件。                                                           |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW 是亚马逊为 Kindle 设备开发的电子书文件格式；AZW3 也称为 Kindle Format 8（KF8）。             |

## 应该在哪里使用电子表格转换 API？

- **遗留系统迁移**：将数千个旧版 XLS 文件转换为 XLSX，以适配现代系统。
- **归档标准化**：将各种电子表格格式（XLS、XLSM、ODS、CSV）统一转换为单一格式用于归档。
- **办公套件互操作性**：将 Excel 文件转换为与 LibreOffice、Google Sheets 或 Apple Numbers 兼容的格式。
- **数据源标准化**：将各种电子表格格式转换为 CSV 或 JSON，以便导入数据库。
- **网页发布**：将财务模型转换为 HTML 格式，以便网页展示。

## 为什么应使用电子表格转换 API？

- **开发者友好**：Aspose.Cells Cloud 提供多种编程语言的 SDK 库，便于快速开发，并附带详尽文档。相比自行构建图表渲染解决方案，可显著减少开发工作量。
- **经济高效**：可在不预先上传工作簿的情况下转换表格数据，节省存储空间并降低成本。
- **全面的格式支持**：支持 20 多种电子表格格式之间的转换。
- **保留数据准确性与格式一致性**。

## 如何使用 SDK 调用电子表格转换 API？

以下代码示例展示了如何使用多种 SDK 调用电子表格转换 API。

### 电子表格转换 API 规范

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">电子表格转换 API 规范</a> 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 请求。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="11" tabName11="请求" tabName12="响应" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是最快捷的开发方式，它屏蔽了底层细节，使您能通过简洁的代码将电子表格文件转换为其他格式。请查阅 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 仓库</a> 以获取 Aspose.Cells Cloud SDK 的完整列表。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "使用 Aspose.Cells Cloud 将电子表格文件转换为其他格式。",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "将电子表格转换为指定格式。"
    }
  ]
}
</script>