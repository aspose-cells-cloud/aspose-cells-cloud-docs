---
title: "Import Batch Data into Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Import batch data"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, Cloud API, import batch data, Excel, CSV, JSON, XML, arrays"
description: "Import batch data into Excel worksheets via Aspose.Cells Cloud REST API using CSV, JSON, XML, or arrays."
weight: 19
ArticleTitle: "Import Batch Data into Excel Worksheet – Aspose.Cells Cloud Documentation"
---
The **PostImport** API (`POST https://api.aspose.cloud/v3.0/cells/import`) in Aspose.Cells Cloud enables importing batch data into an Excel file by accepting a multipart request: the first part carries an ImportBatchDataOption configuration object, and the second part uploads the source data file (such as CSV, JSON, or XML), supporting output generation in multiple formats including XLSX, PDF, and CSV via the optional outFormat parameter.

The operation uses an HTTP request with multipart content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## The Post Import Web API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| outFormat | String | Query | The output data file format.(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers) |
| password | String | Query | The password needed to open an Excel file. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| region | String | Query | The regional settings for workbook. |

### Response

```json
[
  {
    "Name": "FilesResult",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesResult"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

### ImportBatchDataOption

| Parameter Name           | Type              | Description                                                                                                                                                                                   |
| ------------------------ | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**            | `List<CellValue>` | Collection of cell values to be written directly.                                                                                                                                             |
| **DestinationWorksheet** | `string`          | Name of the worksheet where the data will be imported.                                                                                                                                        |
| **IsInsert**             | `bool`            | When `true`, the data is inserted and existing cells are shifted; when `false`, the data overwrites existing cells.                                                                           |
| **ImportDataType**       | `string`          | Format of the data to import. Allowed values: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | `FileSource`      | Specifies the location of the data file when **BatchData** is `null`.                                                                                                                         |

### CellValue

| Parameter Name  | Type     | Description                                               |
| --------------- | -------- | --------------------------------------------------------- |
| **rowIndex**    | `int`    | Zero‑based row index of the target cell.                  |
| **columnIndex** | `int`    | Zero‑based column index of the target cell.               |
| **type**        | `string` | Data type of the value (e.g., `int`, `double`, `string`). |
| **value**       | `string` | The actual value to write into the cell.                  |
| **style**       | `Style`  | Optional styling information for the cell.                |

### FileSource

| Parameter Name     | Type     | Description                                                                |
| ------------------ | -------- | -------------------------------------------------------------------------- |
| **FileSourceType** | `string` | Source of the file: `InMemoryFiles`, `CloudFileSystem`, or `RequestFiles`. |
| **FilePath**       | `string` | Path or identifier of the file within the chosen source.                   |

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

## How to Use the PostImportData API with SDKs

### PostImportData API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) defines a publicly accessible programming interface that allows you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

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
