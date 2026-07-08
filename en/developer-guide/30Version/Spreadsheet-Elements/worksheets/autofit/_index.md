---
title: "Working with Autofit on an Excel Worksheet"
second_title: "Document"
linktitle: "Autofit"
type: docs
url: /worksheets/autofit/
aliases: [/autofit-rows-and-columns-of-worksheet/]
keywords: "autofit, column, row, Aspose.Cells, Cloud, Excel, API, resize"
description: "Learn how to automatically resize rows and columns in an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL, .NET, Java, and Python examples."
weight: 20
ArticleTitle: "Working with Autofit on an Excel Worksheet – Aspose.Cells Cloud API"
---

## Working with autofit on an Excel worksheet

- [How to autoFit a column on an Excel worksheet.](/cells/worksheets/autofit/column/)
- [How to autoFit columns on an Excel worksheet.](/cells/worksheets/autofit/columns/)
- [How to autoFit a row on an Excel worksheet.](/cells/worksheets/autofit/row/)
- [How to autoFit rows on an Excel worksheet.](/cells/worksheets/autofit/rows/)

**Prerequisites**  
Before using the Autofit operations you must have:

1. An Aspose.Cells Cloud account with a valid **Client Id** and **Client Secret**.  
2. A workbook uploaded to Aspose Cloud storage (or accessible via a public URL).  
3. The worksheet name you intend to modify.

**API Reference**  

| Operation | HTTP Method | Endpoint | Required Parameters | Request Body | Sample Response | Status Codes |
|-----------|-------------|----------|--------------------|--------------|----------------|--------------|
| AutoFit a **column** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (path) <br> `columnIndex` (query) | *none* | `{ "code": 200, "status": "OK", "message": "Column autofitted." }` | 200, 400, 401, 404, 500 |
| AutoFit **columns** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (path) <br> `startColumn`, `endColumn` (query) | *none* | `{ "code": 200, "status": "OK", "message": "Columns autofitted." }` | 200, 400, 401, 404, 500 |
| AutoFit a **row** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (path) <br> `rowIndex` (query) | *none* | `{ "code": 200, "status": "OK", "message": "Row autofitted." }` | 200, 400, 401, 404, 500 |
| AutoFit **rows** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (path) <br> `startRow`, `endRow` (query) | *none* | `{ "code": 200, "status": "OK", "message": "Rows autofitted." }` | 200, 400, 401, 404, 500 |

**Code Samples**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Authenticate
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// Call Autofit columns
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Autofit rows
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# Autofit a single column
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

These snippets demonstrate how to:

1. Authenticate with Aspose.Cells Cloud using your **Client Id** and **Client Secret**.  
2. Call the appropriate Autofit endpoint for columns or rows.  
3. Process the response, which confirms that the operation succeeded.

**Next Steps**

After the Autofit call completes, you can download the updated workbook:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

Feel free to adjust the `startColumn`, `endColumn`, `startRow`, and `endRow` parameters to target specific ranges.