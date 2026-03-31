---
title: "Import Batch Data into Excel Worksheet"
second_title: "Document"
linktitle: "Import batch data"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, Cloud API, import batch data, Excel, CSV, JSON, XML, SDK"
description: "Learn how to import batch data (CSV, JSON, XML, arrays) into an Excel worksheet using Aspose.Cells Cloud REST API. Includes authentication, request/response examples, SDK snippets, and error handling."
weight: 19
---

This REST API **imports batch data** into an Excel worksheet.

The operation uses an HTTP request with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart payload contains the **ImportBatchDataOption** object, and the second part carries the data file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

**Authentication** – The API requires OAuth 2.0. Include an `Authorization: Bearer <access_token>` header in the request. Details on obtaining an access token are available in the Aspose Cloud authentication guide.

The important parameters are described in the tables below.

### ImportBatchDataOption

| Parameter Name          | Type               | Description |
|-------------------------|--------------------|-------------|
| **BatchData**           | `List<CellValue>`  | Collection of cell values to be written directly. |
| **DestinationWorksheet**| `string`           | Name of the worksheet where the data will be imported. |
| **IsInsert**            | `bool`             | When `true`, the data is inserted and existing cells are shifted; when `false`, the data overwrites existing cells. |
| **ImportDataType**      | `string`           | Format of the data to import. Allowed values: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**              | `FileSource`       | Specifies the location of the data file when **BatchData** is `null`. |

### CellValue

| Parameter Name | Type   | Description |
|----------------|--------|-------------|
| **rowIndex**   | `int`  | Zero‑based row index of the target cell. |
| **columnIndex**| `int`  | Zero‑based column index of the target cell. |
| **type**       | `string`| Data type of the value (e.g., `int`, `double`, `string`). |
| **value**      | `string`| The actual value to write into the cell. |
| **style**      | `Style`| Optional styling information for the cell. |

### FileSource

| Parameter Name   | Type   | Description |
|------------------|--------|-------------|
| **FileSourceType**| `string`| Source of the file: `InMemoryFiles`, `CloudFileSystem`, or `RequestFiles`. |
| **FilePath**      | `string`| Path or identifier of the file within the chosen source. |

### Example (XML)

```xml
<ImportBatchDataOption>
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
</ImportBatchDataOption>
```

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality. SDKs handle low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with different SDKs:

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