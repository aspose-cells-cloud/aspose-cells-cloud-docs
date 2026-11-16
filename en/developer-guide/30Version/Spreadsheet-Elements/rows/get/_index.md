---
title: "Retrieve a Single Row from an Excel Worksheet using Aspose.Cells Cloud API"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Get"
type: docs
url: /rows/get/
description: "Learn how to retrieve a specific row from an Excel worksheet stored in Aspose Cloud Storage using the Aspose.Cells Cloud REST API. Includes request syntax, parameters, response schema, sample cURL, and SDK code (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, get row, Excel API, spreadsheet REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
weight: 100
ArticleTitle: "Get Row from Excel Worksheet via Aspose.Cells Cloud REST API"
---

## Retrieve a Single Row from an Excel Worksheet

**Endpoint**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`

Retrieve a row from a worksheet that is stored in Aspose Cloud Storage. The operation requires a valid OAuth 2.0 access token with **Read** scope.

## HTTP Request

```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

## Parameters

### Path parameters

| Name        | Type    | Required | Description                                          |
| ----------- | ------- | -------- | ---------------------------------------------------- |
| `name`      | string  | ✅       | Name of the workbook file (e.g., `MyWorkbook.xlsx`). |
| `sheetName` | string  | ✅       | Name of the worksheet (e.g., `Sheet1`).              |
| `rowIndex`  | integer | ✅       | Zero‑based index of the row to retrieve.             |

### Query parameters _(optional)_

| Name          | Type   | Required | Description                                                     |
| ------------- | ------ | -------- | --------------------------------------------------------------- |
| `folder`      | string | ❌       | Path to the folder in cloud storage where the workbook resides. |
| `storageName` | string | ❌       | Name of the storage service (if you use a custom storage).      |

## cURL Example

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Response

### Success schema (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": {
      /* style object */
    },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...additional cells... */
    ]
  }
}
```

### Error example (`401 Unauthorized`)

```json
{
  "Code": 401,
  "Message": "Access token is missing or invalid."
}
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |
