---
title: "Delete All Worksheet Comments"
description: "Delete all comments from a worksheet in an Excel file using Aspose.Cells Cloud API. Learn the DELETE endpoint, required parameters, authentication, sample cURL request, response format, error codes, and SDK examples."
keywords: "Aspose, Cells, delete comments, worksheet, API, REST, Excel, cloud"
url: /comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Delete All Worksheet Comments

**API version:** `v3.0`  
**Resource:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud provides a robust REST endpoint that removes **all** comments from a specified worksheet. This operation is irreversible; once executed, the comments cannot be recovered.

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Authentication** | A valid JWT access token is required in the `Authorization` header (`Bearer <jwt token>`). Obtain the token via the [OAuth2 authentication flow](https://docs.aspose.cloud/cells/authentication/). |
| **Storage** | The file must reside in a storage that is accessible to Aspose.Cells Cloud (default storage is used if `storageName` is omitted). |
| **Permissions** | The token must have permission to read and write the target file. |
| **SDKs (optional)** | SDKs are available for .NET, Java, PHP, Ruby, Node.js, Python, Perl, and Go (see **SDK Examples** section). |

---

## HTTP Request

### Endpoint

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Path Parameters

| Name      | Type   | Description |
|-----------|--------|-------------|
| `name`    | string | Name of the Excel file (e.g., `test.xlsx`). |
| `sheetName` | string | Name of the worksheet (e.g., `Sheet1`). |

### Query Parameters

| Name        | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `folder`    | string | optional | Path to the folder that contains the file. |
| `storageName` | string | optional | Name of the storage where the file is located. |

### Request Headers

| Header                | Value                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer <jwt token>`               |
| `Accept`              | `application/json`                |
| `Content-Type`        | `application/json`                |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Replace `test.xlsx`, `Sheet1`, `Documents`, `MyStorage`, and `<jwt token>` with your actual values.*

---

## Response

### Success (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

The response body conforms to the `CellsCloudResponse` model.

### Error Responses

| HTTP Code | Meaning                     | Example Body |
|-----------|----------------------------|--------------|
| **400**   | Bad request – invalid parameters. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**   | Unauthorized – missing/invalid JWT token. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | Not found – file or worksheet does not exist. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**   | Internal server error. | `{ "Code": 500, "Message": "Server error." }` |

---

## SDK Examples

The following snippets demonstrate how to call the endpoint with the official Aspose.Cells Cloud SDKs (version 3.13.0). Replace placeholder values (`<fileName>`, `<sheet>`, `<jwt token>`, etc.) with your own data.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | The file name.
var sheetName = "Sheet1"; // string | The worksheet name.
var folder = "Documents"; // string | Folder path (optional)
var storageName = "MyStorage"; // string | Storage name (optional)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComments: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # optional
storage_name = 'MyStorage'    # optional

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comments: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Error:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # optional
storage_name = "MyStorage"    # optional

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comments:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Exception when calling WorksheetsApi->delete_worksheet_comments: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Notes & Limitations

* This operation **deletes every comment** in the specified worksheet. Use it with caution—there is no undo.
* The request does **not** accept a request body; all required information is conveyed via the URL and headers.
* If the target file is **protected** or the worksheet is **read‑only**, the API will return a `400` or `401` error depending on the underlying cause.
* The endpoint works with files stored in **Aspose Cloud Storage** as well as with **Amazon S3**, **Azure Blob**, or **Google Cloud Storage** when correctly referenced via `storageName`.

---

## Related Resources

* **OpenAPI Specification** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **Authentication Guide** – [OAuth2 for Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **SDK Repository** – <https://github.com/aspose-cells-cloud>
* **General Worksheets API** – <https://docs.aspose.cloud/cells/worksheets/>

---

*Last updated: 2026‑07‑30*