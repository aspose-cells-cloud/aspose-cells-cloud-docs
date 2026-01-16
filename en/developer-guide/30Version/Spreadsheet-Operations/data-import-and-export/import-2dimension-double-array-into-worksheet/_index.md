---
title: "Import 2‑Dimension Double Array into Excel Worksheet"
second_title: "Document"
linktitle: "Import 2‑dimension double array"
type: docs
url: /import-a-2D-double-array-into-excel-worksheet/
aliases: [/import-2dimension-double-array-into-excel-worksheet/,/import-2dimension-double-array-into-worksheet/, /import-data/2dimension-double-array/, /import/2dimension-double-array/]
keywords: "Import 2‑Dimension Double Array, Excel, Aspose Cells Cloud, REST API, Spreadsheet, Data Import"
description: "Learn how to import a two‑dimensional double array into an Excel worksheet using Aspose.Cells Cloud REST API. Includes request format, parameters, and SDK code samples."
weight: 20
---

This REST API **imports a two‑dimensional double array** into an Excel worksheet.

The request is an HTTP `POST` with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart body contains the **Import2DimensionDoubleArrayOption** data, and the second part contains the source data file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The important parameters are described in the following table:

### Import2DimensionDoubleArrayOption

| Parameter Name          | Type          | Description |
|-------------------------|---------------|-------------|
| **FirstRow**            | `int`         | Row index (1‑based) where the import starts. |
| **FirstColumn**         | `int`         | Column index (1‑based) where the import starts. |
| **Data**                | `Double[,]`   | Two‑dimensional array of double values to be imported. |
| **DestinationWorksheet**| `string`      | Name of the worksheet that will receive the data. |
| **IsInsert**            | `string`      | `"true"` to insert rows, `"false"` to overwrite existing cells. |
| **ImportDataType**      | `string`      | Type of data being imported (e.g., `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData`, etc.). |
| **Source**              | `FileSource`  | Indicates the data file location when the `BatchData` parameter is null. |

**Example**

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

> **Note:** The JSON field `importDataType` follows the naming used by the API; keep the case as shown in the example.

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality. SDKs handle low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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