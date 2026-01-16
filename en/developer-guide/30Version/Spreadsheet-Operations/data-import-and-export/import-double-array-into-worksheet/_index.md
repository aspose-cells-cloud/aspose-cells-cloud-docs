---
title: "Import Double Array into Excel Worksheet"
second_title: "Document"
linktitle: "Import double array"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Import Double Array, Aspose.Cells Cloud, REST API, Excel, Spreadsheet, SDK, C#, PHP, Ruby"
description: "Use the Aspose.Cells Cloud REST API to import double‑array data into an Excel worksheet. The API accepts multipart requests with an ImportDoubleArrayOption payload and supports multiple SDKs (C#, PHP, Ruby, etc.) for easy integration."
weight: 20
---

This REST API **imports double‑array data** into an Excel worksheet.

The request is an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart content contains the **ImportDoubleArrayOption** data and the second part contains the data file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The important parameters are described in the following table:

**ImportDoubleArrayOption**

| Parameter Name        | Type          | Description                                                                                                 |
|-----------------------|---------------|-------------------------------------------------------------------------------------------------------------|
| FirstRow              | int           | Zero‑based index of the first row where the data will be placed.                                            |
| FirstColumn           | int           | Zero‑based index of the first column where the data will be placed.                                         |
| IsVertical            | string        | `true` / `false` – determines whether the array is inserted vertically (`true`) or horizontally (`false`). |
| Data                  | Double[]      | Array of double values to import.                                                                            |
| DestinationWorksheet  | string        | Name of the target worksheet.                                                                                |
| IsInsert              | string        | `true` / `false` – if `true`, data is inserted; if `false`, existing cells are overwritten.                 |
| ImportDataType        | string        | Type of data being imported (e.g., `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, etc.). |
| Source                | FileSource    | Specifies the data file location when the `BatchData` parameter is null.                                   |

### Example (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

### Example (JSON)

```json
{
    "Data": [1.99, 1.9, 2.0],
    "DestinationWorksheet": "Sheet1",
    "FirstRow": 0,
    "FirstColumn": 0,
    "IsVertical": false,
    "IsInsert": true,
    "importDataType": "DoubleArray"
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

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}