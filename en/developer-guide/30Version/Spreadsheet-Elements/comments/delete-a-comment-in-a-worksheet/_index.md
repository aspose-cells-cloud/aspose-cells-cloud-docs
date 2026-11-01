---
title: "Delete Worksheet Comment API – Aspose.Cells Cloud"
type: docs
url: /comments/delete/
description: "Delete Excel worksheet comments via Aspose.Cells Cloud REST API v3.0 with JWT auth and SDK examples."
keywords: "delete cell comment, Excel API, Aspose.Cells Cloud, REST API, worksheet comment removal"
date: "2024-05-15"
lastModified: "2024-05-15"
canonical: "https://docs.aspose.cloud/cells/comments/delete/"
draft: false
weight: 100
linktitle: "Delete Comment"
ArticleTitle: "Delete Worksheet Comment via Aspose.Cells Cloud REST API"
---
The **DeleteWorksheetComment** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}`) removes a cell comment from a specified worksheet in an Excel file stored in the cloud, preserving the cell's content. Aspose.Cells Cloud provides robust support for this operation, enabling developers to programmatically clean up annotations using its REST API or SDKs for .NET, Java, Python, Node.js, and Go.

> **Page last updated:** May 15, 2024

## Overview

A **comment** is a text note attached to a specific cell in an Excel worksheet. The **Delete Worksheet Comment** operation removes the comment from the specified cell, leaving the cell content intact.

![Diagram: Excel cell with comment bubble being deleted via API call](/cells/images/Aspose-image-for-open-graph.jpg "Delete a worksheet comment using Aspose.Cells Cloud REST API")

## Authentication

All Aspose.Cells Cloud endpoints require **JWT token–based authentication**. Include the token in the `Authorization` header:

```http
Authorization: Bearer <jwt token>
```

For step-by-step instructions on obtaining and using a JWT token, see the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Delete Worksheet Comment Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| cellName | String | Path | The cell name. |
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

### Query Parameters

| Parameter     | Type   | Required | Description                                                                               |
| ------------- | ------ | -------- | ----------------------------------------------------------------------------------------- |
| `folder`      | string | ❌       | Folder path where the workbook is stored (e.g., `Docs`). If omitted, root folder is used. |
| `storageName` | string | ❌       | Name of the storage service (e.g., `MyCloud`). If omitted, the default storage is used.   |

## Delete a Worksheet Comment via REST API

### Request Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SalesData.xlsx/worksheets/Q3_Results/comments/B5?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
```

### Response

#### Success (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

#### HTTP Status Codes

| Code | Meaning               | Description                                                  |
| ---- | --------------------- | ------------------------------------------------------------ |
| 200  | OK                    | Comment deleted successfully.                                |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                |
| 404  | Not Found             | Workbook, worksheet, or comment not found.                   |
| 429  | Too Many Requests     | Rate limit exceeded. See [Rate Limiting](#rate-limiting).    |
| 500  | Internal Server Error | Unexpected server error.                                     |

### Error Responses

| HTTP Code | Example Response                                         | Description                                     |
| --------- | -------------------------------------------------------- | ----------------------------------------------- |
| 400       | `{ "Code": 400, "Message": "Invalid parameters." }`      | Malformed request (e.g., invalid `cellName`).   |
| 401       | `{ "Code": 401, "Message": "Authentication required." }` | Missing or expired token.                       |
| 404       | `{ "Code": 404, "Message": "Resource not found." }`      | Workbook, worksheet, or comment does not exist. |

## SDK Examples

All examples below use **Aspose.Cells Cloud SDK v21.0.0** (current as of May 2024). Replace placeholder values with your own.

> 💡 **Tip**: Install SDKs via:
>
> - **C#**: `dotnet add package Aspose.Cells.Cloud --version 24.5.0`
> - **Java**: Maven artifact `com.aspose:aspose-cells-cloud:24.5.0`
> - **Python**: `pip install asposecellscloud==21.0.0`
> - **Node.js**: `npm install @asposecloud/cells-cloud@21.0.0`
> - **PHP**: `composer require aspose/cells-cloud-php`
> - **Ruby**: `gem install aspose_cells_cloud`
> - **Perl**: `cpan install AsposeCellsCloud`
> - **Go**: `go get github.com/aspose-cells-cloud/aspose-cells-cloud-go/v21`

### C#

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var apiInstance = new WorksheetsApi(config);

try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "SalesData.xlsx",
        sheetName: "Q3_Results",
        cellName: "B5",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine($"Comment deleted. Status: {result.Status}");
}
catch (Exception e)
{
    Console.WriteLine($"Error: {e.Message}");
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
                "SalesData.xlsx", "Q3_Results", "B5", "Docs", "MyStorage"
            );
            System.out.println("Deleted comment, status: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Error: " + e.getMessage());
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
        'SalesData.xlsx', 'Q3_Results', 'B5', 'Docs', 'MyStorage'
    );
    echo "Comment deleted. Status: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage(), PHP_EOL;
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
  result = api_instance.delete_worksheet_comment(
    'SalesData.xlsx', 'Q3_Results', 'B5', 'Docs', 'MyStorage'
  )
  puts "Comment deleted – status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```

### Node.js (TypeScript)

```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
  accessToken: "<jwt token>",
  basePath: "https://api.aspose.cloud",
});

const api = new WorksheetsApi(config);

api
  .deleteWorksheetComment(
    "SalesData.xlsx",
    "Q3_Results",
    "B5",
    "Docs",
    "MyStorage",
  )
  .then((response) => {
    console.log("Comment deleted. Status:", response.status);
  })
  .catch((error) => {
    console.error("Error:", error);
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
        name="SalesData.xlsx",
        sheet_name="Q3_Results",
        cell_name="B5",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Comment deleted. Status:", response.status)
except Exception as e:
    print("Error:", e)
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
        name        => 'SalesData.xlsx',
        sheet_name  => 'Q3_Results',
        cell_name   => 'B5',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Comment deleted. Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Error: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v21/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v21/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "SalesData.xlsx", "Q3_Results", "B5", "Docs", "MyStorage",
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Comment deleted. Status: %s\n", result.Status)
}
```

## Rate Limiting

Rate limits apply **per application ID** (not per user). The default limit is **100 requests per minute**. Exceeding this returns HTTP 429 (`Too Many Requests`). Respect the `Retry-After` header or implement exponential backoff.

For details, see the [Rate Limiting Policy](https://docs.aspose.cloud/total/working-with-aspose-cloud-service/rate-limiting/).

## Related Operations

- [Add Worksheet Comment](/total/comments/add/)
- [Update Worksheet Comment](/total/comments/update/)
- [Get Worksheet Comments](/total/comments/get/)

## Try It

Test this API interactively using the [Swagger Console](https://apiconsole.aspose.cloud/).

## See Also

- **OpenAPI Specification**: [DeleteWorksheetComment](https://docs.aspose.cloud/cells/apireference/#/Worksheets/DeleteWorksheetComment)
- **Authentication Guide**: [Authenticating API Requests](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- **SDK Repository**: [GitHub – aspose-cells-cloud](https://github.com/aspose-cells-cloud)
- **API Reference**: [Aspose.Cells Cloud API](https://docs.aspose.cloud/cells/)

## Changelog

- **2024-05-15** (v21.0.0): Updated SDK examples, clarified rate limits, fixed broken links, improved accessibility (added alt text), and standardized metadata.
- **2026-07-30**: _Note: Original future-dated content corrected to reflect current release._
