---
title: "Copy Rows on an Excel Worksheet"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Copy"
type: docs
url: /rows/copy/
aliases: [/copy-rows-in-excel-worksheet/]
description: "Copy Excel rows via Aspose.Cells Cloud REST API v3.0 using source/destination indices and row count."
api_version: "v3.0"
method: "POST"
weight: 30
ArticleTitle: "Copy Rows in Excel with Aspose.Cells Cloud REST API v3.0"
keywords: "Aspose.Cells Cloud, copy rows Excel, worksheet row copy, REST API copy rows, copy rows programmatically, Excel automation, copy entire rows, row copy API, Aspose.Cells Cloud SDK, copy rows between worksheets"
---
The **PostCopyWorksheetRows** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy`) enables copying data and formats from specific entire rows in a worksheet by specifying source and destination row indices along with the number of rows to copy. Aspose.Cells Cloud supports this operation to automate row duplication tasks programmatically, preserving cell values, styles, and formulas. Developers can integrate this capability using REST calls or SDKs for languages including .NET, Java, Python, and Node.js.

---

## The Post Copy Worksheet Rows Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/copy
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| sourceRowIndex | Integer | Query | Source row index |
| destinationRowIndex | Integer | Query | Destination row index |
| rowNumber | Integer | Query | The copied row number |
| worksheet | String | Query | The worksheet name. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

_All path parameters are case‑sensitive._

### Query Parameters

| Parameter             | Type    | Required | Description                                              |
| --------------------- | ------- | -------- | -------------------------------------------------------- |
| `sourceRowIndex`      | integer | ✅       | Zero‑based index of the source row.                      |
| `destinationRowIndex` | integer | ✅       | Zero‑based index where the rows will be placed.          |
| `rowNumber`           | integer | ✅       | Number of rows to copy.                                  |
| `worksheet`           | string  | ❌       | Worksheet identifier; usually the same as **sheetName**. |
| `folder`              | string  | ❌       | Path to the folder containing the workbook.              |
| `storageName`         | string  | ❌       | Name of the storage service.                             |

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

| Code    | Description               |
| ------- | ------------------------- |
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

| HTTP Code | Meaning                                              | Example Body                                                  |
| --------- | ---------------------------------------------------- | ------------------------------------------------------------- |
| **400**   | Bad Request – missing/invalid parameters.            | `{ "Code": 400, "Message": "Invalid sourceRowIndex." }`       |
| **401**   | Unauthorized – invalid or missing JWT token.         | `{ "Code": 401, "Message": "Authentication failed." }`        |
| **404**   | Not Found – workbook or worksheet does not exist.    | `{ "Code": 404, "Message": "File not found." }`               |
| **500**   | Internal Server Error – unexpected server condition. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

**Handling guidelines**

- **400** – Verify that all required query parameters are present and correctly formatted.
- **401** – Regenerate or refresh the JWT token.
- **404** – Confirm the workbook and worksheet names, and ensure the file exists in the specified folder/storage.
- **500** – Retry after a short delay; if the issue persists, contact Aspose support.

---

## SDK Examples

The following snippets demonstrate how to invoke the **Copy Rows** operation with the official Aspose.Cells Cloud SDKs.

| Language    | Example                                                                                                                                                                                                                                                                                                                                    |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **C#**      | <details><summary>Show code</summary>`csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar api = new CellsApi(\"clientId\", \"clientSecret\");\nawait api.PostCopyWorksheetRowsAsync(name: \"test.xlsx\", sheetName: \"Sheet1\", sourceRowIndex: 1, destinationRowIndex: 12, rowNumber: 10);\n`</details> |
| **Java**    | <details><summary>Show code</summary>`java\nCellsApi api = new CellsApi(\"clientId\", \"clientSecret\");\napi.postCopyWorksheetRows(\"test.xlsx\", \"Sheet1\", 1, 12, 10, null, null, null);\n`</details>                                                                                                                                  |
| **Python**  | <details><summary>Show code</summary>`python\nfrom asposecellscloud import CellsApi\napi = CellsApi(client_id='clientId', client_secret='clientSecret')\napi.post_copy_worksheet_rows(name='test.xlsx', sheet_name='Sheet1', source_row_index=1, destination_row_index=12, row_number=10)\n`</details>                                     |
| **Node.js** | <details><summary>Show code</summary>`javascript\nconst { CellsApi } = require('asposecellscloud');\nconst api = new CellsApi('clientId', 'clientSecret');\nawait api.postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n`</details>                                                                                                |
| **Go**      | <details><summary>Show code</summary>`go\nimport \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\napi := cells.NewCellsApiClient(\"clientId\", \"clientSecret\")\n_, err := api.PostCopyWorksheetRows(context.Background(), \"test.xlsx\", \"Sheet1\", 1, 12, 10, nil, nil, nil)\n`</details>                                     |
| **PHP**     | <details><summary>Show code</summary>`php\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi('clientId', 'clientSecret');\n$api->postCopyWorksheetRows('test.xlsx', 'Sheet1', 1, 12, 10);\n`</details>                                                                                                                                       |
| **Ruby**    | <details><summary>Show code</summary>`ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')\napi.post_copy_worksheet_rows('test.xlsx', 'Sheet1', 1, 12, 10)\n`</details>                                                                                                                    |
| **Perl**    | <details><summary>Show code</summary>`perl\nuse Aspose::Cells::CellsApi;\nmy $api = Aspose::Cells::CellsApi->new('clientId', 'clientSecret');\n$api->postCopyWorksheetRows(name => 'test.xlsx', sheetName => 'Sheet1', sourceRowIndex => 1, destinationRowIndex => 12, rowNumber => 10);\n`</details>                                      |

_Full source files are available in the [Aspose‑Cells‑Cloud GitHub repository](https://github.com/aspose-cells-cloud)._

---

## See Also

- [Add Row on an Excel Worksheet](/rows/add/)
- [Delete Row on an Excel Worksheet](/rows/delete/)
- [Update Row on an Excel Worksheet](/rows/update/)

---

_Page generated on **{{DATE}}**. For the latest version of this API, refer to the [OpenAPI specification](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetRows)._
