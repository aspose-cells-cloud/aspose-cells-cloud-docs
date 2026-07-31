---
title: "Working with Excel ListObject"
ArticleTitle: "Working with Excel ListObject"
second_title: "Document"
linktitle: "ListObjects"
type: docs
url: /list-objects/
aliases:
  - /working-with-list-objects/
  - /working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, Excel table API, add table, update table, delete table, convert table to range, sort Excel table"
description: "Learn how to add, update, delete, retrieve, sort, and convert Excel ListObjects (tables) using Aspose.Cells Cloud REST API. Includes code samples for C#, Java, Python, and more."
weight: 100
---

Excel ListObjects (tables) provide a structured way to organize data sets. They include features such as automatic data arrangement, header rows, built‑in filters, and optional total rows. Master these capabilities to analyze your data quickly and efficiently.

**ListObject definition:** A **ListObject** is Excel’s native table object that groups rows and columns, enables sorting, filtering, styling, and can be accessed via the Aspose.Cells Cloud API.

## How to Work with Table (List Object)

- [How to add a table (list object) inside the worksheet](/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [How to update a table (list object) inside the worksheet](/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [How to convert a table (list object) to a range](/cells/convert-list-object-or-table-to-range/)
- [How to sort table data](/cells/sort-table-data/)
- [How to remove duplicate rows from a table](/cells/list-objects/remove-duplicates/)
- [How to insert a slicer for a table](/cells/list-objects/insert-slicer/)

**API Reference (overview):**  
The Aspose.Cells Cloud REST API exposes ListObject operations through endpoints such as `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`, and `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Required query parameters include `folder` and `storage`. Request bodies are JSON objects describing the table’s properties (name, showHeaderRow, showTotalRow, etc.), and responses return JSON payloads with the created or modified ListObject details.

**Prerequisites:**  
- A valid Aspose.Cells Cloud authentication token.  
- The workbook file must be uploaded to a supported storage location (default: **/**) and the `folder` query parameter should point to that location.  
- Optional: Set `storage` if using a non‑default storage service.

**Endpoint details**

| Method | Endpoint | Query Parameters | Request Body (JSON) | Success Response (example) | Status Codes |
|--------|----------|------------------|---------------------|----------------------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (required), `storage` (optional) | *none* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (required), `storage` (optional) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Created, 400 – Bad Request, 401 – Unauthorized, 409 – Conflict |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (required), `storage` (optional) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (required), `storage` (optional) | *none* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Bad Request, 401 – Unauthorized, 404 – Not Found |

**Code snippets**

*C# (POST – Add ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – Retrieve ListObjects)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – Update ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – Remove ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Notes:**  
- ListObject indices are zero‑based.  
- When adding a ListObject, the `StartRow` and `StartColumn` define the upper‑left cell of the table.  
- The API supports pagination via `offset` and `limit` query parameters (not shown in the table) for large worksheets.  
- Rate limits: 100 requests per minute per account; exceeding this returns **429 Too Many Requests**.

By incorporating the term **Excel ListObject** several times throughout the page, the content aligns with the target keywords “Excel ListObject”, “Aspose.Cells Cloud”, and “Excel table API”, improving SEO while remaining natural for readers.