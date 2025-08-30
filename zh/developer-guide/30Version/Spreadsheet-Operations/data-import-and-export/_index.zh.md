---
title: 将数据导入 Excel 文件并从 Excel 文件导出数据
second_title: Aspose.Cells Cloud Documen
linktitle: 进出口数据
type: docs
url: /zh/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: 生成可包含图表、表格和其他数据可视化元素的新文档或报告
weight: 25
kwords: Excel 数据导入与直接数据库访问；批量数据导入与逐行数据写入；自动数据导出与手动数据提取。
---
Aspose.Cells云API支持从多种数据源导入数据，并可将Excel、图表、图例数据导出为不同格式，包括Excel、CSV、PDF、HTML、PNG等，使数据管理和共享变得简单高效。

## 如何从各种数据源导入数据

将数据导入 Excel 文件是一个复杂的过程。许多因素都会增加其复杂性，因此在导出过程中应考虑这些因素。Aspose.Cells Cloud 的一大优势在于能够以精准的专业质量将各种格式和类型的数据导入文件。

### 导入数据 API 信息

提供了以下 API 来将数据导入到一个或多个 Excel 文件中：

|API|描述|
|:- |:- |
|[POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|无需使用存储即可将数据导入 Excel 文件。|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|使用存储将数据导入 Excel 文件。|

### 请求参数

#### 不使用存储

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|文件|文件|表单数据|要上传的文件|
|导入选项|导入选项|HTTP主体|整数数组/双精度数组/字符串数组/二维整数数组/二维双精度数组/二维字符串数组/批量数据/CSV数据/图片|

#### 使用存储

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路||
|文件夹|细绳|询问||
|存储名称|细绳|询问|存储名称。|
|导入数据||身体||

#### 导入数据选项参数

**重要参数说明如下表**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>批量数据</td><td>列表<CellValue></td> <td>批次数据</td> </tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维字符串批量数据数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>转换数字数据</td><td>细绳</td> <td>真/假。</td> </tr>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一列</td><td>整数</td><td></td></tr>
    <tr><td>分隔符字符串</td><td>细绳</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>自定义解析器</td><td>列表<CustomParserConfig></td><td></td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>CSV数据</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一列</td><td>整数</td><td></td></tr>
    <tr><td>垂直</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>数据</td><td>细绳[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>图片</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一列</td><td>整数</td><td></td></tr>
    <tr><td>数据</td><td>整数[,]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维整数数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一列</td><td>整数</td><td></td></tr>
    <tr><td>数据</td><td>双倍的[，]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维双精度数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一列</td><td>整数</td><td></td></tr>
    <tr><td>数据</td><td>细绳[，]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维字符串数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一列</td><td>整数</td><td></td></tr>
    <tr><td>垂直</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>数据</td><td>整数[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>整数数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一列</td><td>整数</td><td></td></tr>
    <tr><td>垂直</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>数据</td><td>双倍的[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>双数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>左上行</td><td>整数</td> <td></td> </tr>
    <tr> <td>左上列</td><td>整数</td><td></td></tr>
    <tr> <td>右下行</td><td>整数</td> <td></td> </tr>
    <tr> <td>右下列</td><td>整数</td><td></td></tr>
    <tr><td>文件名</td><td>细绳</td><td></td></tr>
    <tr><td>数据</td><td>细绳</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真/假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>字符串数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>当 BatchData 参数为空时，指示数据文件位置。</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr><td>行索引</td><td>整数</td> <td></td> </tr>
    <tr><td>列索引</td><td>整数</td><td></td></tr>
    <tr><td>类型</td><td>细绳</td><td>数据类型</td></tr>
    <tr><td>价值</td><td>细绳</td> <td></td></tr>
    <tr><td>风格</td><td>样式（对象）</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr><td>文件源类型</td><td>细绳</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>文件路径</td><td>细绳</td><td>文件位置</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## 如何将 Excel 对象导出为各种文件格式

如果您最初以某种格式创建了 Excel 文件，例如[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)， 和[CSV](https://docs.fileformat.com/spreadsheet/csv/)有时，您可能会发现将 Excel 文件转换为其他格式很有用，这样您就可以利用其提供的特殊功能。例如，您可能希望将 Excel 文件导出到[PDF](https://docs.fileformat.com/pdf/)保护您的内容免受任何未经授权的修改，并使其易于同时阅读和共享。

Excel 对象的导出过程非常复杂。许多因素都会增加其复杂性，因此在导出过程中应考虑这些因素。能够将 Excel 对象导出为具有精确专业质量的单一格式文件是 Aspose.Cells Cloud 的一大亮点。

它完美适用于从 Excel 文件导出的工作簿、图表、形状和图片。您可以导出以下格式：[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [消耗臭氧层物质](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) . 仅导出格式：[PDF](https://docs.fileformat.com/pdf/), [奥特斯](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [数字](https://docs.fileformat.com/spreadsheet/numbers/), [食物中毒](https://docs.fileformat.com/spreadsheet/fods/).

该请求是具有多部分内容的 HTTP 请求（请参阅[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)或者[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。多部分内容的第一部分包含数据文件，第二部分包含保存选项。

将 REST API `export` 工作簿和内部对象转换为不同格式的文件。

### 出口API信息

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

请求参数为：

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|文件|文件|表单数据|要上传的文件|
|对象类型|细绳|询问|对象类型（工作簿/工作表/图表/形状/图片/列表对象/ole对象）|
|格式|细绳|询问|[文件格式](/cells/zh/supported-file-formats/)  |

这[OpenAPI规范](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)定义一个可公开访问的编程接口，并允许您直接从 Web 浏览器执行 REST 交互。

您可以使用 cURL 命令行工具轻松访问 Aspose.Cells 的 Web 服务。以下示例展示了如何使用 cURL 调用云端 API。

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

## 如何调用导入导出 API

以下文章详细讲解了各个API如何调用，并包含cURL和各个API的SDK示例：

- [如何在不使用存储的情况下将数据导入 Excel 文件。](/cells/zh/import/without-using-storage)
- [如何使用存储将数据导入 Excel 文件。](/cells/zh/import/with-using-storage)
- [如何将批次数据导入 Excel 工作表](/cells/zh/import-batch-data-into-excel-worksheet/)
- [如何将 CSV 数据导入 Excel 工作表](/cells/zh/import-csv-data-into-excel-worksheet/)
- [如何将图片导入Excel工作表](/cells/zh/import-picture-into-excel-worksheet/)
- [如何将整数数组导入 Excel 工作表](/cells/zh/import-integer-array-into-excel-worksheet/)
- [如何将双精度数组导入 Excel 工作表](/cells/zh/import-double-array-into-excel-worksheet/)
- [如何将字符串数组导入 Excel 工作表](/cells/zh/import-string-array-into-excel-worksheet/)
- [如何将二维整数数组导入 Excel 工作表](/cells/zh/import-a-2D-integer-array-into-excel-worksheet/)
- [如何将二维双精度数组导入 Excel 工作表](/cells/zh/import-a-2D-double-array-into-excel-worksheet/)
- [如何将二维字符串数组导入 Excel 工作表](/cells/zh/import-a-2D-string-array-into-excel-worksheet/)
- [将 Excel 图表导出为不同的文件格式](/cells/zh/export-excel-chart-to-different-formats/)
- [将 Excel 列表对象导出为不同的文件格式](/cells/zh/export-excel-listobject-to-different-formats/)
- [将 Excel ole 对象导出为不同的文件格式](/cells/zh/export-excel-ole-object/)
- [将 Excel 图片导出为不同的文件格式](/cells/zh/export-excel-picture-to-different-formats/)
- [将 Excel 形状导出为不同的文件格式](/cells/zh/export-excel-shape-to-different-formats/)
- [将 Excel 工作簿导出为不同的文件格式](/cells/zh/export-excel-to-different-formats/)
- [将 Excel 工作表导出为不同的文件格式](/cells/zh/export-excel-worksheet-to-different-formats//)
