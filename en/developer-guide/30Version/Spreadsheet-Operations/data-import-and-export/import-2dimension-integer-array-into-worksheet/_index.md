---
title: "Import 2 Dimension Integer Array into Excel Worksheet"
second_title: "Document"
linktitle: "Import 2 dimension integer array"
type: docs
url: /import-a-2D-integer-array-into-excel-worksheet/
aliases: [/import-2dimension-integer-array-into-excel-worksheet/,/import-2dimension-integer-array-into-worksheet/, /import-data/2dimension-integer-array/, /import/2dimension-integer-array/]
keywords: "Aspose.Cells Cloud, import 2D integer array, Excel worksheet, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API enables importing two‑dimensional integer arrays into Excel worksheets. SDKs are available for Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 20
---

This REST API **imports a two‑dimensional integer array** into an Excel worksheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the `Import2DimensionIntegerArrayOption` data and the second part contains the data file.

The important parameters are described in the following table:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

**Import2DimensionIntegerArrayOption**

| Parameter Name          | Type            | Description                                                                                                   |
|-------------------------|-----------------|---------------------------------------------------------------------------------------------------------------|
| FirstRow                | int             | The 1‑based index of the first row where the data will be placed.                                            |
| FirstColumn             | int             | The 1‑based index of the first column where the data will be placed.                                         |
| Data                    | Integer[,]      | Two‑dimensional integer array containing the values to import.                                               |
| DestinationWorksheet    | string          | Name of the destination worksheet.                                                                            |
| IsInsert                | string          | `"true"` to insert the data (shifting existing cells), `"false"` to overwrite existing cells.                |
| ImportDataType          | string          | Specifies the data format. Supported values: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source                  | FileSource      | Indicates the data file location when the `BatchData` parameter is `null`.                                   |

**Example**

```json
{
    "Data": [
        [1, 2],
        [3, 4]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 4,
    "FirstColumn": 1,
    "ImportDataType": "TwoDimensionIntArray"
}
```

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}