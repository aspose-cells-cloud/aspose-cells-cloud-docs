---
title: "Protect Excel Workbooks with Passwords"
second_title: "Comprehensive Developer Guide"
ArticleTitle: "Spreadsheet Protection – Set Open Password and Modify Password"
linktitle: "Protection"
date: 2024-03-15
type: docs
url: /protection/
keywords: "Aspose.Cells, Cloud, API, Spreadsheet, Protection, Open Password, Read-Write Password, Excel"
description: "Learn how to secure Excel workbooks using Aspose.Cells Cloud REST API — set open, read/write passwords, and remove protection via code samples in C#, Python, and curl."
weight: 60
---

In this guide you will learn how to set, modify, and remove both the **open password** and the **read-write password** for spreadsheets using the Aspose.Cells Cloud Web API. These features help protect sensitive data in your Excel workbooks.

**Prerequisites**

- An active Aspose.Cells Cloud account with a valid API key and SID.
- The workbook you want to protect must be uploaded to Aspose Cloud storage or accessible via a public URL.

**API Reference**

| **HTTP Method** | **Endpoint**                   | **Query / Path Parameters**                                                                                                                                                                       | **Description**                                                                  |
| --------------- | ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `PUT`           | `/cells/{fileName}/protection` | `fileName` (path) – name of the workbook<br>`openPassword` (query, optional) – password required to open the file<br>`readWritePassword` (query, optional) – password required to modify the file | Sets or updates the open and/or read-write passwords for the specified workbook. |
| `DELETE`        | `/cells/{fileName}/protection` | `fileName` (path) – name of the workbook                                                                                                                                                          | Removes any passwords protecting the workbook.                                   |

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

**HTTP Status Codes**

| Code | Meaning               | Description                                                  |
| ---- | --------------------- | ------------------------------------------------------------ |
| 200  | OK                    | Protection applied successfully; workbook now secured.       |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                            |
| 500  | Internal Server Error | Unexpected server error.                                     |

**Code Samples**

_C# (Aspose.Cells Cloud SDK)_

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

_Python (Aspose.Cells Cloud SDK)_

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

_Bash (cURL)_

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyFile.xlsx/protection?openPassword=MyOpenPwd123&readWritePassword=MyEditPwd456" \
     -H "Authorization: Bearer <access_token>"
```

**Error Handling**  
When an error occurs, the API returns a JSON payload containing `Code`, `Message`, and optionally `Description`. Check the status code and handle it accordingly in your application logic.

**Best Practices**

- Use strong, unique passwords for workbook protection.
- Store credentials securely—avoid hardcoding secrets in source code.
- Rotate passwords periodically for sensitive workbooks.
