---
title: "Import String Array into Excel Worksheet"
second_title: "Document"
linktitle: "Import string array"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Import String Array, Excel, Aspose.Cells Cloud, REST API, Spreadsheet"
description: "Learn how to import a string array into an Excel worksheet using the Aspose.Cells Cloud REST API. This guide covers the required multipart request, parameter details, and SDK examples for multiple programming languages."
weight: 40
---

This REST API imports string array data into an Excel worksheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the **ImportStringArrayOption** data and the second part contains the data file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The important parameters are described in the following table:

**ImportStringArrayOption**

| Parameter Name          | Type        | Description                                                                                           |
|-------------------------|------------|-------------------------------------------------------------------------------------------------------|
| FirstRow                | int        | The starting row index (1‑based) where the data will be placed.                                      |
| FirstColumn             | int        | The starting column index (1‑based) where the data will be placed.                                   |
| IsVertical              | string     | `true` to insert data vertically; `false` to insert horizontally.                                    |
| Data                    | String[]   | The string array to be imported.                                                                      |
| DestinationWorksheet    | string     | The name of the worksheet that will receive the data.                                                |
| IsInsert                | string     | `true` to insert rows/columns; `false` to overwrite existing cells.                                   |
| ImportDataType          | string     | Type of data being imported (e.g., `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source                  | FileSource | Indicates the data file location when the **BatchData** parameter is null.                           |

### Example

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

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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