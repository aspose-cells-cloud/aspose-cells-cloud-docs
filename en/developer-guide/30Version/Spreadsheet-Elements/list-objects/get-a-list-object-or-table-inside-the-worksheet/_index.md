---
title: "Aspose.Cells Cloud API – Get List Object (Table) from Worksheet"
description: "Retrieve a ListObject (table) from an Excel worksheet using Aspose.Cells Cloud REST API. Supports export to multiple formats (PDF, CSV, JSON, …)."
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Table
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Get List Object (Table) from Worksheet

Retrieve a **list object** (also known as a *table*) from a specific worksheet in an Excel workbook. The endpoint can also export the table directly to a chosen format by using the optional `format` query parameter.

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Authentication** | A valid **JWT** (Bearer) token is required. Obtain the token via the **OAuth2** authentication flow described in the [Authentication guide](/authentication/). |
| **Storage** | The workbook must be stored in an Aspose Cloud storage location. If the file resides in a non‑default storage, specify the `storageName` query parameter. |
| **Rate limits** | The API follows the standard Aspose Cloud rate‑limit policy (default = 100 requests/minute per account). |
| **SDKs (optional)** | Using one of the official SDKs (C#, Java, Python, …) simplifies request construction and response handling. See the **SDK Samples** section below. |

---

## Request

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Parameter | Type | Location | Required | Description |
|-----------|------|----------|----------|-------------|
| **name** | `string` | Path | ✔️ | Name of the Excel file (including extension). |
| **sheetName** | `string` | Path | ✔️ | Worksheet that contains the list object. |
| **listobjectindex** | `integer` | Path | ✔️ | Zero‑based index of the list object to retrieve. |
| **format** | `string` | Query | ❌ | Desired export format (e.g., `pdf`, `csv`, `json`). |
| **folder** | `string` | Query | ❌ | Folder path where the workbook is stored. |
| **storageName** | `string` | Query | ❌ | Name of the Aspose Cloud storage to use. |

#### Notes

* All calls **must** be made over HTTPS.  
* When the `format` parameter is supplied, the response body is the exported file stream (e.g., `application/pdf`).  
* Without `format`, the API returns a JSON description of the ListObject.

---

## cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*Replace `<your_jwt_token>` with a valid JWT obtained from the authentication endpoint.*

---

## Successful Response (JSON)

When **`format` is omitted**, the API returns a JSON payload describing the ListObject.

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

When **`format` is provided**, the response body is a binary stream of the requested file type (e.g., `Content-Type: text/csv`).

---

## Error Handling

| HTTP Code | Meaning | Example JSON |
|-----------|---------|--------------|
| **400** | Bad request – missing or invalid parameters. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | Unauthorized – missing or invalid JWT token. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | Not found – workbook, worksheet, or list object does not exist. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | Internal server error. | `{"Code":500,"Message":"Unexpected server error."}` |

### Common Pitfalls (Notes)

* **Zero‑based index** – `listobjectindex` starts at **0**. Requesting index `1` returns the second table in the sheet.  
* **Folder & storage** – If the workbook is stored in a sub‑folder, include the `folder` query parameter (e.g., `?folder=Reports/2024`).  
* **Export format** – Only formats supported by the Aspose.Cells conversion engine are allowed (`pdf`, `xlsx`, `csv`, `json`, …). Supplying an unsupported value triggers a **400** error.

---

## SDK Samples

The following snippets demonstrate how to call the endpoint using the official Aspose.Cells Cloud SDKs. Replace placeholder values (`<YOUR_CLIENT>`, `<YOUR_JWT>`, etc.) with your actual configuration.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Initialise the API client
var apiInstance = new ListObjectsApi();

// Build the request
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // e.g., "csv" to export
    folder: null,
    storageName: null
);

// Execute
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

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
                1,              // listobjectindex
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
<summary>🐍 Python</summary>

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
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

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
<summary>💎 Ruby</summary>

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
<summary>🦪 Go</summary>

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

| Related endpoint | Description |
|------------------|-------------|
| **Add ListObject** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` – create a new table. |
| **Update ListObject** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – modify table properties. |
| **Delete ListObject** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` – remove a table. |
| **List All ListObjects** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` – enumerate tables in a worksheet. |

---

## References

* **OpenAPI specification** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Authentication guide** – <https://docs.aspose.cloud/cells/authentication/>  
* **GitHub repository (SDKs)** – <https://github.com/aspose-cells-cloud>  

---