---
title: "Import String Array into Excel Worksheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Import string array"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases: [/import-string-array-into-worksheet/,/import-data/string-array/,/import/string-array/]
keywords: "Import string array data into Excel files."
description: "Aspose.Cells Cloud REST API support importing string array data into Excel files. SDK support kinds of development languages. They include Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby, and swift."
weight: 40
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Import String Array into Excel Worksheet
---

This REST API `import string array data` into Excel work sheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the ImportStringArrayOption data and the second contains a data file.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

The important parameters are described in the following table:

**ImportStringArrayOption**

| Parameter Name|Type|Description|
| :- | :- | :- |
| FirstRow | int |  |
| FirstColumn | int |  |
| IsVertical | string | true/false. |
| Data | String[] |  |
| DestinationWorksheet | string | destination work sheet name. |
| IsInsert | string | true/false. |
| ImportDataType | string | IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Source | FileSource | Indicates data file position when the BatchData parameter is null. |

**Example**

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

## Cloud SDK Family

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

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
