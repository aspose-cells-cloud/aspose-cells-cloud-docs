---
title: "How to Retrieve a Row from an Excel Worksheet using Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Get"
type: docs
url: /rows/get/
keywords: "Aspose.Cells Cloud, get row, Excel API, retrieve row, spreadsheet REST, C# SDK, Java SDK, Python SDK"
description: "Learn how to get a single row from an Excel worksheet with Aspose.Cells Cloud REST API. Includes request syntax, parameters, sample code in C#, Java, Python, and error handling."
weight: 20
---

## How to Retrieve a Row from an Excel Worksheet using Aspose.Cells Cloud API

Retrieve a single row from a worksheet stored in Aspose Cloud Storage. This operation requires a valid OAuth2 access token with **Read** permission and works with any workbook that has already been uploaded to the cloud.

- [How to get a row on an Excel worksheet](/cells/rows/get/row/)  
- [How to get multiple rows on an Excel worksheet](/cells/rows/get/rows/)  

### Prerequisites
1. Upload the workbook to Aspose Cloud Storage.  
2. Obtain an OAuth2 access token with the **Read** scope.  
3. Know the exact **file name**, **worksheet name**, and the **zero‑based row index** you want to retrieve.

## Request

**HTTP Method:** `GET`  
**Endpoint:**  

```
https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

| Parameter   | Type   | Required | Description                               |
|-------------|--------|----------|-------------------------------------------|
| `fileName`  | string | Yes      | Name of the workbook (including extension). |
| `sheetName` | string | Yes      | Name of the worksheet containing the row. |
| `rowIndex`  | int    | Yes      | Zero‑based index of the row to retrieve. |
| `storageName` | string | No    | Cloud storage name if not the default.   |
| `folder`    | string | No       | Folder path in storage where the file resides. |

**Example Request**

```http
GET https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/4?storageName=MyStorage
Authorization: Bearer {access_token}
```

## Response

A successful call returns **200 OK** with a JSON payload representing the row.

### JSON Schema (excerpt)

```json
{
  "Row": {
    "Index": 4,
    "Cells": [
      { "Column": 0, "Value": "John", "DataType": "String" },
      { "Column": 1, "Value": 28, "DataType": "Number" },
      { "Column": 2, "Value": "2026-03-30", "DataType": "DateTime" }
    ],
    "Style": { /* styling information */ }
  }
}
```

### Example Payload

```json
{
  "Row": {
    "Index": 4,
    "Cells": [
      { "Column": 0, "Value": "Alice" },
      { "Column": 1, "Value": 35 },
      { "Column": 2, "Value": "Marketing" }
    ]
  }
}
```

## Error Handling

| HTTP Status | Description                              | Sample Error Body |
|-------------|------------------------------------------|-------------------|
| 400         | Bad request – missing or invalid parameters. | `{ "Code": "InvalidParameter", "Message": "rowIndex must be a non‑negative integer." }` |
| 401         | Unauthorized – invalid or expired token. | `{ "Code": "Unauthorized", "Message": "Access token is missing or invalid." }` |
| 404         | Not found – workbook, worksheet, or row does not exist. | `{ "Code": "FileNotFound", "Message": "The requested file was not found." }` |
| 500         | Internal server error – unexpected failure. | `{ "Code": "InternalError", "Message": "An unexpected error occurred." }` |

## SDK Code Samples

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var response = api.GetWorksheetRow("Book1.xlsx", "Sheet1", 4);
Console.WriteLine($"Row {response.Row.Index} retrieved successfully.");
```

### Java  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.RowResponse;

CellsApi api = new CellsApi("client_id", "client_secret");
RowResponse response = api.getWorksheetRow("Book1.xlsx", "Sheet1", 4);
System.out.println("Row index: " + response.getRow().getIndex());
```

### Python  

```python
from asposecellscloud import CellsApi, ApiClient

api_client = ApiClient(client_id="client_id", client_secret="client_secret")
api = CellsApi(api_client)

row = api.get_worksheet_row("Book1.xlsx", "Sheet1", 4)
print(f"Retrieved row {row.row.index}")
```

## Next Steps / Related Operations

- [Get multiple rows](/cells/rows/get/rows/)  
- [Add a row](/cells/rows/add/)  
- [Delete a row](/cells/rows/delete/)  
- [Update a row](/cells/rows/put/)  

<p class="last-updated">Last updated: 2024-12-01</p>

## FAQ

<details>
<summary>Can I retrieve a row from a protected worksheet?</summary>
Yes. Provide the appropriate access token with **Read** permission. If the worksheet is password‑protected, include the `password` query parameter in the request.
</details>

<details>
<summary>What is the row index base?</summary>
The row index is zero‑based; the first row has an index of 0.
</details>

---