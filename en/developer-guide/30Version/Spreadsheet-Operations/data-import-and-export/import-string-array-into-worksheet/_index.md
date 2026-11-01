---
title: "Import String Array into Excel Worksheet – Aspose.Cells Cloud"
second_title: "Developer Guide"
linktitle: "Import string array"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, import string array, Excel REST API, multipart upload, worksheet data import, cloud SDK"
description: "Learn how to import a string array into an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes request format, parameters, and SDK examples."
weight: 40
ArticleTitle: "Import String Array into Excel Worksheet – Aspose.Cells Cloud"
---
The **PostImport** API (`POST https://api.aspose.cloud/v3.0/cells/import`) enables importing data—including string arrays—into an Excel file via Aspose.Cells Cloud, supporting output formats such as CSV, XLSX, PDF, and more. Developers can upload a file and specify parameters like `outFormat` to generate the desired output, making it ideal for programmatically populating spreadsheets with list-based data, such as configuration values or externally sourced string collections.

This REST API imports string‑array data into an Excel worksheet.

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

The request uses multipart HTTP content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart body contains an **ImportStringArrayOption** payload; the second part contains the source data file.

The important parameters are described in the following table:

<caption>ImportStringArrayOption parameters</caption>

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

### **ImportStringArrayOption**

| Parameter Name       | Type       | Description                                                                                                                                                                         |
| -------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | The starting row index (1‑based) where the data will be placed.                                                                                                                     |
| FirstColumn          | int        | The starting column index (1‑based) where the data will be placed.                                                                                                                  |
| IsVertical           | boolean    | `true` to insert data vertically; `false` to insert horizontally.                                                                                                                   |
| Data                 | String[]   | The string array to be imported.                                                                                                                                                    |
| DestinationWorksheet | string     | The name of the worksheet that will receive the data.                                                                                                                               |
| IsInsert             | boolean    | `true` to insert rows/columns (shifting existing cells); `false` to overwrite existing cells.                                                                                       |
| ImportDataType       | string     | Type of data being imported (e.g., `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Describes where the data file resides when **BatchData** is null (e.g., `CloudFileSystem`, `LocalFile`). Required if `BatchData` is not supplied.                                   |

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

## How to Use the PostImportData API with SDKs

### PostImportData API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

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
