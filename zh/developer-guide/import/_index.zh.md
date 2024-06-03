---
title: 重要
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API 支持将数据导入 Excel 文件。SDK 支持多种开发语言。包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 31
kwords: Excel, Office 云, REST API, 电子表格, PDF, CSV, Json, Markdwon, 导入
---
将数据导入 Excel 文件是一个复杂的过程。许多因素都会造成复杂性，因此在导出过程中应考虑到这些因素。能够以精确的专业质量将各种格式和类型的数据导入文件是 Aspose.Cells Cloud 的一大特色。

## RSET API

提供了以下 API 用于将数据导入一个或多个 Excel 文件：

|API|描述|
|:- |:- |
|[POST /单元格/导入](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|无需使用存储即可将数据导入 Excel 文件。|
|[POST /cells/{名称}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|使用存储将数据导入Excel文件。|

## 请求参数
 
### 无需使用存储

|参数名称|类型|路径/查询字符串/HTTPBody|描述|
|:- |:- |:- |:- |
|文件|文件|表单数据|要上传的文件|
|导入选项|导入选项|HTTP主体|整数数组/双精度数组/字符串数组/二维整数数组/二维双精度数组/二维字符串数组/批数据/CSV数据/图片|

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
    <tr> <td>批次数据</td><td>列表<CellValue></td> <td>批次数据</td> </tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>二维字符串批数据数组</td></tr>
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
    <tr> <td>转换数值数据</td><td>细绳</td> <td>真假。</td> </tr>
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
    <tr><td>垂直</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>数据</td><td>细绳[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
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
    <tr><td>数据</td><td>整数[，]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
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
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
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
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
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
    <tr><td>垂直</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>数据</td><td>整数[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>导入数据类型</td><td>细绳</td><td>整型数组</td></tr>
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
    <tr><td>垂直</td><td>细绳</td><td>真假。</td></tr>
    <tr><td>数据</td><td>双倍的[]</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
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
    <tr> <td>右下栏</td><td>整数</td><td></td></tr>
    <tr><td>文件名</td><td>细绳</td><td></td></tr>
    <tr><td>数据</td><td>细绳</td> <td></td></tr>
    <tr> <td>目的地工作表</td><td>细绳</td><td>目标工作表名称。</td></tr>
    <tr><td>是否插入</td><td>细绳</td><td>真假。</td></tr>
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

## 如何调用 RSET API

以下文章详细说明了每个API如何调用，并包含cURL和每个API的SDK示例：

- [如何在不使用存储的情况下将数据导入 Excel 文件。](/cells/zh/import/without-using-storage)
- [如何使用存储将数据导入Excel文件。](/cells/zh/import/with-using-storage)
- [如何将批次数据导入 Excel 工作表](/cells/zh/import/batch-data/)
- [如何将 CSV 数据导入 Excel 工作表](/cells/zh/import/csv-data/)
- [如何将图片导入 Excel 工作表](/cells/zh/import/picture/)
- [如何将整数数组导入 Excel 工作表](/cells/zh/import/integer-array/)
- [如何将双精度数组导入 Excel 工作表](/cells/zh/import/double-array/)
- [如何将字符串数组导入 Excel 工作表](/cells/zh/import/string-array/)
- [如何将二维整数数组导入 Excel 工作表](/cells/zh/import/2dimension-integer-array/)
- [如何将二维双精度数组导入 Excel 工作表](/cells/zh/import/2dimension-double-array/)
- [如何将二维字符串数组导入 Excel 工作表](/cells/zh/import/2dimension-string-array/)
