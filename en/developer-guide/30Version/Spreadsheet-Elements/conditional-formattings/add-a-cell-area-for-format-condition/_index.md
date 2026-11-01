---
title: Add CellArea to Conditional Formatting
date: 2024-03-15T00:00:00Z
lastmod: 2024-05-22T14:20:00Z
url: /conditional-formattings/add-cell-area/
description: "Add a CellArea like A1:C3 to an Excel conditional formatting rule using Aspose.Cells Cloud API v3.0"
keywords: Aspose.Cells Cloud, REST API, Excel automation, conditional formatting API, cURL example, SDK for .NET, Java, Python, Go, cell range
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
type: docs
linktitle: "Add CellArea to CF"
ArticleTitle: "Add CellArea to Conditional Formatting in Aspose.Cells Cloud REST API v3.0"
---
The **PutWorksheetFormatConditionArea** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`) enables developers to assign a specific cell range—defined by the `cellArea` query parameter—to an existing conditional formatting rule in a worksheet via Aspose.Cells Cloud. This operation supports precise control over where formatting is applied, ensuring dynamic reports and data visualizations remain accurate and relevant to the intended data subset.

## Why This Matters

CellArea defines the exact range of cells affected by a conditional format—critical for dynamic reporting in Excel workbooks. Accurately assigning or updating cell ranges ensures formatting applies only where intended, preventing errors in data visualization and analysis.

## Add CellArea to Conditional Formatting

**Summary** – Adds a cell area (e.g., `A1:C3`) to an existing conditional‑formatting rule in a worksheet via the Aspose.Cells Cloud REST API v3.0.

---

## Authentication

All calls require **JWT token‑based authentication**. Pass the token in the `Authorization` header:

```http
Authorization: Bearer <jwt token>
```

---

## The Put Worksheet Format Condition Area Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| index | Integer | Path | Gets the Conditional Formatting element at the specified index. |
| cellArea | String | Query | Adds a conditional formatted cell range. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
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
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

### Query Parameters

| Name          | Type   | Required | Description                                        |
| ------------- | ------ | -------- | -------------------------------------------------- |
| `cellArea`    | string | Yes      | Cell range to add, in A1 notation (e.g., `A1:C3`). |
| `folder`      | string | No       | Folder path where the file is stored.              |
| `storageName` | string | No       | Storage service name.                              |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Expected Successful Response

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

#### Response Schema – `CellArea`

| Property      | Type | Description                           |
| ------------- | ---- | ------------------------------------- |
| `StartRow`    | int  | Zero‑based index of the first row.    |
| `StartColumn` | int  | Zero‑based index of the first column. |
| `EndRow`      | int  | Zero‑based index of the last row.     |
| `EndColumn`   | int  | Zero‑based index of the last column.  |

---

## HTTP Status Codes

| Code | Meaning               | Description                                                     |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | CellArea added successfully; response contains updated details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., malformed `cellArea`).     |
| 401  | Unauthorized          | Invalid or missing JWT token.                                   |
| 409  | Conflict              | New `cellArea` overlaps an existing area in the same rule.      |
| 413  | Payload Too Large     | Request exceeds size limits.                                    |
| 500  | Internal Server Error | Unexpected server error.                                        |

---

## SDK Examples

> **Before running examples**, replace `<YOUR_APP_SID>` and `<YOUR_APP_KEY>` with your credentials from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).
