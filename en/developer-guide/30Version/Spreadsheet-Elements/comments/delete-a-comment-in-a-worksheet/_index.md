---
title: "Delete Worksheet Comment API – Aspose.Cells Cloud"
description: "Delete a specific cell comment in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, request/response examples, SDK snippets, and error handling."
keywords: "Aspose.Cells, delete comment, Excel API, REST, worksheet comment"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# Delete Worksheet Comment API – Aspose.Cells Cloud

> **Page last updated:** July 30, 2026  

## Overview
A **comment** is a text note attached to a particular cell in an Excel worksheet.  
The **Delete Worksheet Comment** operation removes a comment from the specified cell.

![Aspose.Cells Cloud – Delete Worksheet Comment illustration](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – Delete Worksheet Comment API")

## Authentication
All Aspose.Cells Cloud endpoints require **JWT token‑based authentication**.  
Include the token in the `Authorization` header:

```
Authorization: Bearer <jwt token>
```

For details on obtaining a JWT token, see the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Prerequisites
- A valid JWT access token.  
- The target workbook (`{name}`) must exist in the specified storage location.  
- Optional: One of the Aspose.Cells Cloud SDKs installed for your preferred language.

## HTTP Request

### Endpoint
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Path Parameters
| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `name`      | string | ✅ | The name of the Excel workbook (e.g., `test.xlsx`). |
| `sheetName` | string | ✅ | The name of the worksheet that contains the comment. |
| `cellName`  | string | ✅ | The address of the cell whose comment will be deleted (e.g., `A1`). |

### Query Parameters
| Parameter   | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `folder`      | string | ❌ | Folder path where the workbook is stored. If omitted, the root folder is used. |
| `storageName` | string | ❌ | Name of the storage service (e.g., `MyCloud`). If omitted, the default storage is used. |

## Request Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Response

### Success (200)

```json
{
  "Code": 200,
  "Status": "OK"
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
### Error Responses

| HTTP Code | Description | Example |
|-----------|-------------|---------|
| 400 | Bad request – missing or malformed parameters. | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401 | Unauthorized – invalid or missing token. | `{ "Code": 401, "Message": "Authentication required." }` |
| 404 | Not found – the file, worksheet, or comment does not exist. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500 | Internal server error – unexpected condition on the server. | `{ "Code": 500, "Message": "Server error." }` |

## SDK Examples
Below are ready‑to‑run snippets for the most popular languages. Replace `<jwt token>`, `test.xlsx`, `Sheet1`, and `A1` with your own values.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Configure the API client
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Comment deleted. Status: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Deleted comment, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Exception when calling WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Comment deleted. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Comment deleted – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Comment deleted. Status:", response.status);
    })
    .catch((error) => {
        console.error("Error deleting comment:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comment deleted. Status:", response.status)
except Exception as e:
    print("Exception when calling WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comment deleted. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (optional)
        "MyStorage",   // storageName (optional)
    )
    if err != nil {
        fmt.Printf("Error when calling DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Comment deleted. Status: %s\n", result.Status)
}
```

## Related Operations
- [Add Worksheet Comment](/comments/add/)  
- [Update Worksheet Comment](/comments/update/)  

## Rate Limiting
Aspose.Cells Cloud enforces a default **rate limit of 100 requests per minute per account**. Exceeding this limit returns HTTP 429 Too Many Requests. Implement exponential back‑off or respect the `Retry-After` header to avoid throttling.

## See Also
- **OpenAPI Specification:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Authentication guide:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **SDK Repository:** <https://github.com/aspose-cells-cloud>  

---