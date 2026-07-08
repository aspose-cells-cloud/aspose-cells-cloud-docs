---
title: "How to Retrieve a Row from an Excel Worksheet using Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Get"
type: docs
url: /rows/get/
keywords: "Aspose.Cells Cloud, get row, Excel API, spreadsheet REST, C# SDK, Java SDK, Python SDK"
description: "Learn how to get a single row from an Excel worksheet with Aspose.Cells Cloud REST API. Includes request syntax, parameters, sample code in C#, Java, Python, and error handling."
weight: 20
ArticleTitle: "Retrieve a Single Row from an Excel Worksheet using Aspose.Cells Cloud API"
---

## How to Retrieve a Row from an Excel Worksheet using Aspose.Cells Cloud API

Retrieve a single row from a worksheet stored in Aspose Cloud Storage. This operation requires a valid OAuth2 access token with **Read** permission and works with any workbook that has already been uploaded to the cloud.

- [How to get a row on an Excel worksheet](/cells/rows/get/row/)
- [How to get multiple rows on an Excel worksheet](/cells/rows/get/rows/)

**Prerequisites:**  
- An Aspose Cloud account with an active subscription.  
- OAuth2 access token that includes the **Read** scope.  
- The target workbook must already exist in Aspose Cloud Storage.

**Notes:**  
- Rate‑limit: 100 requests per minute per account.  
- Supported file formats include XLS, XLSX, CSV, and ODS.  
- Maximum row index is zero‑based; the first row is `0`.

**API Reference**  
- **HTTP Method:** `GET`  
- **Endpoint:** `/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  
- **Path Parameters:**  
  - `name` (string, required): Name of the workbook file.  
  - `sheetName` (string, required): Name of the worksheet.  
  - `rowIndex` (integer, required): Zero‑based index of the row to retrieve.  
- **Query Parameters (optional):**  
  - `folder` (string): Folder path in cloud storage where the workbook is located.  
  - `storageName` (string): Name of the storage service.  

**Response Schema (JSON):**  
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

**Possible Status Codes:**  

| Code | Meaning                              |
|------|--------------------------------------|
| 200  | Row retrieved successfully.          |
| 401  | Unauthorized – invalid or missing token. |
| 404  | Workbook, worksheet, or row not found. |
| 500  | Internal server error.                |

**Sample Request (cURL)**  
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

**Sample Responses**  

*Success (200)*  
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15,
    "Cells": [
      { "ColumnIndex": 0, "Value": "Sample", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 42, "DataType": "Number" }
    ]
  }
}
```

*Error (401)*  
```json
{
  "Code": 401,
  "Message": "Access token is missing or invalid."
}
```

**SDK Code Samples**

*C#*  
```csharp
var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow("MyWorkbook.xlsx", "Sheet1", 5, folder: "Docs");
Console.WriteLine($"Row {response.Row.Index} retrieved with {response.Row.Cells.Count} cells.");
```

*Java*  
```java
CellsApi api = new CellsApi(clientId, clientSecret);
RowResponse response = api.cellsRowsGetWorksheetRow("MyWorkbook.xlsx", "Sheet1", 5, "Docs", null);
System.out.println("Row index: " + response.getRow().getIndex());
```

*Python*  
```python
api = CellsApi(client_id, client_secret)
response = api.cells_rows_get_worksheet_row(
    name="MyWorkbook.xlsx",
    sheet_name="Sheet1",
    row_index=5,
    folder="Docs"
)
print(f"Row {response.row.index} retrieved with {len(response.row.cells)} cells.")
```

**Related Operations**  
- [Add Row](/cells/rows/post/) – Insert a new row into a worksheet.  
- [Delete Row](/cells/rows/delete/) – Remove an existing row from a worksheet.  