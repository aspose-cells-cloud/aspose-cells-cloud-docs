---
title: 将 CSV 数据导入 Excel 工作表
second_title: Aspose.Cells Cloud Documen
linktitle: 导入 csv 数据
type: docs
url: /zh/import/csv-data/
aliases: [/import-csv-data-into-excel-worksheet/, /import-csv-data-into-worksheet/,/import-data/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API 支持将 csv 数据导入 Excel 文件。SDK 支持多种开发语言。包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 19
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、将 CSV 数据导入 Excel 工作表
---
此 REST 将 API `import csv data` 放入 Excel 工作表。

该请求是具有多部分内容的 HTTP 请求（请参阅[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)或者[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。多部分内容的第一部分包含 ImportCSVDataOption 数据，第二部分包含数据文件。

## 重置 API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

其中重要参数说明如下表：


**导入CSV数据选项**

|参数名称|类型|描述|
|:- |:- |:- |
|分隔符字符串|细绳||
|转换数值数据|细绳|真假。|
|第一排|整数||
|第一列|整数||
|源文件|细绳||
|自定义解析器|列表<CustomParserConfig> ||


**自定义解析器配置**

|参数名称|类型|描述|
|:- |:- |:- |
|列索引|整数||
|解析方法|细绳||
|自定义样式|细绳||

**例子**

```xml

 <ImportCSVDataOption>
     <DestinationWorksheet>Sheet1</DestinationWorksheet>
     <IsInsert>true</IsInsert>
     <ImportDataType>CSVData</ImportDataType>
     <SeparatorString>;</SeparatorString>
     <ConvertNumericData>true</ConvertNumericData>
     <FirstRow>1</FirstRow>
     <FirstColumn>2</FirstColumn>
     <SourceFile>TestImportDataCSV.csv</SourceFile>
     <CustomParsers>
         <CustomParserConfig>
             <ColumnIndex>0</ColumnIndex>
             <ParseMethod>ToString</ParseMethod>
             <CustomStyle>#</CustomStyle>
         </CustomParserConfig>
     </CustomParsers>
 </ImportCSVDataOption>

```

## Cloud SDK 系列

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
