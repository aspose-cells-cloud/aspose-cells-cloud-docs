---
title: "Retrieve List Object from Worksheet"
date: 2024-03-15T00:00:00Z
lastmod: 2024-03-15T00:00:00Z
description: "Learn how to retrieve a ListObject (Excel table) from a worksheet using the Aspose.Cells Cloud REST API, including cURL examples, SDK samples (C#, Java, Python, PHP, Ruby, Go, Node.js), and comprehensive error handling."
keywords:
  - Aspose.Cells
  - Excel API
  - REST API
  - ListObject
  - Table API
  - Get Table
  - Excel Cloud
  - API Documentation
linktitle: "Get"
type: docs
weight: 9
aliases:
  - /get-a-list-object-or-table-inside-the-worksheet/
  - /tables/get/
---

## Retrieve a List Object (Table) from a Worksheet

Retrieve a **list object** (also known as a *table*) from a specific worksheet in an Excel workbook using the Aspose.Cells Cloud REST API. The endpoint supports retrieving the full ListObject metadata in JSON format or exporting the table directly to a specified format (PDF, CSV, JSON, etc.) via the optional `format` query parameter.

---

## Prerequisites

| Requirement         | Details                                                                                                                                                        |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Authentication**  | A valid **JWT** (Bearer) token is required. Obtain the token via the **OAuth2** authentication flow described in the [Authentication guide](/authentication/). |
| **Storage**         | The workbook must be stored in an Aspose Cloud storage location. For non-default storage, specify the `storageName` query parameter.                         |
| **Rate limits**     | Standard Aspose Cloud rate limit: 100 requests/minute per account.                                                                                             |
| **SDKs (optional)** | Official SDKs (C#, Java, Python, PHP, Ruby, Go, Node.js) simplify request construction and response handling. See **SDK Samples** below.                      |

---

## Request

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Parameter           | Type      | Location | Required | Description                                                                 |
| ------------------- | --------- | -------- | -------- | --------------------------------------------------------------------------- |
| **name**            | `string`  | Path     | ✔️       | Name of the Excel file (including extension, e.g., `Book1.xlsx`).         |
| **sheetName**       | `string`  | Path     | ✔️       | Worksheet name containing the target list object.                           |
| **listobjectindex** | `integer` | Path     | ✔️       | **Zero-based** index of the list object to retrieve.                        |
| **format**          | `string`  | Query    | ❌       | Export format: `pdf`, `csv`, `json`, `xlsx`, etc. Omit to return JSON.     |
| **folder**          | `string`  | Query    | ❌       | Folder path where the workbook resides (e.g., `Reports/2024`).              |
| **storageName**     | `string`  | Query    | ❌       | Name of the Aspose Cloud storage (if not using default storage).           |

#### Notes
- All requests **must** use HTTPS.
- When `format` is provided, the response is a binary file stream (e.g., `Content-Type: text/csv`).
- Without `format`, the response is a JSON object describing the ListObject.
- Parameter names in SDKs follow language-specific conventions (e.g., `listObjectIndex` in C#/Java, `listobjectindex` in Python/Ruby/Go/PHP/Node.js).

---

## cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

> **Note**: Replace `<your_jwt_token>` with a valid JWT obtained from the [Authentication endpoint](/authentication/).

---

## Successful Response

### JSON Response (when `format` is omitted)

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

### Exported File Stream (when `format` is provided)

- Example response headers:
  ```
  Content-Type: text/csv
  Content-Disposition: attachment; filename="Table3.csv"
  ```
- Response body: Raw CSV content of the table.

---

## Error Handling

| HTTP Code | Meaning                                                         | Example JSON Response                                |
| --------- | --------------------------------------------------------------- | ---------------------------------------------------- |
| **400**   | Bad request – missing/invalid parameters or unsupported format. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401**   | Unauthorized – missing, expired, or invalid JWT token.          | `{"Code":401,"Message":"Authentication failed."}`    |
| **404**   | Resource not found – file, worksheet, or list object missing.   | `{"Code":404,"Message":"ListObject not found."}`     |
| **500**   | Internal server error.                                          | `{"Code":500,"Message":"Unexpected server error."}`  |

### Common Pitfalls
- **Zero-based indexing**: `listobjectindex=1` retrieves the *second* table in the worksheet.
- **Folder path**: Include subfolder paths in the `folder` query (e.g., `?folder=Reports/2024`).
- **Supported formats**: Only formats supported by Aspose.Cells (e.g., `pdf`, `xlsx`, `csv`, `json`) are accepted. Invalid values return `400`.

---

## SDK Samples

> **Note**: SDK method parameter names follow language conventions (e.g., `listObjectIndex` in C#, `listobjectindex` in Python). See [Prerequisites](#prerequisites) for details.

<details>
<summary>💻 C# — Retrieve ListObject</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new ListObjectsApi();

var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listObjectIndex: 1,
    format: null,               // e.g., "csv" to export
    folder: null,
    storageName: null
);

var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```

</details>

<details>
<summary>☕ Java — Retrieve ListObject</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listObjectIndex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```

</details>

<details>
<summary>🐍 Python — Retrieve ListObject</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```

</details>

<details>
<summary>🟢 Node.js (TypeScript) — Retrieve ListObject</summary>

```typescript
import {
  ListObjectsApi,
  GetWorksheetListObjectRequest,
} from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
  name: "Book1.xlsx",
  sheetName: "Sheet1",
  listobjectindex: 1,
  format: undefined,
  folder: undefined,
  storageName: undefined,
});

api
  .getWorksheetListObject(request)
  .then((response) => console.log(response))
  .catch((err) => console.error(err));
```

</details>

<details>
<summary>🐘 PHP — Retrieve ListObject</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```

</details>

<details>
<summary>💎 Ruby — Retrieve ListObject</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```

</details>

<details>
<summary>🦪 Go — Retrieve ListObject</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```

</details>

---

## See Also

| Related Endpoint                     | Description                                     |
| ------------------------------------ | ----------------------------------------------- |
| [Add ListObject](/list-objects/add/) | Create a new table in a worksheet.              |
| [Update ListObject](/list-objects/update/) | Modify table properties (style, columns, etc.). |
| [Delete ListObject](/list-objects/delete/) | Remove a table from a worksheet.                |
| [List All ListObjects](/list-objects/list/) | Enumerate all tables in a worksheet.            |

---

## References

- **OpenAPI Specification** – [https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject)
- **Authentication Guide** – [https://docs.aspose.cloud/cells/authentication/](https://docs.aspose.cloud/cells/authentication/)
- **GitHub SDK Repositories** – [https://github.com/aspose-cells-cloud](https://github.com/aspose-cells-cloud)