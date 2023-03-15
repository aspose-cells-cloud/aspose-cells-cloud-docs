---
title: 将字符串数组导入 Excel Workshee
second_title: Aspose.Cells Cloud Documen
linktitle: 导入字符串数组
type: docs
url: /zh/import/string-array/
aliases: [/import-string-array-into-excel-worksheet/,/import-string-array-into-worksheet/,/import-data/string-array/]
keywords: Import string array data into Excel files
description: Aspose.Cells Cloud REST API 支持将字符串数组数据导入到 Excel 文件中。 SDK支持多种开发语言。它们包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 40
---
这个 REST API `import string array data` 变成 Excel 工作表。

该请求是一个包含多部分内容的 HTTP 请求（请参阅[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)或者[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).多部分内容的第一部分包含 ImportStringArrayOption 数据，第二部分包含数据文件。

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

重要参数说明如下表：


**导入字符串数组选项**

|参数名称|类型|描述|
|:- |:- |:- |
|第一排|整数||
|第一列|整数||
|是垂直的|细绳|真假。|
|数据|细绳[]||
|目的地工作表|细绳|目标工作表名称。|
|是插入|细绳|真假。|
|导入数据类型|细绳|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData。|
|来源|文件来源|当 BatchData 参数为 null 时指示数据文件位置。|


**例子**

```xml

<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>

```

## 云 SDK 系列

使用 SDK 是加速开发的最佳方式。 SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 仓库](https://github.com/aspose-cells-cloud)有关 Aspose.Cells Cloud SDK 的完整列表。

以下代码示例演示如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




