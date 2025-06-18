---
title: 将二维双精度数组导入 Excel 工作表
second_title: Aspose.Cells Cloud Documen
linktitle: 进口二维双阵列
type: docs
url: /zh/import/2dimension-double-array/
aliases: [/import-2dimension-double-array-into-excel-worksheet/,/import-2dimension-double-array-into-worksheet/, /import-data/2dimension-double-array/]
keywords: Import 2 dimension double array data into Excel files
description: Aspose.Cells Cloud REST API 支持将二维双数组数据导入 Excel 文件。SDK 支持多种开发语言。包括 Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby 和 swift
weight: 20
kwords: Excel、Office 云、REST API、电子表格、PDF、CSV、Json、Markdwon、将 2 维双精度数组导入 Excel 工作表
---
此 REST 将 API `import 2 dimension double array data` 放入 Excel 工作表。

该请求是具有多部分内容的 HTTP 请求（请参阅[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)或者[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)）。多部分内容的第一部分包含 Import2DimensionDoubleArrayOption 数据，第二部分包含数据文件。

## 重置 API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```
其中重要参数说明如下表：

**Import2DimensionDoubleArray选项**

|参数名称|类型|描述|
|:- |:- |:- |
|第一排|整数||
|第一列|整数||
|数据|双倍的[，]||
|目的地工作表|细绳|目标工作表名称。|
|是否插入|细绳|真假。|
|导入数据类型|细绳|整数数组/双精度数组/字符串数组/二维整数数组/二维双精度数组/二维字符串数组/批数据/CSV数据。|
|来源|文件源|当 BatchData 参数为空时，指示数据文件位置。|



**例子**

```json

{
    "Data": [
        [1.0, 2.9, 3.1],
        [2.0, 2.1, 3.1]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 4,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionDoubleArray"
}

```

## Cloud SDK 系列

使用 SDK 是加快开发速度的最佳方式。SDK 负责处理底层细节，让您专注于项目任务。请查看[GitHub 存储库](https://github.com/aspose-cells-cloud)获得 Aspose.Cells Cloud SDKs 的完整列表。

以下代码示例演示了如何使用各种 SDK 调用 Aspose.Cells Web 服务：

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




