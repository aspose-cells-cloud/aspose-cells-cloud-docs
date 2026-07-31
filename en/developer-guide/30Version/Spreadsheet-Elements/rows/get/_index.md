---
title: "Retrieve a Single Row from an Excel Worksheet using Aspose.Cells Cloud API"
description: "Learn how to retrieve a specific row from an Excel worksheet stored in Aspose Cloud Storage using the Aspose.Cells Cloud REST API. Includes request syntax, parameters, response schema, sample cURL, and SDK code (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, get row, Excel API, spreadsheet REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# Retrieve a Single Row from an Excel Worksheet

**Endpoint**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Retrieve a row from a worksheet that is stored in Aspose Cloud Storage. The operation requires a valid OAuth 2.0 access token with **Read** scope.

---

## Table of Contents
1. [Prerequisites](#prerequisites)  
2. [HTTP Request](#http-request)  
3. [Parameters](#parameters)  
   - [Path parameters](#path-parameters)  
   - [Query parameters](#query-parameters)  
4. [cURL Example](#curl-example)  
5. [Response](#response)  
   - [Success schema](#success-schema)  
   - [Status codes](#status-codes)  
6. [SDK Code Samples](#sdk-code-samples)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [Related Operations](#related-operations)  
8. [Notes & Limits](#notes--limits)  

---

## Prerequisites
- **Aspose Cloud account** with an active subscription.  
- **OAuth 2.0 access token** that includes the **Read** scope.  
- The target workbook must already exist in Aspose Cloud Storage.  

---

## HTTP Request
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*Base URL*: `https://api.aspose.cloud/v3.0`

---

## Parameters

### Path parameters
| Name      | Type   | Required | Description                         |
|-----------|--------|----------|-------------------------------------|
| `name`    | string | ✅       | Name of the workbook file (e.g., `MyWorkbook.xlsx`). |
| `sheetName`| string | ✅     | Name of the worksheet (e.g., `Sheet1`). |
| `rowIndex`| integer| ✅       | Zero‑based index of the row to retrieve. |

### Query parameters *(optional)*
| Name        | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `folder`    | string | ❌       | Path to the folder in cloud storage where the workbook resides. |
| `storageName`| string| ❌       | Name of the storage service (if you use a custom storage). |

---

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
    "Style": { /* style object */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...additional cells... */
    ]
  }
}
```

### Status codes
| Code | Meaning |
|------|---------|
| **200** | Row retrieved successfully. |
| **401** | Unauthorized – missing or invalid access token. |
| **404** | Workbook, worksheet, or row not found. |
| **500** | Internal server error. |

### Error example (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Access token is missing or invalid."
}
```

---

## SDK Code Samples

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // optional
);

Console.WriteLine($"Row {response.Row.Index} retrieved with {response.Row.Cells.Count} cells.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – optional
);

System.out.println("Row index: " + response.getRow().getIndex());
System.out.println("Cells count: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Row {response.row.index} retrieved with {len(response.row.cells)} cells.")
except ApiException as e:
    print("Exception when calling CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## Related Operations
| Operation | Description |
|-----------|-------------|
| **Add Row** | `POST /cells/{name}/worksheets/{sheetName}/rows` – Insert a new row into a worksheet. |
| **Delete Row** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – Remove an existing row. |
| **Get Multiple Rows** | `GET /cells/{name}/worksheets/{sheetName}/rows` – Retrieve a collection of rows. |
| **Rows Overview** | `/cells/rows/` – General documentation for row‑related endpoints. |

---

## Notes & Limits
- **Rate limit**: 100 requests per minute per account.  
- **Supported formats**: XLS, XLSX, CSV, ODS.  
- Row index is **zero‑based**; the first row is `0`.  
- Ensure the workbook is uploaded to the specified `folder` before calling this endpoint.  

---