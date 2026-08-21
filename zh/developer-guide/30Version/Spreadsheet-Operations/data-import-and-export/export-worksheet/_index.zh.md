---
title: "导出工作表 – Aspose.Cells Cloud"
second_title: "文档"
linktitle: "工作表"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [/export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells, 导出工作表, Excel API, PDF, CSV, TIFF, ODS, 图像格式"
description: "了解如何使用 Aspose.Cells Cloud REST API 将 Excel 工作表导出为 PDF、CSV、TIFF 及其他格式。包含 cURL 示例、所需身份验证、参数详情及响应处理说明。"
weight: 20
ArticleTitle: "将 Excel 工作表导出为多种格式 – Aspose.Cells Cloud"
---

您可以将工作表导出为以下格式：

- **XLS** – [XLS 格式详情](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [XLSX 格式详情](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [XLSB 格式详情](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [CSV 格式详情](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [TSV 格式详情](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [XLSM 格式详情](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [ODS 格式详情](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [TXT 格式详情](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [PDF 格式详情](https://docs.fileformat.com/pdf/)
- **OTS** – [OTS 格式详情](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [XPS 格式详情](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [DIF 格式详情](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [PNG 格式详情](https://docs.fileformat.com/Image/png/)
- **JPEG** – [JPEG 格式详情](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [BMP 格式详情](https://docs.fileformat.com/image/bmp/)
- **SVG** – [SVG 格式详情](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [TIFF 格式详情](https://docs.fileformat.com/image/tiff/)
- **EMF** – [EMF 格式详情](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Numbers 格式详情](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [FODS 格式详情](https://docs.fileformat.com/spreadsheet/fods/)

[了解其他相关导出操作，例如导出整个工作簿或图表。](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## PostExport API

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要基于 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 令牌的身份验证</a>。

### 请求参数

| 参数名称     | 类型   | 路径/查询字符串/HTTP 正文 | 必填 | 描述                                                                 |
|--------------|--------|---------------------------|------|----------------------------------------------------------------------|
| file         | 文件   | formData                  | 是   | 待上传的文件                                                         |
| objectType   | 字符串 | query                     | 是   | 待导出对象类型。导出图表时请使用 `chart`；其他可能值包括 `worksheet`（工作表）、`picture`（图片）等。 |
| format       | 字符串 | query                     | 是   | 目标输出格式。支持的值：`png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf`。 |

### 响应

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **错误处理**

若请求失败，API 将返回一个包含 `Code` 和 `Message` 字段的 JSON 错误对象。常见的 HTTP 状态码包括 **401 Unauthorized**（令牌缺失或无效）和 **400 Bad Request**（参数无效）。

**HTTP 状态码**

| 状态码 | 含义             | 描述                                           |
|--------|------------------|------------------------------------------------|
| 200    | OK（成功）       | 过滤器应用成功；响应包含操作详情。             |
| 400    | Bad Request（错误请求） | 缺少或参数无效（例如不支持的文件类型）。       |
| 401    | Unauthorized（未授权）  | JWT 令牌无效或缺失。                           |
| 413    | Payload Too Large（载荷过大） | 上传文件超过大小限制。                         |
| 500    | Internal Server Error（内部服务器错误） | 发生意外服务器错误。                           |

**注意事项**

- 上传文件的最大大小为 50 MB。  
- 该 API 支持单次请求导出多个工作表；每个工作表将作为独立文件返回于 `Files` 数组中。  
- 对于大型工作簿，可启用异步处理；使用 `202 Accepted` 响应轮询操作状态。

## 如何结合 SDK 使用 PostExport API

### 前置条件

调用 API 前，请通过 Aspose.Cells Cloud 身份验证流程获取有效的 JWT 访问令牌，并确保将其包含在每项请求的 `Authorization` 请求头中。SDK 在配置好客户端凭据后会自动完成令牌获取。

### PostExport API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) 定义了一个公开可访问的编程接口，可让您直接通过 Web 浏览器执行 REST 交互。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示如何使用 cURL 调用 Cloud API：

```bash
# 将工作表导出为 TIFF 格式
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是开发 Aspose.Cells Cloud 应用的最快方式。SDK 抽象了底层细节，使您能专注于业务逻辑。有关支持的 SDK 完整列表，请访问 [GitHub 仓库](https://github.com/aspose-cells-cloud)。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---