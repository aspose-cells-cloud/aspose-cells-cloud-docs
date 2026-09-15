---
title: Delete all OLE objects in an Excel worksheet
description: Delete all OLE objects from an Excel worksheet using Aspose.Cells Cloud REST API v3.0. Includes cURL examples, SDK samples (C#, Java, Python, Node.js, Go), path/query parameters, error handling, and best practices.
linktitle: Clear
type: docs
url: /oleobjects/clear/
aliases: [/delete-all-oleobjects-from-excel-worksheet/]
keywords: Aspose.Cells Cloud, delete OLE objects, Excel API, REST API, worksheet OLE clear, cloud SDK
api_version: v3.0
last_updated: 2024-11-01
lastmod: 2024-11-01
weight: 60
---

# Delete all OLE objects in an Excel worksheet

**OleObjects – Clear** removes **all** OLE (Object Linking and Embedding) objects from a specified worksheet while leaving cell data untouched. This operation is useful for cleaning legacy spreadsheets or preparing a workbook for redistribution.

> **Note:** The operation is *idempotent* — calling it when no OLE objects exist returns a successful `200 OK`.

---

## Prerequisites

- A valid **Aspose Cloud JWT access token** (OAuth 2.0).
- The target workbook must be stored in Aspose Cloud storage (or specify the `folder`/`storageName` where it resides).
- API version **v3.0** or higher.

---

## HTTP Request

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Path parameters

| Name        | Type   | Required | Description                    |
| ----------- | ------ | -------- | ------------------------------ |
| `name`      | string | ✔️       | The name of the workbook file. |
| `sheetName` | string | ✔️       | The name of the worksheet.     |

### Query parameters

| Name          | Type   | Required | Description                                 |
| ------------- | ------ | -------- | ------------------------------------------- |
| `folder`      | string | optional | Folder containing the workbook.             |
| `storageName` | string | optional | Storage name where the workbook is located. |

**Headers**

| Header          | Value                |
| --------------- | -------------------- |
| `Authorization` | `Bearer <jwt token>` |
| `Accept`        | `application/json`   |
| `Content-Type`  | `application/json`   |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*Replace `<jwt token>` with a valid access token and adjust `folder`/`storageName` as needed.*

---

## Successful Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | All OLE objects deleted successfully.                             |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type, locked workbook). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Workbook exceeds size limit (max 2 GB per file).                  |
| 500  | Internal Server Error | Unexpected server error.                                          |

---

## SDK Samples

The following code snippets demonstrate how to invoke **DeleteWorksheetOleObjects** with the official Aspose.Cells Cloud SDKs. Replace placeholder values (`<YOUR_TOKEN>`, `<FILE_NAME>`, etc.) with your own data.

{{< sdk-collapse lang="csharp" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration { 
    AccessToken = "<YOUR_TOKEN>", 
    BasePath = "https://api.aspose.cloud" 
};
var api = new OleObjectsApi(config);
api.DeleteWorksheetOleObjects(
    name: "Sample.xlsx", 
    sheetName: "Sheet1", 
    folder: "Samples", 
    storageName: null
);
```
{{< /sdk-collapse >}}

{{< sdk-collapse lang="java" >}}
```java
import com.aspose.cells.cloud.api.OleObjectsApi;
import com.aspose.cells.cloud.client.ApiClient;
import com.aspose.cells.cloud.client.Configuration;

Configuration config = new Configuration();
config.setAccessToken("<YOUR_TOKEN>");
config.setBasePath("https://api.aspose.cloud");
OleObjectsApi api = new OleObjectsApi(new ApiClient(config));
api.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);
```
{{< /sdk-collapse >}}

{{< sdk-collapse lang="python" >}}
```python
from asposecellscloud import ApiClient, Configuration, OleObjectsApi

config = Configuration()
config.access_token = '<YOUR_TOKEN>'
config.host = 'https://api.aspose.cloud'
client = ApiClient(configuration=config)
api = OleObjectsApi(client)
api.delete_worksheet_ole_objects(
    name='Sample.xlsx', 
    sheet_name='Sheet1', 
    folder='Samples'
)
```
{{< /sdk-collapse >}}

{{< sdk-collapse lang="nodejs" >}}
```javascript
const { OleObjectsApi, Configuration } = require('asposecellscloud');

let config = new Configuration({ 
    accessToken: '<YOUR_TOKEN>', 
    basePath: 'https://api.aspose.cloud' 
});
let api = new OleObjectsApi(config);
api.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })
  .then(() => console.log('All OLE objects deleted'))
  .catch(err => console.error(err));
```
{{< /sdk-collapse >}}

{{< sdk-collapse lang="go" >}}
```go
package main

import (
    "context"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "<YOUR_TOKEN>"
    cfg.Host = "https://api.aspose.cloud"
    api := asposecellscloud.NewOleObjectsApi(cfg)
    _, err := api.DeleteWorksheetOleObjects(
        context.Background(), 
        "Sample.xlsx", 
        "Sheet1", 
        map[string]interface{}{ "folder": "Samples" }
    )
    if err != nil { panic(err) }
    println("All OLE objects deleted")
}
```
{{< /sdk-collapse >}}

*Full source files for all supported languages are available in the [Aspose.Cells Cloud SDK repository on GitHub (v3.0 branch)](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/v3.0).*

---

## Errors & Handling

- **Idempotency** – Deleting OLE objects on a worksheet that already has none still returns `200 OK`.
- **Token expiry** – If you receive `401 Unauthorized`, obtain a fresh JWT token and retry.
- **Invalid worksheet name** – Ensure the worksheet name matches the case used in the workbook; otherwise a `400 Bad Request` is returned.
- **File locked** – If the workbook is open in another application, the API returns `400 Bad Request` with a message indicating the file is locked.

Implement retry logic with exponential back‑off for transient `500` errors.

---

## FAQ

**Q1: Do I need to specify the `folder` and `storageName` parameters?**  
**A:** No. If omitted, Aspose Cloud assumes the default storage and root folder.

**Q2: Can I delete OLE objects from a specific cell only?**  
**A:** This endpoint deletes **all** OLE objects in the worksheet. To remove a single object, use the *Delete a specific OLE object* operation:  
`DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`

**Q3: What happens if the workbook is locked for editing?**  
**A:** The API will return `400 Bad Request` with a message indicating the file is locked. Ensure the file is not opened elsewhere before calling the endpoint.

**Q4: Is there a size limit for the workbook?**  
**A:** Yes — Aspose Cloud supports files up to 2 GB per request. Larger files should be split or processed in chunks.

---

## Best Practices

- **Performance** – Use `async` or `defer` attributes when loading third-party scripts on your documentation site to reduce initial page load time.
- **Security** – Add `rel="noopener noreferrer"` to any external links that open in a new tab.
- **Accessibility** – Decorative icons (e.g., caret-down arrows in sidebars) should have `alt=""` and `role="presentation"` to meet WCAG AA standards.
- **Consistency** – Keep date formats in ISO‑8601 (`YYYY-MM-DD`) to avoid encoding artifacts.
- **Typographic accuracy** – Use standard en-dash (`–`) for ranges (e.g., `2–GB`) and avoid zero-width spaces.

---

## Related Operations

- **Add OLE object** – [`POST /cells/{name}/worksheets/{sheetName}/oleobjects`](/cells/add-ole-object/)
- **Delete a specific OLE object** – [`DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`](/cells/delete-ole-object/)

Use the navigation links at the bottom of the page to move between related API actions.

---

![Flow diagram: client sends DELETE request to Aspose.Cells Cloud to remove OLE objects from a worksheet.](https://apireference.aspose.cloud/storage/api/v1.0/images/oleobjects-clear-workflow.png)  
*Client → [JWT Auth] → Cloud API → Storage → Response*