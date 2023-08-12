---
title: 进口
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API 支持将数据导入到 Excel 文件中。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 31
---
将数据导入 Excel 文件是一个复杂的过程。许多因素导致了复杂性，因此在导出过程中应考虑到。能够以精确的专业品质将各种格式和类型的数据导入到文件中是Aspose.Cells Cloud的首要功能。

## RSET API

提供以下接口将数据导入到一个或多个Excel文件中：

|API|描述|
|:- |:- |
|[POST /单元格/导入](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|将数据导入到 Excel 文件中，无需使用存储。|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|使用存储将数据导入到 Excel 文件中。|

## 请求参数
 
### 不使用存储

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|文件|文件|表单数据|要上传的文件|
|导入选项|导入选项|HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/图片|

### 使用存储

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|姓名|细绳|小路||
|文件夹|细绳|询问||
|存储名称|细绳|询问|存储名称。|
|导入数据||身体||


### 导入数据选项参数

**重要参数说明如下表**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>批量数据</td><td>列表<CellValue></td> <td>批量数据</td> </tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维字符串批量数据数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">范围</th><th scope="col">类型</th> <th scope="col">描述</th></tr>
  </thead>
  <tbody>
    <tr> <td>转换数值数据</td><td>细绳</td> <td>真假。</td> </tr>
    <tr> <td>第一排</td><td>整数</td> <td></td> </tr>
    <tr> <td>第一栏</td><td>整数</td><td></td></tr>
    <tr><td>分隔符字符串</td><td>细绳</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>自定义解析器</td><td>列表<CustomParserConfig></td><td></td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>CSV数据</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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
    <tr> <td>第一栏</td><td>整数</td><td></td></tr>
    <tr><td>是垂直的</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>数据</td><td>细绳[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>图片</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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
    <tr> <td>第一栏</td><td>整数</td><td></td></tr>
    <tr><td>数据</td><td>整数[，]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维整数数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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
    <tr> <td>第一栏</td><td>整数</td><td></td></tr>
    <tr><td>数据</td><td>双倍的[，]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维双数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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
    <tr> <td>第一栏</td><td>整数</td><td></td></tr>
    <tr><td>数据</td><td>细绳[，]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维字符串数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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
    <tr> <td>第一栏</td><td>整数</td><td></td></tr>
    <tr><td>是垂直的</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>数据</td><td>整数[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>整数数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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
    <tr> <td>第一栏</td><td>整数</td><td></td></tr>
    <tr><td>是垂直的</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>数据</td><td>双倍的[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>双数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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
    <tr> <td>左上栏</td><td>整数</td><td></td></tr>
    <tr> <td>右下行</td><td>整数</td> <td></td> </tr>
    <tr> <td>右下栏</td><td>整数</td><td></td></tr>
    <tr><td>文件名</td><td>细绳</td><td></td></tr>
    <tr><td>数据</td><td>细绳</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>字符串数组</td></tr>
    <tr> <td>来源</td><td>文件源</td><td>BatchData参数为空时，表示数据文件位置。</td></tr>
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

## 如何调用RSET API

以下文章详细讲解了每个API如何调用，并包含每个cURL以及每个API的SDK示例：

- [如何在不使用存储的情况下将数据导入到 Excel 文件中。](/cells/zh/import/without-using-storage)
- [如何使用存储将数据导入到 Excel 文件中。](/cells/zh/import/with-using-storage)
- [如何将批次数据导入Excel工作表](/cells/zh/import/batch-data/)
- [如何将 CSV 数据导入 Excel 工作表](/cells/zh/import/csv-data/)
- [如何将图片导入Excel工作表](/cells/zh/import/picture/)
- [如何将整数数组导入 Excel 工作表](/cells/zh/import/integer-array/)
- [如何将双数组导入 Excel 工作表](/cells/zh/import/double-array/)
- [如何将字符串数组导入 Excel 工作表](/cells/zh/import/string-array/)
- [如何将二维整数数组导入 Excel 工作表](/cells/zh/import/2dimension-integer-array/)
- [如何将二维双数组导入到 Excel 工作表中](/cells/zh/import/2dimension-double-array/)
- [如何将二维字符串数组导入到 Excel 工作表中](/cells/zh/import/2dimension-string-array/)
