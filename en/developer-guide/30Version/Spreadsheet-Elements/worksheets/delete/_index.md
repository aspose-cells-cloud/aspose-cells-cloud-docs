---
title: "How to work with deleting worksheets in an Excel workbook"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /worksheets/delete/
keywords: "delete worksheet, Aspose.Cells Cloud, REST API, C#, Java, Python, Excel"
description: "Learn how to delete single or multiple worksheets from an Excel workbook using Aspose.Cells Cloud REST API. Includes C#, Java, and Python examples, prerequisites, error‑handling tips, and related operations."
weight: 20
---

## Working with Deleting Worksheets in an Excel Workbook

When an application generates or modifies Excel files dynamically, you may need to remove worksheets that are no longer required—such as temporary reports, placeholder sheets, or outdated data. The Aspose.Cells Cloud API makes it easy to delete a single worksheet or several worksheets in one request.

### Prerequisites
- An active **Aspose.Cells Cloud** account with a valid **API Key** and **Access Token**.  
- The workbook must be stored in a supported storage location (e.g., Aspose Cloud storage or a connected external storage).  
- The **file name**, **folder path**, and **storage name** (if not default) of the workbook you want to modify.  
- The appropriate SDK installed (C#, Java, Python, etc.).  

### Delete a Single Worksheet
To delete a single worksheet, send a `DELETE` request to the endpoint:

```
DELETE https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}
```

**Parameters**

| Parameter | Description |
|-----------|-------------|
| `fileName` | Name of the Excel workbook (including extension). |
| `sheetName` | Exact name of the worksheet to delete. |
| `folder` *(optional)* | Path to the folder containing the workbook. |
| `storage` *(optional)* | Name of the storage. |

#### Step‑by‑step code examples  

1. **C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var config = new Configuration
{
    AppSid = "<your_app_sid>",
    AppKey = "<your_app_key>"
};
var cellsApi = new CellsApi(config);

var response = await cellsApi.DeleteWorksheetAsync(
    name: "Report.xlsx",
    sheetName: "TempSheet",
    folder: "reports",
    storage: null);
Console.WriteLine($"Status: {response.Status}");
```

2. **Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<your_app_sid>", "<your_app_key>");

ApiResponse<Void> response = api.deleteWorksheet(
    "Report.xlsx",
    "TempSheet",
    "reports",
    null);
System.out.println("HTTP status: " + response.getStatusCode());
```

3. **Python**

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration(app_sid='<your_app_sid>', app_key='<your_app_key>')
api = CellsApi(Configuration=config)

response = api.delete_worksheet(
    name='Report.xlsx',
    sheet_name='TempSheet',
    folder='reports')
print(f'Status code: {response.status}')
```

### Delete Multiple Worksheets
Multiple worksheets can be removed in a single call by supplying a comma‑separated list of sheet names in the `sheetNames` query parameter.

```
DELETE https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets?sheetNames=Sheet1,Sheet2,Sheet3
```

#### Example (C#)

```csharp
var response = await cellsApi.DeleteWorksheetsAsync(
    name: "Report.xlsx",
    sheetNames: "Sheet1,Sheet2",
    folder: "reports",
    storage: null);
Console.WriteLine($"Deleted sheets, status: {response.Status}");
```

*Java* and *Python* snippets follow the same pattern—replace `DeleteWorksheetAsync` with `DeleteWorksheetsAsync` (C#) or the corresponding method in the language‑specific SDK.

### Response & Error Handling
| HTTP Status | Meaning | Typical Response |
|-------------|---------|------------------|
| **200 OK** | Worksheet(s) deleted successfully. | `{ "Code": "OK", "Status": "Deleted" }` |
| **401 Unauthorized** | Invalid or missing authentication credentials. | `{ "Code": "InvalidAuthentication", "Message": "Authentication failed." }` |
| **404 Not Found** | Specified workbook or worksheet does not exist. | `{ "Code": "WorksheetNotFound", "Message": "Worksheet 'SheetX' does not exist." }` |
| **400 Bad Request** | Missing required parameters or malformed request. | `{ "Code": "InvalidParameter", "Message": "Parameter 'sheetNames' is required." }` |

Always check the status code returned by the SDK method and handle non‑200 responses accordingly.

### Next Steps / Related Operations
- **Add a worksheet** – `/cells/{fileName}/worksheets` (`POST`)  
- **Rename a worksheet** – `/cells/{fileName}/worksheets/{sheetName}` (`PUT`)  
- **Move a worksheet** – `/cells/{fileName}/worksheets/{sheetName}/move` (`POST`)  

---

#### Common Questions

**Q:** *How can I delete a single worksheet without affecting other sheets?*  
**A:** Use the `DELETE /cells/{fileName}/worksheets/{sheetName}` endpoint; only the specified worksheet is removed.

**Q:** *Do I need to send a request body when deleting multiple worksheets?*  
**A:** No request body is required. Provide a comma‑separated list of worksheet names in the `sheetNames` query parameter.

**Q:** *What response do I receive if the worksheet I try to delete does not exist?*  
**A:** The API returns **404 Not Found** with JSON `{ "Code": "WorksheetNotFound", "Message": "Worksheet 'X' does not exist." }`. Handle this status in your code to avoid unexpected failures.  