---
title: "Import Batch Data into Excel Worksheet"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /import-data/batch-data/
aliases: [/import-batch-data-into-excel-worksheet/,/import-batch-data-into-worksheet/]
description: "Cells.Cloud API for Excel operate: Import Batch Data into Excel Worksheet."
weight: 10
---


This REST API `import batch data` into Excel work sheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the ImportBatchDataOption data and the second contains a data file.

The important parameters are described in the following table:


**ImportBatchDataOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| BatchData | List<CellValue> | batch data | 
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |



**CellValue**

| Parameter Name|Type|Description|
| :- | :- | :- |
| rowIndex | int |  | 
| columnIndex | int |  | 
| type | string | data type |
| value | string |  |
| style | Style(object) |  |



**FileSource**
| Parameter Name|Type|Description|
| :- | :- | :- |
| FileSourceType | string | InMemoryFiles/CloudFileSystem/RequestFiles | 
| FilePath | string | file position |


**Example**

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

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:


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
