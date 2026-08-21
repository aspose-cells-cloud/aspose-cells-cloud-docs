---
title: "使用 Aspose.Cells Cloud API 导出工作表——支持格式、cURL 和 SDK 示例"
second_title: "文档"
linktype: "docs"
url: /zh/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud 获取工作表、工作表导出、Excel API、REST、CSV、PDF、PNG、JPEG、GIF、BMP、TIFF、EMF、XPS、OTS、XLS、XLSX、XLSB、XLSM、ODS、FODS、Numbers、云 API"
description: "了解如何使用 Aspose.Cells Cloud REST API 从 Excel 文件中导出单个工作表。内容包括端点、参数、修正后的 cURL 示例、身份验证详情、错误处理，以及 C#、Java、Python 等多种语言的 SDK 代码片段。"
weight: 10
ArticleTitle: "使用 Aspose.Cells Cloud API 导出工作表——支持格式、cURL 和 SDK 示例"
---

此 REST API 可让您将 Excel 文件中的**单个工作表导出为多种不同文件格式**。

**摘要**——使用 **Get Worksheet（获取工作表）** 端点，以您选择的格式下载工作簿中的单个工作表。

支持导出的格式如下：

| 格式    | 扩展名   | MIME 类型                                                         |
| ------- | -------- | ----------------------------------------------------------------- |
| XLS     | .xls     | application/vnd.ms-excel                                          |
| XLSX    | .xlsx    | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb    | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv     | text/csv                                                          |
| TSV     | .tsv     | text/tab-separated-values                                         |
| XLSM    | .xlsm    | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods     | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt     | text/plain                                                        |
| PDF     | .pdf     | application/pdf                                                   |
| OTS     | .ots     | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps     | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif     | application/x-dif                                                 |
| PNG     | .png     | image/png                                                         |
| JPEG    | .jpeg    | image/jpeg                                                        |
| GIF     | .gif     | image/gif                                                         |
| BMP     | .bmp     | image/bmp                                                         |
| WMF     | .wmf     | image/wmf                                                         |
| TIFF    | .tiff    | image/tiff                                                        |
| EMF     | .emf     | image/emf                                                         |
| NUMBERS | .numbers | application/vnd.apple.numbers                                     |
| FODS    | .fods    | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## 安全与身份验证  
Aspose.Cells Cloud API 采用安全机制，需使用 [基于 JWT 令牌的身份验证](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)。

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **请求参数**

| 参数名称                 | 类型    | 位置   | 描述                                                                 |
| ------------------------ | ------- | ------ | -------------------------------------------------------------------- |
| **name**                 | string  | path   | **必需。** Excel 文件名。                                           |
| **sheetName**            | string  | path   | **必需。** 要导出的工作表名称。                                     |
| **format**               | string  | query  | 导出工作表的目标文件格式（例如：`pdf`、`png`）。                    |
| **verticalResolution**   | integer | query  | 图像格式（如 PNG、JPEG）的垂直分辨率（DPI）。                       |
| **horizontalResolution** | integer | query  | 图像格式的水平分辨率（DPI）。                                       |
| **area**                 | string  | query  | 要导出的单元格范围（例如：`A1:D10`）。                              |
| **pageIndex**            | integer | query  | 工作表分页时要导出的页码索引。                                      |
| **folder**               | string  | query  | 存储中源文件所在的文件夹路径。                                      |
| **storageName**          | string  | query  | Aspose Cloud 存储空间的名称。                                       |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI 规范</a> 定义了一个公开可访问的编程接口，可让您直接通过网页浏览器执行 REST 调用。

您可使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<二进制数据>
```

{{< /tab >}}

{{< /tabs >}}

## 错误处理

API 返回标准 HTTP 状态码。常见响应如下：

| 状态码 | 含义                                         | 示例 JSON 响应体                           |
| ------ | -------------------------------------------- | ------------------------------------------ |
| **200** | 成功——返回工作表数据流。                     | `{ "stream": "..." }`                      |
| **400** | 请求错误——缺少或参数无效。                   | `{ "error": "Invalid format parameter." }` |
| **401** | 未授权——JWT 令牌无效或缺失。                 | `{ "error": "Authentication failed." }`    |
| **404** | 未找到——指定的文件或工作表不存在。           | `{ "error": "Worksheet not found." }`      |
| **500** | 服务器内部错误——服务器发生意外情况。         | `{ "error": "Unexpected error." }`         |

请在客户端代码中正确处理这些响应，以向用户提供适当的反馈信息。

## 云 SDK 家族

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查阅 <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub 仓库</a>，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}