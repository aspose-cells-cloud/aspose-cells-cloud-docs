---
title: "导出工作簿"
second_title: "文档"
linktitle: "工作簿"
type: docs
url: /zh/export-excel-to-different-formats/
aliases: [  /zh/export/excel-to-different-formats/ ]
keywords: "Aspose.Cells Cloud, Excel 导出, 工作簿转换, PDF, CSV, JSON, 图像格式, 电子表格 API, XLSX, ODS, PNG"
description: "逐步指南：使用 Aspose.Cells Cloud REST API 和 SDK 将 Excel 工作簿导出为多种格式，包括 PDF、CSV、JSON 及各种图像类型。"
weight: 20
---

您可以将工作簿导出为以下任意格式：[XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)、[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)。

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **安全与身份验证**

Aspose.Cells Cloud API 采用安全机制，需进行 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。


### 请求参数

| 参数名 | 类型 | 路径/查询字符串/HTTP 请求体 | 必填 | 描述 |
|--------|------|-----------------------------|------|------|
| file | 文件 | formData | 是 | 待上传的文件 |
| objectType | 字符串 | query | 是 | 待导出的对象类型。导出图表时使用 `chart`；其他可能值包括 `worksheet`（工作表）、`picture`（图片）等。 |
| format | 字符串 | query | 是 | 期望的输出格式。支持值：`png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf`。 |


### **响应**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**HTTP 状态码**

| 状态码 | 含义 | 描述 |
|--------|------|------|
| 200 | 成功 | 对象导出成功；响应包含文件列表。 |
| 400 | 错误请求 | 缺少或无效的参数。 |
| 401 | 未授权 | 无效或缺失的访问令牌。 |
| 413 | 请求实体过大 | 上传文件超出大小限制。 |
| 500 | 服务器内部错误 | 服务器发生意外错误。 |


## 如何使用 PostExport API 结合 SDK

### PostExport API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) 定义了一个公开可访问的编程接口，允许您直接从 Web 浏览器发起 REST 调用。

您可使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API：

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### 使用 Aspose.Cells Cloud SDK

使用 SDK 可加快开发进度，因其已处理底层细节，使您能专注于业务逻辑。Aspose.Cells Cloud SDK 的完整列表可在 [GitHub 仓库](https://github.com/aspose-cells-cloud) 中查看。

以下代码示例展示了如何使用多种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}