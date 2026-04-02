---
title: "Import Integer Array into Excel Worksheet"
linktitle: "Import integer array"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, Import integer array, REST API, SDK"
description: "Import an integer array into an Excel worksheet using Aspose.Cells Cloud REST API. Supports multipart requests and multiple SDKs (C#, PHP, Ruby, etc.)."
weight: 30
---

This REST API imports an integer array into an Excel worksheet.

The request is an HTTP **POST** with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart body contains the **ImportIntegerArrayOption** data, and the second part contains the source data file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The important parameters are described in the following table.

### ImportIntegerArrayOption

| Parameter Name           | Type      | Description                                                                                                                                                                            |
|--------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FirstRow**             | int       | Zero‑based index of the first row where the data will be placed.                                                                                                                       |
| **FirstColumn**          | int       | Zero‑based index of the first column where the data will be placed.                                                                                                                    |
| **IsVertical**           | boolean   | `true` to insert the array vertically (down a column); `false` to insert it horizontally (across a row).                                                                              |
| **Data**                 | Integer[] | The integer array to be imported.                                                                                                                                                     |
| **DestinationWorksheet**| string    | Name of the worksheet that will receive the data.                                                                                                                                      |
| **IsInsert**             | boolean   | `true` to insert rows/columns before writing the data; `false` to overwrite existing cells.                                                                                           |
| **ImportDataType**       | string    | Type of the data being imported. Valid values: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource| Indicates the position of the data file when the **BatchData** parameter is `null`.                                                                                                   |

#### Example Request Body

```json
{
    "Data": [1, 2, 4],
    "DestinationWorksheet": "Sheet1",
    "FirstRow": 1,
    "FirstColumn": 2,
    "IsVertical": true,
    "IsInsert": true,
    "ImportDataType": "IntArray"
}
```

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality. SDKs abstract low‑level details, letting you focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}