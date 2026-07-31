---
title: Delete all OLE objects in an Excel worksheet
description: Learn how to remove every OLE object from an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, request/response examples, SDK snippets, authentication, error handling, and FAQs.
keywords: Aspose.Cells Cloud, delete OLE objects, Excel API, REST API, worksheet OLE clear, cloud SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Delete all OLE objects in an Excel worksheet

**OleObjects – Clear** removes **all** OLE (Object Linking and Embedding) objects from a specified worksheet while leaving cell data untouched. This operation is useful for cleaning legacy spreadsheets or preparing a workbook for redistribution.

---

## Prerequisites

- A valid **Aspose Cloud JWT access token** (OAuth 2.0).  
- The target workbook must be stored in Aspose Cloud storage (or you must specify the `folder`/`storageName` where it resides).  
- API version **v3.0** or higher.  

> **Note:** The operation is *idempotent* – calling it when no OLE objects exist returns a successful `200 OK`.

---

## HTTP Request

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Path parameters

| Name      | Type   | Required | Description          |
|-----------|--------|----------|----------------------|
| `name`    | string | ✔️       | The name of the workbook file. |
| `sheetName`| string | ✔️       | The name of the worksheet. |

### Query parameters

| Name        | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `folder`    | string | optional | Folder containing the workbook. |
| `storageName`| string | optional | Storage name where the workbook is located. |

**Headers**

| Header               | Value                         |
|----------------------|------------------------------|
| `Authorization`      | `Bearer <jwt token>` |
| `Accept`             | `application/json` |
| `Content-Type`       | `application/json` |

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

### Response Codes

| HTTP Status | Description | Example |
|-------------|-------------|---------|
| **200 OK** | All OLE objects were removed (or none existed). | `{ "Code": 200, "Status": "OK" }` |
| **400 Bad Request** | Missing or invalid parameters. | `{ "Code": 400, "Message": "Invalid worksheet name." }` |
| **401 Unauthorized** | Authentication failed or token missing/expired. | `{ "Code": 401, "Message": "Access token is invalid." }` |
| **404 Not Found** | Workbook or worksheet does not exist. | `{ "Code": 404, "Message": "Workbook not found." }` |
| **500 Internal Server Error** | Unexpected server error. | `{ "Code": 500, "Message": "Unexpected error." }` |

---

## SDK Samples

The following code snippets demonstrate how to invoke **DeleteWorksheetOleObjects** with the official Aspose.Cells Cloud SDKs. Replace placeholder values (`<YOUR_TOKEN>`, `<FILE_NAME>`, etc.) with your own data.

| Language | Sample |
|----------|--------|
| **C#** | <details><summary>Show C# example</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = \"<YOUR_TOKEN>\", BasePath = \"https://api.aspose.cloud\" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: \"Sample.xlsx\", sheetName: \"Sheet1\", folder: \"Samples\", storageName: null);\n```</details> |
| **Java** | <details><summary>Show Java example</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken(\"<YOUR_TOKEN>\");\nconfig.setBasePath(\"https://api.aspose.cloud\");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects(\"Sample.xlsx\", \"Sheet1\", \"Samples\", null);\n```</details> |
| **Python** | <details><summary>Show Python example</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Show Node.js example</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Show Go example</summary>```go\npackage main\nimport (\n    \"context\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_TOKEN>\"\n    cfg.Host = \"https://api.aspose.cloud\"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), \"Sample.xlsx\", \"Sheet1\", map[string]interface{}{ \"folder\": \"Samples\" })\n    if err != nil { panic(err) }\n    println(\"All OLE objects deleted\")\n}\n```</details> |

*Full source files for all supported languages are available in the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).*

---

## Errors & Handling

- **Idempotency** – Deleting OLE objects on a worksheet that already has none still returns `200 OK`.  
- **Token expiry** – If you receive `401 Unauthorized`, obtain a fresh JWT token and retry.  
- **Invalid worksheet name** – Ensure the worksheet name matches the case used in the workbook; otherwise a `400 Bad Request` is returned.  

Implement retry logic with exponential back‑off for transient `500` errors.

---

## FAQ

**Q1: Do I need to specify the `folder` and `storageName` parameters?**  
**A:** No. If omitted, Aspose Cloud assumes the default storage and root folder.

**Q2: Can I delete OLE objects from a specific cell only?**  
**A:** This endpoint deletes **all** OLE objects in the worksheet. To remove a single object, use the *Delete a specific OLE object* operation.

**Q3: What happens if the workbook is locked for editing?**  
**A:** The API will return `400 Bad Request` with a message indicating the file is locked. Ensure the file is not opened elsewhere before calling the endpoint.

**Q4: Is there a size limit for the workbook?**  
**A:** The service follows the general Aspose Cloud file size limits (currently up to 2 GB per file). Larger files may need to be split or processed in chunks.

---

## Best Practices

- **Performance** – Use the `async` or `defer` attributes when loading third‑party scripts on your documentation site to reduce initial page load time.  
- **Security** – Add `rel="noopener noreferrer"` to any external links that open in a new tab.  
- **Accessibility** – Decorative icons (e.g., caret‑down arrows in sidebars) should have `alt=""` and `role="presentation"` to meet WCAG AA standards.  
- **Consistency** – Keep date formats in ISO‑8601 (`YYYY‑MM‑DD`) to avoid encoding artifacts.  

---

## Related Operations

- **Add OLE object** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Delete a specific OLE object** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Use the navigation links at the bottom of the page to move between related API actions.

---