---
title: "Import Data without Using Storage – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Import data without storage"
type: docs
url: /import/without-using-storage/
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: "Aspose.Cells, Cloud API, import data without storage, Excel import API, REST import"
description: "Import Excel data via Aspose.Cells Cloud API using PostImportData without storage—JWT auth and multipart/form-data."
weight: 100
ArticleTitle: "Import Data without Using Storage – Aspose.Cells Cloud API"
---
The **PostImport** API (`POST https://api.aspose.cloud/v3.0/cells/import`) enables developers to import data into an Excel file and generate output in various formats—such as CSV, XLSX, PDF, or images—by sending a multipart form-data request containing the source file and optional query parameters for output format, password, and regional settings. Aspose.Cells Cloud handles the import process without requiring files to be stored in cloud storage, supporting professional-grade data integration directly from client applications.

This REST API imports **data** into an Excel file.

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

The **ImportOption** parameters are described in the **ImportData option reference** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter).

**Prerequisites:**  
A valid JWT token must be generated beforehand, and the file size must not exceed the service limit (typically 100 MB). Supported file formats include XLS, XLSX, CSV, and ODS. Ensure the appropriate SDK is installed if you prefer programmatic access.

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

**Notes:**  
When sending the request, the `Content-Type: multipart/form-data` header is automatically set by the `-F` flag. For large payloads, consider compressing the data before import and implement retry logic for transient errors.

## How to Use the Post Import API with SDKs?

### Post Import API Specification

The <a href="https://reference.aspose.cloud/cells/#/LightCells/PostImport" rel="noopener noreferrer">Post Import API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

_The `-F` flag automatically sets `Content-Type: multipart/form-data`._

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "Code": 200
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
