---
title: "导出工作表页面 – Aspose.Cells Cloud API 参考"
articleTitle: "导出工作表页面 – Aspose.Cells Cloud API 参考"
secondTitle: "文档"
linkTitle: "页面"
type: docs
url: /worksheets/page-to-different-formats/
aliases: [/get-worksheet-for-page-index/]
keywords: "Aspose.Cells Cloud, 工作表页面导出, PDF, PNG, CSV, REST API, JWT 身份验证, 文件格式"
description: "了解如何使用 Aspose.Cells Cloud REST API 将特定工作表页面导出为 PDF、PNG、CSV 等格式。包含 cURL 请求示例、参数说明以及多种语言的 SDK 示例。"
weight: 240
---

当您需要获取报表的可打印快照、图表图像或数据提取结果，而无需下载整个工作簿时，导出特定工作表页面非常有用。此接口可让您以最适合下游工作流的格式获取单页内容。

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API 可将指定工作表的某一页转换为多种文件格式。支持的格式包括：[XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)、[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[GIF](https://docs.fileformat.com/image/gif/)、[BMP](https://docs.fileformat.com/image/bmp/)、[WMF](https://docs.fileformat.com/image/wmf/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)。

## REST API

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) 定义了一个公开可用的编程接口，使您能够直接通过 Web 浏览器执行 REST 调用。

> **前提条件** – 您必须拥有有效的 JWT 身份验证令牌，并将工作簿存储在通过 `folder` 参数指定的云文件夹中。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 云服务。以下示例展示了如何使用 cURL 调用云 API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**响应** – 服务以所选格式返回请求的页面。对于图像格式（png、jpeg、gif 等），响应体包含二进制图像数据；对于文档格式（pdf、xls、csv 等），响应体包含文件内容。成功调用将返回 HTTP 200 状态码。

*PNG 响应示例（base64 编码片段，已截断）：*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**参数说明**

| 参数名                 | 类型    | 描述                                                     | 默认值 |
| ---------------------- | ------- | -------------------------------------------------------- | ------ |
| `format`               | string  | 输出文件格式（例如 `pdf`、`png`、`csv`）。               | `pdf`  |
| `verticalResolution`   | integer | 渲染图像的垂直 DPI。                                     | `100`  |
| `horizontalResolution` | integer | 渲染图像的水平 DPI。                                     | `100`  |
| `pageIndex`            | integer | 要导出的工作表页面索引（从 0 开始，`0` 表示第一页）。     | `0`    |
| `folder`               | string  | 存放源工作簿的云存储文件夹。                             | —      |

**HTTP 状态码**

| 状态码 | 含义             | 描述                                       |
|--------|------------------|--------------------------------------------|
| 200    | OK（成功）       | 操作成功；响应体包含操作详情。             |
| 400    | Bad Request      | 缺失或无效的参数（例如不支持的文件类型）。 |
| 401    | Unauthorized     | 无效或缺失 JWT 令牌。                      |
| 413    | Payload Too Large| 上传文件超出大小限制。                     |
| 500    | Internal Server Error | 服务器内部意外错误。                  |

**可能的错误**

- **401 Unauthorized** – 无效或缺失 JWT 令牌。
- **404 Not Found** – 指定的工作簿或工作表不存在。
- **400 Bad Request** – 参数值无效（例如不支持的 `format`）。
- **500 Internal Server Error** – 服务器端意外问题。

## 云 SDK 开发套件

使用 SDK 是加速开发的最佳方式。SDK 会处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells 云服务：

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