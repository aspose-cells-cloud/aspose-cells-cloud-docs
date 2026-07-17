---
title: "Import JSON Data into Excel"
second_title: "Document"
linktitle: "Import JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, JSON import, Excel API, REST import JSON, SDK examples"
description: "Learn how to import JSON data into an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint details, request/response examples, and SDK code for .NET, Java, and Python."
weight: 40
---

This REST API **imports JSON data** into an Excel worksheet.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

| Parameter Name        | Location     | Type   | Description                                                                                          |
| --------------------- | ------------ | ------ | ---------------------------------------------------------------------------------------------------- |
| name                  | Path         | string | The name of the workbook file.                                                                       |
| importJsonRequest     | HTTP body    | class  | The request payload that contains JSON import details.                                               |
| password              | Query string | string | Password for opening the workbook (if protected).                                                    |
| folder                | Query string | string | The folder that contains the original workbook.                                                      |
| storageName           | Query string | string | The name of the storage where the workbook resides.                                                  |
| outPath               | Query string | string | Path for the output file after import. If omitted, the updated workbook is returned in the response. |
| outStorageName        | Query string | string | Storage name for the output file.                                                                    |
| checkExcelRestriction | Query string | string | Flag indicating whether to enforce Excel‑specific restrictions (true/false).                         |

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

### Response

A successful request returns **HTTP 200** with a JSON payload similar to:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Possible status codes:

| Code | Meaning                                 |
| ---- | --------------------------------------- |
| 200  | Import succeeded                        |
| 400  | Bad request – missing or invalid data   |
| 401  | Unauthorized – invalid or missing token |
| 500  | Internal server error                   |


## How to Use the PostWorkbookImportJson API with SDKs

### PostWorkbookImportJson API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the most efficient way to accelerate development. SDKs handle low‑level details, allowing you to focus on your business logic. For a complete list of Aspose.Cells Cloud SDKs, please visit the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
