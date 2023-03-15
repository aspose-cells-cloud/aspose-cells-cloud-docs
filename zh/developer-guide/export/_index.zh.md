---
title: 将工作簿和内部对象导出为各种格式
second_title: Aspose.Cells Cloud Documen
linktitle: 出口
type: docs
url: /zh/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API 支持将 Excel 文件和内部对象导出为各种格式文件。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 31
---
如果您最初创建了一个特定格式的 Excel 文件，例如[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [超低频](https://docs.fileformat.com/spreadsheet/xlsb/)， 和[CSV文件](https://docs.fileformat.com/spreadsheet/csv/) , 您有时可能会发现将 excel 文件转换为另一种格式很有用，这样您就可以利用它提供的特殊功能。例如，您可能希望将 excel 文件导出到[PDF](https://docs.fileformat.com/pdf/)以保护您的内容免受任何未经授权的修改，并使其易于同时阅读和共享。

Excel 对象导出是一个复杂的过程。许多因素导致了复杂性，因此在出口过程中应予以考虑。能够将 Excel 对象导出为具有精确专业品质的格式文件是 Aspose.Cells Cloud 的一项顶级功能。

它非常适合从 Excel 文件导出的工作簿、图表、形状和图片。您可以导出格式：[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [超低频](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV文件](https://docs.fileformat.com/spreadsheet/csv/), [硅通孔](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [消耗臭氧层物质](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) .仅导出格式：[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [差值](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [数字](https://docs.fileformat.com/spreadsheet/numbers/), [食品](https://docs.fileformat.com/spreadsheet/fods/).

该请求是一个包含多部分内容的 HTTP 请求（请参阅[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)或者[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).多部分内容的第一部分包含数据文件，第二部分包含保存选项。

REST API `export` 工作簿和内部对象到不同格式的文件。

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

请求参数为：
 
|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|文件|文件|表单数据|要上传的文件|
|对象类型|细绳|询问|对象类型（工作簿/工作表/图表/形状/图片/listobject/oleobject）|
|格式|细绳|询问|[文件格式](/cells/zh/supported-file-formats/)  |
 
这[OpenAPI 规范](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport)定义了一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。
 
您可以使用 cURL 命令行工具轻松访问 Aspose.Cells Web 服务。以下示例显示如何使用 cURL 调用 Cloud API。
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## 云 SDK 系列


使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export.php" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


以下文章详细解释了每个API，包含cURL和每个API的SDK示例：


1. [将 Excel 图表导出为不同的文件格式](/cells/zh/export/excel-chart-to-different-formats/)
2. [将 Excel 列表对象导出为不同的文件格式](/cells/zh/export/excel-listobject-to-different-formats/)
3. [将 Excel ole 对象导出为不同的文件格式](/cells/zh/export/excel-ole-object/)
4. [将Excel图片导出为不同的文件格式](/cells/zh/export/excel-picture-to-different-formats/)
5. [将 Excel 形状导出为不同的文件格式](/cells/zh/export/excel-shape-to-different-formats/)
6. [将 Excel 工作簿导出为不同的文件格式](/cells/zh/export/excel-to-different-formats/)
7. [将 Excel 工作表导出为不同的文件格式](/cells/zh/export/excel-worksheet-to-different-formats//)
