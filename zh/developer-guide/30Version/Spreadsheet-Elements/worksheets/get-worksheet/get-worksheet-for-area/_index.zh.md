---
title: "导出工作表区域为 PNG、PDF、CSV — Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "区域"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, 导出工作表区域, PNG, PDF, CSV, Excel 转换, REST API, SDK"
description: "了解如何使用 Aspose.Cells Cloud REST API 或 SDK（C#、Java、Python 等）将 Excel 工作表中的指定单元格区域导出为 PNG、PDF、CSV 及其他 20 多种格式。"
weight: 230
ArticleTitle: "使用 Aspose.Cells Cloud API 将工作表区域导出为 PNG、PDF、CSV — 完整指南"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API 可将工作表的指定区域转换为多种文件格式。支持的格式包括：[XLS](https://docs.fileformat.com/spreadsheet/xls/)、[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)、[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)、[CSV](https://docs.fileformat.com/spreadsheet/csv/)、[TSV](https://docs.fileformat.com/spreadsheet/tsv/)、[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)、[ODS](https://docs.fileformat.com/spreadsheet/ods/)、[TXT](https://docs.fileformat.com/word-processing/txt/)、[PDF](https://docs.fileformat.com/pdf/)、[OTS](https://docs.fileformat.com/spreadsheet/ots/)、[XPS](https://docs.fileformat.com/page-description-language/xps/)、[DIF](https://docs.fileformat.com/spreadsheet/dif/)、[PNG](https://docs.fileformat.com/Image/png/)、[JPEG](https://docs.fileformat.com/image/jpeg/)、[GIF](https://docs.fileformat.com/image/gif/)、[BMP](https://docs.fileformat.com/image/bmp/)、[WMF](https://docs.fileformat.com/image/wmf/)、[TIFF](https://docs.fileformat.com/image/tiff/)、[EMF](https://docs.fileformat.com/image/emf/)、[NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)、[FODS](https://docs.fileformat.com/spreadsheet/fods/)。

本指南介绍如何使用 Aspose.Cells Cloud API 将 Excel 工作表中的**特定单元格区域**导出为 PNG、PDF、CSV 及其他 20 多种格式。如需了解相关操作（如导出整个工作表或转换整个工作簿），请参阅 **[导出整个工作表](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** 和 **[将工作簿转换为 PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)** 页面。

## REST API

[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat)定义了一个公开可用的编程接口，可让您直接从 Web 浏览器执行 REST 交互。

### 请求参数

| 参数                  | 类型   | 必填 | 描述                                         |
|-----------------------|--------|------|----------------------------------------------|
| `name`                | string | 是   | 工作簿文件名。                               |
| `sheetName`           | string | 是   | 目标工作表名称。                             |
| `format`              | string | 是   | 所需的输出格式（如 png、pdf、csv 等）。      |
| `area`                | string | 否   | 要导出的单元格区域（例如：`B3:K8`）。        |
| `verticalResolution`  | int    | 否   | 光栅格式的垂直 DPI。                         |
| `horizontalResolution`| int    | 否   | 光栅格式的水平 DPI。                         |
| `folder`              | string | 否   | 包含该文件的云存储文件夹。                   |
| `storage`             | string | 否   | 存储服务的名称。                             |

### 成功响应

* **200 OK** — 以二进制格式返回请求的文件（PNG、PDF、CSV 等）。

### 错误响应

| 状态码 | 描述                                       |
|--------|--------------------------------------------|
| 400    | 错误请求 — 缺少或无效的参数。              |
| 401    | 未授权 — 缺少或无效的认证令牌。            |
| 404    | 未找到 — 指定的工作簿或工作表不存在。      |
| 500    | 内部服务器错误 — 服务器上发生意外情况。    |

**错误响应示例**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "参数 'area' 格式错误。预期格式：B3:K8。"
  }
}
```

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例展示了如何使用 cURL 调用 Cloud API。

{{< tabs tabTotal="2" tabID="1" tabName1="请求" tabName2="响应" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

已转换的图像（二进制 PNG）

{{< /tab >}}

{{< /tabs >}}

## 云 SDK 家族

使用 SDK 是开发速度最快的途径。SDK 抽象了底层细节，让您专注于项目逻辑。请查看 [GitHub 仓库](https://github.com/aspose-cells-cloud)，获取 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例展示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}