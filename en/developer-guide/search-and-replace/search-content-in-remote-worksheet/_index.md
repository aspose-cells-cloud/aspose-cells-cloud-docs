---
title: "Search Text in Remote Excel Worksheet – Aspose.Cells Cloud API"
linktitle: "Search Text in Remote Spreadsheet"
type: docs
description: "Find text, numbers, or formulas in a remote Excel worksheet using Aspose.Cells Cloud API. Supports case-insensitive search, password-protected files, and cloud storage integration."
keywords: "aspose.cells, excel api, text search, remote worksheet, cloud api"
---
The **SearchContentInRemoteWorksheet** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content`) enables developers to programmatically search for specified text, numbers, or formulas within a worksheet of an Excel workbook stored in cloud storage using Aspose.Cells Cloud, supporting case-insensitive and whole-word matching options while returning match locations directly in the cloud without requiring local file downloads.

## The Search Content in Remote Worksheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### Authentication

All requests require a valid OAuth 2.0 JWT token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for implementation details.

```http
Authorization: Bearer {access_token}
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | Specify the search workbook file name. |
| worksheet | String | Path | Specify the search worksheet name. |
| searchText | String | Query | Specify the search content. |
| ignoringCase | Boolean | Query | Ignore the text of the search. |
| folder | String | Query | The folder path where the workbook is stored. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response

```json
[
  {
    "Name": "SearchResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "SearchResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Responses

| Status Code | Description                                                      |
| ----------- | ---------------------------------------------------------------- |
| `400`       | Invalid URL or malformed request parameters                      |
| `401`       | Missing or invalid OAuth 2.0 credentials                         |
| `404`       | Workbook, worksheet, or storage path not found                   |
| `500`       | Server-side error (e.g., unsupported file format, access denied) |

### Success Response (200 OK)

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **`textItems`**: Array of match objects, each containing:
  - `cellName`: Cell address (e.g., `"C7"`)
  - `text`: The matched string
  - `occurrences`: Number of matches in that cell
- **`code`**: HTTP status code
- **`status`**: Human-readable status message

## Use Cases

- **Compliance Auditing**: Locate sensitive terms (e.g., “Confidential”, “PII”) across large spreadsheets.
- **Cross-Sheet Validation**: Identify recurring identifiers (e.g., project IDs, customer codes) in multiple worksheets.
- **Template Verification**: Confirm placeholders (e.g., `{{Date}}`) are replaced after report generation.
- **Historical Data Mining**: Extract business event codes or status markers from legacy files.

## Implementation Examples

### cURL Request

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/annual_report.xlsx/worksheets/Sheet1/search/content?searchText=Total&ignoringCase=true&folder=Reports" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json"
```

### Using Aspose.Cells Cloud SDKs

SDKs for .NET, Java, Python, PHP, Node.js, and Ruby streamline integration and reduce boilerplate code. See the [GitHub Repository](https://github.com/aspose-cells-cloud) for source code and examples.

#### Python Example (Aspose.Cells Cloud SDK for Python)

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models.search_response import SearchResponse

api = CellsApi(client_id, client_secret, base_url)
response = api.search_content_in_remote_worksheet(
    name="annual_report.xlsx",
    worksheet="Sheet1",
    search_text="Total",
    ignoring_case=True,
    folder="Reports"
)
print(f"Found {len(response.text_items)} cells with matches")
```
