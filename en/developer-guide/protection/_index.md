---
title: "Aspose.Cells Cloud Web API – Set / Modify Open Password for Excel Files"
second_title: "Comprehensive Developer Guide"
ArticleTitle: "Spreadsheet Protection – Set Open Password and Modify Password"
linktitle: "Protection"
type: docs
url: /protection/
keywords: "Aspose.Cells, Cloud, API, Spreadsheet, Protection, Open Password, Read‑Write Password, Excel"
description: "Learn how to protect an Excel workbook with an open or read‑write password using Aspose.Cells Cloud REST API. Includes request syntax, code samples, and error handling."
weight: 60
---

In this guide you will learn how to set, modify, and remove both the **open password** and the **read‑write password** for spreadsheets using the Aspose.Cells Cloud Web API. These features help protect sensitive data in your Excel workbooks.

**Prerequisites**  
- An active Aspose.Cells Cloud account with a valid API key and SID.  
- The workbook you want to protect must be uploaded to Aspose Cloud storage or accessible via a public URL.  

**API Reference**  

| **HTTP Method** | **Endpoint** | **Query / Path Parameters** | **Description** |
|-----------------|--------------|----------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (path) – name of the workbook<br>`openPassword` (query, optional) – password required to open the file<br>`readWritePassword` (query, optional) – password required to modify the file | Sets or updates the open and/or read‑write passwords for the specified workbook. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (path) – name of the workbook | Removes any passwords protecting the workbook. |

**Request Body Example (JSON)**  

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**Response Example (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Workbook protection updated successfully."
}
```

**Status Codes**  

| Code | Meaning |
|------|---------|
| 200  | Operation completed successfully. |
| 400  | Bad request – missing required parameters or invalid JSON. |
| 401  | Unauthorized – invalid API credentials. |
| 500  | Server error – unexpected condition. |

**Code Samples**

*C# (Aspose.Cells Cloud SDK)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (Aspose.Cells Cloud SDK)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**Error Handling**  
When an error occurs, the API returns a JSON payload containing `Code`, `Message`, and optionally `Description`. Check the status code and handle it accordingly in your application logic.

**Related Topics**  

- **[How to protect a spreadsheet with a password using Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[How to unprotect a spreadsheet with a password using Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  