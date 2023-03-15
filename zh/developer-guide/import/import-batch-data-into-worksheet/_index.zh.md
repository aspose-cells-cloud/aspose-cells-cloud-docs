﻿---
title: 将批处理数据导入 Excel Workshee
second_title: Aspose.Cells Cloud Documen
linktitle: 导入批次数据
type: docs
url: /zh/import/batch-data/
aliases: [/import-batch-data-into-excel-worksheet/,/import-batch-data-into-worksheet/,/import-data/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API 支持批量导入Excel文件。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 19
---
这个 REST API `import batch data` 变成 Excel 工作表。

该请求是一个包含多部分内容的 HTTP 请求（请参阅[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)或者[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).多部分内容的第一部分包含 ImportBatchDataOption 数据，第二部分包含数据文件。

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

重要参数说明如下表：


**导入批处理数据选项**

|参数名称|类型|描述|
|:- |:- |:- |
|批量数据|列表<CellValue> |批量数据|
|目的地工作表|细绳|目标工作表名称。|
|是插入|细绳|真假。|
|导入数据类型|细绳|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData。|
|来源|文件来源|当 BatchData 参数为 null 时指示数据文件位置。|



**细胞价值**

|参数名称|类型|描述|
|:- |:- |:- |
|行索引|整数||
|列索引|整数||
|类型|细绳|数据类型|
|价值|细绳||
|风格|样式（对象）||



**文件来源**
|参数名称|类型|描述|
|:- |:- |:- |
|文件源类型|细绳|InMemoryFiles/CloudFileSystem/RequestFiles|
|文件路径|细绳|文件位置|


**例子**

```xml
<ImportIntArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportIntArrayOption>

```

## 云 SDK 系列

使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：


{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
