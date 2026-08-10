---
title: "How to Get Range Content from an Excel Worksheet"
second_title: "Document"
linktitle: "Get"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, get, range, spreadsheet, REST"
description: "Learn how to retrieve range content from an Excel worksheet using Aspose.Cells Cloud REST API. Includes request syntax and sample code."
weight: 20
ArticleTitle: "How to Get Range Content from an Excel Worksheet – Aspose.Cells Cloud API"
---

## Working with retrieving range content in an Excel worksheet

- [How to get cell data based on a named range](/cells/ranges/get/values/)
- [How to get a named range from an Excel workbook](/cells/ranges/get/name/)

**Prerequisites**

- A valid Aspose Cloud access token (or `client_id`/`client_secret` for OAuth).
- The Excel file must be uploaded to the target storage folder.
- Aspose.Cells Cloud SDK version 3.0 or later.

The **Get Range** operation returns the content of a specified range in a worksheet.  
It is a simple `GET` request that returns the range data in JSON format (or other formats when requested).

**Request Overview**

| Element | Value |
|---------|-------|
| **HTTP Method** | `GET` |
| **Endpoint** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Path Parameters** | `fileName` – name of the Excel file (including extension) <br> `sheetName` – name of the worksheet <br> `rangeName` – name of the range (e.g., `A1:B10`) |
| **Query Parameters** (optional) | `folder` – storage folder <br> `storage` – storage name <br> `outFormat` – response format (e.g., `json`, `xml`) |
| **Headers** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Sample cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**Sample C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Sample Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Sample Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Response Schema (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

- `200 OK` – Range retrieved successfully.  
- `400 Bad Request` – Missing or invalid parameters.  
- `401 Unauthorized` – Invalid or missing access token.  
- `404 Not Found` – Specified file, worksheet, or range does not exist.  
- `500 Internal Server Error` – Unexpected server error.

**Error‑Response Examples**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "The request parameters are invalid or missing."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Invalid or missing access token."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "The specified file, worksheet, or range could not be found."
}
```

**See also**

- [How to get cell data based on a named range](/cells/ranges/get/values/)  
- [How to get a named range from an Excel workbook](/cells/ranges/get/name/)  
- [Update range content](/cells/ranges/update/)  
- [Delete a range](/cells/ranges/delete/)  