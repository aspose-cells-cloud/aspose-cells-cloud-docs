---
title: "Import JSON Data into Excel"
second_title: "Developer Guide"
linktitle: "Import JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, JSON import, Excel API, REST import JSON, SDK examples"
description: "Learn how to import JSON data into an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint details, request/response examples, and SDK code for .NET, Java, and Python."
weight: 40
ArticleTitle: "Import JSON into Excel with Aspose.Cells Cloud REST API"
---
The **PostWorkbookImportJson** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/importjson`) enables Aspose.Cells Cloud users to import JSON data—either from a cloud file or an HTTP URI—directly into an Excel workbook, supporting both structured and unstructured JSON formats without requiring manual conversion.

## The Post Workbook Import JSON Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| importJsonRequest | class:importjsonrequest | HTTPBody | Import Json request. |
| password | String | Query | The password needed to open an Excel file. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |
| outPath | String | Query | Path to save the result. If it's a single file, the `outPath` should encompass both the filename and extension. In the case of multiple files, the `outPath` should only include the folder. |
| outStorageName | String | Query | The storage name where the output file is situated. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| region | String | Query | The regional settings for workbook. |

### Response

```json
[
  {
    "Name": "Stream",
    "DataType": {
      "Identifier": "File"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
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

### **Example Request Body**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

## How to Use the PostWorkbookImportJson API with SDKs

### PostWorkbookImportJson API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the most efficient way to accelerate development. SDKs handle low‑level details, allowing you to focus on your business logic. For a complete list of Aspose.Cells Cloud SDKs, please visit the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
