---
title: "How to work with deleting worksheets in an Excel workbook"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /worksheets/delete/
keywords: "Aspose.Cells, Cloud, REST API, Delete Worksheet, Excel, C#, Java, Python"
description: "Learn how to delete single or multiple worksheets from an Excel workbook using Aspose.Cells Cloud REST API. Includes C#, Java, and Python examples, prerequisites, error‑handling tips, and related operations."
weight: 20
ArticleTitle: "Delete Worksheet(s) in an Excel Workbook with Aspose.Cells Cloud API"
---

## Working with Deleting Worksheets in an Excel Workbook

When an application generates or modifies Excel files dynamically, you may need to remove worksheets that are no longer required—such as temporary reports, placeholder sheets, or outdated data. The Aspose.Cells Cloud API makes it easy to delete a single worksheet or several worksheets in one request.

**API Reference**  

| Item | Details |
|------|---------|
| **HTTP Method** | `DELETE` |
| **Endpoint** | `/cells/{fileName}/worksheets` |
| **Path Parameters** | `fileName` – name of the Excel file (required) |
| **Query Parameters** | `sheetName` – name of the worksheet to delete (optional, for single delete) <br> `folder` – source folder in storage (optional) <br> `storage` – storage name (optional) |
| **Request Body** | *None* |
| **Success Response** | `200 OK` – worksheet(s) deleted successfully. Returns a JSON object with operation status. |
| **Error Responses** | `400 Bad Request` – invalid parameters <br> `401 Unauthorized` – authentication failure <br> `404 Not Found` – file or worksheet not found <br> `500 Internal Server Error` – server‑side issue |

**Request**  

To delete one or more worksheets, send a `DELETE` request to the endpoint above, including the required `fileName` and optionally the `sheetName` query parameter for a single‑sheet deletion. When `sheetName` is omitted, all worksheets in the workbook are removed.

**Parameters**  

- `fileName` (string, required): The Excel file name, including extension.  
- `sheetName` (string, optional): Specific worksheet name to delete. If omitted, the API deletes all worksheets.  
- `folder` (string, optional): Path to the folder containing the file in storage.  
- `storage` (string, optional): Name of the Aspose Cloud storage to use.

**Responses**  

- **200 OK** – Example JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Worksheet(s) deleted successfully."
  }
  ```
- **400 Bad Request** – Invalid request parameters.  
- **401 Unauthorized** – Authentication token missing or invalid.  
- **404 Not Found** – Specified file or worksheet does not exist.  
- **500 Internal Server Error** – Unexpected server error.

**Examples**  

*Below are short code snippets that demonstrate how to call the delete endpoint using three popular languages.*

**C# Example**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Status: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Error: {ex.Message}");
}
```

**Java Example**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Status: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Error: " + e.getMessage());
        }
    }
}
```

**Python Example**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Status: {response.status}")
except ApiException as e:
    print(f"Error: {e}")
```

**Error Handling**  

- Verify that the authentication token is valid before making the request.  
- Check the response status code; handle `400`, `401`, `404`, and `500` accordingly.  
- Use try‑catch blocks (or equivalent) to capture network or SDK exceptions.

**Related Operations**  

- [Add a worksheet](/worksheets/add/) – Create a new worksheet in an existing workbook.  
- [Copy a worksheet](/worksheets/copy/) – Duplicate an existing worksheet.  
- [Rename a worksheet](/worksheets/rename/) – Change the name of a worksheet.  
- [Move a worksheet](/worksheets/move/) – Reorder worksheets within a workbook.  