---
title: "导出列表对象"
second_title: "文档"
linktitle: "列表对象"
type: docs
url: /export-excel-listobject-to-different-formats/
aliases: [/export/excel-listobject-to-different-formats/]
keywords: "导出 ListObject, Excel ListObject, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, XLSX, ODS, PNG, TIFF, SDKs"
description: "Aspose.Cells Cloud REST API 支持将 Excel ListObjects 导出为多种文件格式。SDK 支持多种编程语言，包括 C#、Java、Python、Node.js、Go、PHP、Ruby、Perl 和 Swift。"
weight: 20
---

您可以导出以下格式：[XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)、[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[BMP](https://docs.fileformat.com/image/bmp/)、[SVG](https://docs.fileformat.com/page-description-language/svg/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)。

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **安全与身份验证**

Aspose.Cells Cloud API 是安全的，需要使用 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">基于 JWT 令牌的身份验证</a>。

### 请求参数

| 参数名 | 类型    | 路径/查询字符串/HTTP 请求体 | 是否必需 | 描述 |
|--------|---------|----------------------------|----------|------|
| file   | file    | formData                   | 是       | 待上传的文件 |
| objectType | string | query                      | 是       | 待导出的对象类型。若导出图表，请使用 `chart`；其他可能的值包括 `worksheet`、`picture` 等。 |
| format | string  | query                      | 是       | 目标输出格式。支持的值：`png`、`jpeg`、`gif`、`bmp`、`svg`、`tiff`、`emf`、`wmf`、`pdf`。 |

### 响应示例

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2_ListObjects_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### HTTP 状态码

| 状态码 | 含义             | 描述 |
|--------|------------------|------|
| 200    | OK（成功）       | 成功应用筛选；响应包含操作详情。 |
| 400    | Bad Request（错误请求） | 参数缺失或无效（例如不支持的文件类型）。 |
| 401    | Unauthorized（未授权） | JWT 令牌无效或缺失。 |
| 413    | Payload Too Large（请求实体过大） | 上传文件超出大小限制。 |
| 500    | Internal Server Error（服务器内部错误） | 服务器发生意外错误。 |

## 如何结合 SDK 使用 PostExport API

### PostExport API 规范

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) 定义了一个公开可访问的编程接口，允许您直接通过网页浏览器发起 REST 交互。

您可以使用 **cURL** 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API：

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=listobject&format=tiff" \
-H "accept: multipart/form-data" \
-H "Content-Type: multipart/form-data" \
-H "x-aspose-client: Containerize.Swagger" \
-d '{"File":{}}'
```

### 使用 Aspose.Cells Cloud SDK

使用 SDK 是加快开发速度的最佳方式。SDK 处理底层细节，让您专注于项目任务。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用不同 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportListObject.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportListObject.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportListObject.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportListObject.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportListObject.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportListObject.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportListObject.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportListObject.go" >}}
{{< /tab >}}

{{< /tabs >}}