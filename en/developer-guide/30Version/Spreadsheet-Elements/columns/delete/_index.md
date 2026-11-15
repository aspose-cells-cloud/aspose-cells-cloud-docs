---
title: "Delete Columns from Excel via Aspose.Cells Cloud API"
description: "Delete Excel columns via Aspose.Cells Cloud REST API using cURL or SDKs with optional reference updates."
linktitle: "Delete Columns"
type: docs
url: /columns/delete/
aliases:
  [/delete-column-from-an-excel-worksheet/, /delete-column-from-a-worksheet/]
keywords:
  [
    "Aspose.Cells",
    "Delete Column",
    "Excel API",
    "REST",
    "Cloud",
    "Worksheet",
    "Columns",
  ]

weight: 100
ArticleTitle: "Delete Excel Columns via Aspose.Cells Cloud REST API"
---

The **DeleteWorksheetColumns** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}`) enables developers to remove one or more columns from an Excel worksheet using Aspose.Cells Cloud, with optional automatic updating of cell references—including formulas—in other worksheets via the `updateReference` query parameter.

## The Delete Worksheet Columns Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name  | Type    | Path/Query String/HTTPBody | Description                                                  |
| --------------- | ------- | -------------------------- | ------------------------------------------------------------ |
| name            | String  | Path                       | The file name.                                               |
| sheetName       | String  | Path                       | The worksheet name.                                          |
| columnIndex     | Integer | Path                       | The column index.                                            |
| columns         | Integer | Query                      | The number of columns.                                       |
| updateReference | Boolean | Query                      | Indicates if references in other worksheets will be updated. |
| folder          | String  | Query                      | The folder where the file is situated.                       |
| storageName     | String  | Query                      | The storage name where the file is situated.                 |

### Response

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

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

- **`{name}`** – workbook file name (e.g., `test.xlsx`).
- **`{sheetName}`** – worksheet name (e.g., `Sheet1`).
- **`{columnIndex}`** – zero‑based index of the first column to delete.

### Explanation

- Deletes columns **B and C** (`startColumn=1`, `totalColumns=2`) from `Sheet1` of `test.xlsx`.
- `updateReference=true` ensures formulas and other references are automatically adjusted.
- All SDK examples use `<YOUR_ACCESS_TOKEN>` as the placeholder for consistency.

---

## Responses

| HTTP Code | Description                                                             | Example                                                       |
| --------- | ----------------------------------------------------------------------- | ------------------------------------------------------------- |
| **200**   | Success – the column(s) were deleted.                                   | `{ "Code": 200, "Status": "OK" }`                             |
| **400**   | Bad request – missing or invalid parameters (e.g., `totalColumns < 1`). | `{ "Code": 400, "Message": "Invalid totalColumns value." }`   |
| **401**   | Unauthorized – missing or invalid JWT token.                            | `{ "Code": 401, "Message": "Authentication failed." }`        |
| **404**   | Not found – workbook or worksheet does not exist.                       | `{ "Code": 404, "Message": "Worksheet 'Sheet1' not found." }` |
| **500**   | Internal server error – unexpected condition on the server.             | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

The response body follows the generic **`CellsCloudResponse`** model.

---

## Common Errors

| Error Code | Cause                                   | Resolution                                                                                |
| ---------- | --------------------------------------- | ----------------------------------------------------------------------------------------- |
| **400**    | `totalColumns` ≤ 0 or negative          | Ensure `totalColumns` is ≥ 1 and `startColumn + totalColumns ≤ worksheet column count`.   |
| **400**    | Non-numeric `columnIndex`/`startColumn` | Use zero‑based integer indices only.                                                      |
| **404**    | Workbook file missing                   | Upload the file first via [`PutCreate`](/cells/upload/) or verify `folder`/`storageName`. |
| **404**    | Worksheet name misspelled               | Confirm case-sensitive worksheet name (e.g., `Sheet1`, not `sheet1`).                     |
| **413**    | Request payload too large               | Reduce batch size or split deletion into multiple requests.                               |

---

## How to Use the Delete Worksheet Columns API with SDKs?

### Delete Worksheet Columns API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/DeleteWorksheetColumns" rel="noopener noreferrer">Delete Worksheet Columns API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### cURL Example

```bash
curl -X DELETE \
  "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?startColumn=1&totalColumns=2&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <YOUR_ACCESS_TOKEN>"
```

Below are ready‑to‑run snippets for the most popular SDKs. Replace `<YOUR_ACCESS_TOKEN>` with your actual token.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
