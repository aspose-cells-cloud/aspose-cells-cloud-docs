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
keywords: "Aspose.Cells Cloud, Excel, import integer array, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Import integer arrays into Excel worksheets via Aspose.Cells Cloud REST API with multipart POST and SDK examples"
weight: 30
ArticleTitle: "Import Integer Array into Excel Worksheet – Aspose.Cells Cloud API"
---
The **PostImport** API (`POST https://api.aspose.cloud/v3.0/cells/import`) enables importing data, such as an integer array, into an Excel worksheet using Aspose.Cells Cloud, supporting output formats including XLSX, PDF, CSV, and others; it accepts an uploaded file via form data and optional query parameters to control output format, password protection, and Excel restrictions.

The request must be an HTTP **POST** with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart body contains the **ImportIntegerArrayOption** JSON payload, and the second part contains the source data file (e.g., a CSV or binary Excel file).

## The Post Import Web API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

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

A successful request returns **HTTP 200** with a JSON payload similar to:


Possible status codes:

Both endpoints accept the same multipart payload. The first endpoint performs a generic import operation, while the second targets a specific workbook identified by `{name}`.

### ImportIntegerArrayOption

| Parameter Name           | Type       | Description                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | Zero‑based index of the first row where the data will be placed.                                                                                                                               |
| **FirstColumn**          | int        | Zero‑based index of the first column where the data will be placed.                                                                                                                            |
| **IsVertical**           | boolean    | `true` to insert the array vertically (down a column); `false` to insert it horizontally (across a row).                                                                                       |
| **Data**                 | Integer[]  | The integer array to be imported.                                                                                                                                                              |
| **DestinationWorksheet** | string     | Name of the worksheet that will receive the data.                                                                                                                                              |
| **IsInsert**             | boolean    | `true` to insert rows/columns before writing the data; `false` to overwrite existing cells.                                                                                                    |
| **ImportDataType**       | string     | Type of the data being imported. Valid values: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | Indicates the position of the data file when the **BatchData** parameter is `null`.                                                                                                            |

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

## How to Use the PostImportData API with SDKs

### PostImportData API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

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