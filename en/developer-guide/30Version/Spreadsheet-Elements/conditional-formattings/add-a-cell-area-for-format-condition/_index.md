---
title: Add CellArea to Conditional Formatting
date: 2024-03-15T00:00:00Z
lastmod: 2024-05-22T14:20:00Z
url: /conditional-formattings/add-cell-area/
description: >-
  Learn how to add a CellArea to conditional formatting in Excel using Aspose.Cells Cloud REST API v3.0. Includes step-by-step cURL, SDK (C#, Java, Python, Go), and real-world error handling.
keywords: Aspose.Cells Cloud, REST API, Excel automation, conditional formatting API, cURL example, SDK for .NET, Java, Python, Go, cell range
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

## Why This Matters

CellArea defines the exact range of cells affected by a conditional format—critical for dynamic reporting in Excel workbooks. Accurately assigning or updating cell ranges ensures formatting applies only where intended, preventing errors in data visualization and analysis.

## Add CellArea to Conditional Formatting

**Summary** – Adds a cell area (e.g., `A1:C3`) to an existing conditional‑formatting rule in a worksheet via the Aspose.Cells Cloud REST API v3.0.

---

## Prerequisites

1. **Aspose.Cells Cloud account** – obtain your **App SID** and **App Key** from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).
2. **JWT token** – generate a JWT token using the App SID/Key (see the [Authentication guide](/total/getting-started/rest-api-overview/authenticating-api-requests/)).
3. The target Excel file must already exist in the specified storage/folder.

---

## Authentication

All calls require **JWT token‑based authentication**. Pass the token in the `Authorization` header:

```http
Authorization: Bearer <jwt token>
```

---

## HTTP Request

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Path Parameters

| Name        | Type    | Required | Description                                          |
| ----------- | ------- | -------- | ---------------------------------------------------- |
| `name`      | string  | Yes      | Excel file name (e.g., `Book1.xlsx`).                |
| `sheetName` | string  | Yes      | Worksheet that contains the rule (e.g., `Sheet1`).   |
| `index`     | integer | Yes      | Zero‑based index of the conditional‑formatting rule. |

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
