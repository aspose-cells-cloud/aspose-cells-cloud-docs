---
title: "Copy Rows on an Excel Worksheet"
description: "Copy data and formats from specific entire rows in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes authentication, request/response details, error handling, and SDK examples."
api_version: "v3.0"
endpoint: "/cells/{name}/worksheets/{sheetName}/cells/rows/copy"
method: "POST"
weight: 30
---

# Copy Rows on an Excel Worksheet <span style="float:right;">v3.0</span>

Copy data and formats from specific entire rows in a worksheet.

---

## Prerequisites

| # | Requirement |
|---|-------------|
| 1 | A valid **JWT** token. See the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| 2 | The workbook (`{name}`) must already exist in the selected **folder** / **storage**. |
| 3 | The target worksheet (`{sheetName}`) must be present in the workbook. |
| 4 | (Optional) Know the **folder** and **storageName** if the file is not in the default location. |

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

*All path parameters are case‑sensitive.*

### Path Parameters

| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `name`    | string | ✅ | The workbook file name (e.g., `test.xlsx`). |
| `sheetName` | string | ✅ | The worksheet name (e.g., `Sheet1`). |

### Query Parameters

| Parameter            | Type    | Required | Description |
|----------------------|---------|----------|-------------|
| `sourceRowIndex`     | integer | ✅ | Zero‑based index of the source row. |
| `destinationRowIndex`| integer | ✅ | Zero‑based index where the rows will be placed. |
| `rowNumber`          | integer | ✅ | Number of rows to copy. |
| `worksheet`          | string  | ❌ | Worksheet identifier; usually the same as **sheetName**. |
| `folder`             | string  | ❌ | Path to the folder containing the workbook. |
| `storageName`        | string  | ❌ | Name of the storage service. |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/copy?sourceRowIndex=1&destinationRowIndex=12&rowNumber=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Note**  
> Replace `<jwt token>` with a valid JWT token obtained from the authentication service.

---

## Successful Response

| Code | Description |
|------|-------------|
| **200** | Rows copied successfully. |

```json
{
  "Code": 200,
  "Status": "OK"
}
```

The response body is an instance of `CellsCloudResponse`.

---

## Error Handling

| HTTP Code | Meaning                              | Example Body |
|-----------|--------------------------------------|--------------|
| **400**   | Bad Request – missing/invalid parameters. | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }` |
| **401**   | Unauthorized – invalid or missing JWT token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Not Found – workbook or worksheet does not exist. | `{ "Code": 404, "Message": "File not found." }` |
| **500**   | Internal Server Error – unexpected server condition. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**Handling guidelines**

* **400** – Verify that all required query parameters are present and correctly formatted.  
* **401** – Regenerate or refresh the JWT token.  
* **404** – Confirm the workbook and worksheet names, and ensure the file exists in the specified folder/storage.  
* **500** – Retry after a short delay; if the issue persists, contact Aspose support.

---

## SDK Examples

The following snippets demonstrate how to invoke the **Copy Rows** operation with the official Aspose.Cells Cloud SDKs.

| Language | Example |
|----------|---------|
| **C#**   | <details><summary>Show code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi(\"clientId\", \"clientSecret\");\nawait api.PostCopyWorksheetRowsAsync(name: \"test.xlsx\", sheetName: \"Sheet1\", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n```</details> |
| **Java** | <details><summary>Show code</summary>```java\nCellsApi api = new CellsApi(\"clientId\", \"clientSecret\");\napi.postCopyWorksheetRows(\"test.xlsx\", \"Sheet1\", 1, 12, 10, null, null, null);\n```</details> |
| **Python** | <details><summary>Show code</summary>```python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n```</details> |
| **Node.js** | <details><summary>Show code</summary>```javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Go** | <details><summary>Show code</summary>```go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n```</details> |
| **PHP** | <details><summary>Show code</summary>```php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n```</details> |
| **Ruby** | <details><summary>Show code</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n```</details> |
| **Perl** | <details><summary>Show code</summary>```perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n```</details> |

*Full source files are available in the [Aspose‑Cells‑Cloud GitHub repository](https://github.com/aspose-cells-cloud).*

---

## See Also

- [Add Row on an Excel Worksheet](/rows/add/)  
- [Delete Row on an Excel Worksheet](/rows/delete/)  
- [Update Row on an Excel Worksheet](/rows/update/)  

--- 

*Page generated on **{{DATE}}**. For the latest version of this API, refer to the [OpenAPI specification](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows).*