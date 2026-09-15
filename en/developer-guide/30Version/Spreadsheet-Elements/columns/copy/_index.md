---
title: "Copy Columns in an Excel Worksheet"
description: "Learn how to copy one or more columns (including data, formatting, and formatting rules) in an Excel worksheet using the Aspose.Cells Cloud REST API v3.0. Includes cURL, SDK examples (C#, Java, Python, Ruby, Node.js, Go, Perl), authentication guidance, and error handling."
date: 2024-06-15T10:00:00Z
lastmod: 2024-06-15T14:30:00Z
tags: ["excel", "columns", "copy", "rest-api", "cloud", "aspose.cells"]
categories: ["aspose-cells-cloud", "tutorials", "api-reference"]
weight: 30
draft: false
url: /columns/copy/
aliases:
  - /copy-columns-in-excel-worksheet/
  - /copy-columns-in-an-excel-worksheet/
linktitle: "Copy Columns"
articleTitle: "Copy Columns in an Excel Worksheet using Aspose.Cells Cloud API"
---

## Overview

The **Copy Columns** operation in Aspose.Cells Cloud REST API v3.0 enables you to duplicate a single column or a contiguous range of columns within the same Excel worksheet. The copied content—including values, cell styles, conditional formatting, and formulas—is inserted at a specified destination column index. This operation supports large-scale spreadsheet management and is ideal for tasks such as template duplication, data expansion, and structural reorganization.

> **Note**: This operation only copies within the same worksheet. To copy columns across worksheets or workbooks, use [Copy Worksheet](/worksheets/copy/) or [Paste Special](/cells/paste/) operations.

---

## Security and Authentication

All Aspose.Cells Cloud API requests require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Obtain your `clientId` and `clientSecret` from the [Aspose.Cloud Dashboard](https://dashboard.aspose.cloud/), then generate a short-lived access token using the OAuth2 client credentials flow.

Example token request (cURL):

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "Accept: application/json"
```

Include the resulting `access_token` in all API requests as:

```http
Authorization: Bearer <access_token>
```

---

## REST API Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### Path Parameters

| Parameter   | Type   | Required | Description                                       |
| ----------- | ------ | -------- | ------------------------------------------------- |
| `name`      | string | Yes      | The name of the workbook (e.g., `input.xlsx`).    |
| `sheetName` | string | Yes      | The name of the worksheet containing the columns. |

### Query Parameters

| Parameter                | Type    | Required | Description                                                                                       |
| ------------------------ | ------- | -------- | ------------------------------------------------------------------------------------------------- |
| `sourceColumnIndex`      | integer | Yes      | 0-based index of the first column to copy (e.g., `1` for column B).                               |
| `destinationColumnIndex` | integer | Yes      | 0-based index where the copied column(s) will be inserted.                                        |
| `columnNumber`           | integer | Yes      | Number of consecutive columns to copy.                                                            |
| `worksheet`              | string  | No       | **Optional**: Target worksheet name for cross-worksheet copy. Defaults to `sheetName` if omitted. |
| `folder`                 | string  | No       | Path to the folder in Aspose Cloud storage (e.g., `/docs/sheets`).                                |
| `storageName`            | string  | No       | Name of the cloud storage (e.g., `FirstStorage`). Defaults to the account’s primary storage.      |

> **Important**:
>
> - All indices are **0-based**.
> - The `destinationColumnIndex` must be ≥ 0 and ≤ total columns in the worksheet.
> - Copying columns may shift existing columns to the right.

### OpenAPI Specification

Full API contract: [PostCopyWorksheetColumns](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns)

---

## Request Example (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=3" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -H "accept: application/json"
```

### Response

On success, the API returns a `200 OK` status with a minimal JSON response:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

The workbook is updated in-place in cloud storage. To retrieve the updated file, use the [DownloadFile](/storage/download/) API.

---

## SDK Examples

Using an SDK is the recommended approach for production integrations. It handles authentication, serialization, and error handling automatically.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Models;

var configuration = new Configuration
{
    ClientId = Environment.GetEnvironmentVariable("ASPOSE_CLOUD_CLIENT_ID"),
    ClientSecret = Environment.GetEnvironmentVariable("ASPOSE_CLOUD_CLIENT_SECRET")
};
var cellsApi = new CellsApi(configuration);

var request = new PostCopyWorksheetColumnsRequest
{
    Name = "test.xlsx",
    SheetName = "Sheet1",
    SourceColumnIndex = 1,
    DestinationColumnIndex = 12,
    ColumnNumber = 3,
    Folder = "docs/sheets",
    StorageName = "FirstStorage"
};

var result = await cellsApi.PostCopyWorksheetColumns(request);
Console.WriteLine($"Success: {result.Code}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### Java

```java
import com.aspose.cells.cloud.*;
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

ApiClient apiClient = new ApiClient();
apiClient.setBasePath("https://api.aspose.cloud");
apiClient.setAccessToken("YOUR_ACCESS_TOKEN");

CellsApi cellsApi = new CellsApi(apiClient);

String name = "test.xlsx";
String sheetName = "Sheet1";
Integer sourceColumnIndex = 1;
Integer destinationColumnIndex = 12;
Integer columnNumber = 3;
String folder = "docs/sheets";
String storageName = "FirstStorage";

try {
    CellsCloudResponse response = cellsApi.postCopyWorksheetColumns(
        name, sheetName, sourceColumnIndex, destinationColumnIndex, columnNumber,
        null, folder, storageName);
    System.out.println("Success: " + response.getCode());
} catch (ApiException e) {
    System.err.println("Error: " + e.getResponseBody());
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

### PHP

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\CellsApi;
use Aspose\Cells\Configuration;

$clientId = getenv('ASPOSE_CLOUD_CLIENT_ID');
$clientSecret = getenv('ASPOSE_CLOUD_CLIENT_SECRET');

$configuration = new Configuration();
$configuration->setAppKey($clientSecret);
$configuration->setAppSid($clientId);

$cellsApi = new CellsApi($configuration);

$request = new PostCopyWorksheetColumnsRequest([
    'name' => 'test.xlsx',
    'sheetName' => 'Sheet1',
    'sourceColumnIndex' => 1,
    'destinationColumnIndex' => 12,
    'columnNumber' => 3,
    'folder' => 'docs/sheets',
    'storageName' => 'FirstStorage'
]);

try {
    $result = $cellsApi->postCopyWorksheetColumns($request);
    echo "Success: " . $result->Code;
} catch (Exception $e) {
    echo 'Error: ' . $e->getMessage();
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

### Ruby

```ruby
require 'aspose_cells_cloud'

AsposeCellsCloud.configure do |config|
  config.client_id = ENV['ASPOSE_CLOUD_CLIENT_ID']
  config.client_secret = ENV['ASPOSE_CLOUD_CLIENT_SECRET']
end

cells_api = AsposeCellsCloud::CellsApi.new

request = AsposeCellsCloud::PostCopyWorksheetColumnsRequest.new(
  name: 'test.xlsx',
  sheet_name: 'Sheet1',
  source_column_index: 1,
  destination_column_index: 12,
  column_number: 3,
  folder: 'docs/sheets',
  storage_name: 'FirstStorage'
)

response = cells_api.post_copy_worksheet_columns(request)
puts "Success: #{response.code}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

### Node.js (TypeScript/JavaScript)

```typescript
import { CellsApi, PostCopyWorksheetColumnsRequest } from "aspose-cells-cloud";

const clientId = process.env.ASPOSE_CLOUD_CLIENT_ID;
const clientSecret = process.env.ASPOSE_CLOUD_CLIENT_SECRET;

const cellsApi = new CellsApi(clientId, clientSecret);

const request = new PostCopyWorksheetColumnsRequest({
  name: "test.xlsx",
  sheetName: "Sheet1",
  sourceColumnIndex: 1,
  destinationColumnIndex: 12,
  columnNumber: 3,
  folder: "docs/sheets",
  storageName: "FirstStorage",
});

try {
  const response = await cellsApi.postCopyWorksheetColumns(request);
  console.log(`Success: ${response.code}`);
} catch (error) {
  console.error("Error:", error.response?.data || error.message);
}
```

{{< /tab >}}

{{< tab tabNum="6" >}}

### Python

```python
import os
from asposecellscloud.api.cells_api import CellsApi
from asposecellscloud.models.post_copy_worksheet_columns_request import PostCopyWorksheetColumnsRequest

client_id = os.getenv("ASPOSE_CLOUD_CLIENT_ID")
client_secret = os.getenv("ASPOSE_CLOUD_CLIENT_SECRET")

api = CellsApi(client_id, client_secret)

request = PostCopyWorksheetColumnsRequest(
    name="test.xlsx",
    sheet_name="Sheet1",
    source_column_index=1,
    destination_column_index=12,
    column_number=3,
    folder="docs/sheets",
    storage_name="FirstStorage"
)

response = api.post_copy_worksheet_columns(request)
print(f"Success: {response.code}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

### Perl

```perl
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new(
  app_sid => $ENV{'ASPOSE_CLOUD_CLIENT_ID'},
  app_key => $ENV{'ASPOSE_CLOUD_CLIENT_SECRET'}
);

my $cells_api = AsposeCellsCloud::CellsApi->new(config => $config);

my $request = {
  name => 'test.xlsx',
  sheet_name => 'Sheet1',
  source_column_index => 1,
  destination_column_index => 12,
  column_number => 3,
  folder => 'docs/sheets',
  storage_name => 'FirstStorage'
};

eval {
  my $result = $cells_api->post_copy_worksheet_columns($request);
  print "Success: " . $result->{Code} . "\n";
};
if ($@) {
  warn "Error: " . $@->message;
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

### Go

```go
package main

import (
	"context"
	"fmt"
	"os"

	"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22/api"
	"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22/request"
)

func main() {
	clientID := os.Getenv("ASPOSE_CLOUD_CLIENT_ID")
	clientSecret := os.Getenv("ASPOSE_CLOUD_CLIENT_SECRET")

	ctx := context.Background()
	api := api.NewCellsApi(clientID, clientSecret)

	req := &request.PostCopyWorksheetColumnsRequest{
		Name:                   "test.xlsx",
		SheetName:              "Sheet1",
		SourceColumnIndex:      1,
		DestinationColumnIndex: 12,
		ColumnNumber:           3,
		Folder:                 "docs/sheets",
		StorageName:            "FirstStorage",
	}

	resp, _, err := api.PostCopyWorksheetColumns(ctx, req)
	if err != nil {
		fmt.Printf("Error: %v\n", err)
		return
	}
	fmt.Printf("Success: %d\n", resp.Code)
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Error Handling

The API returns standard HTTP status codes with a JSON body containing error details.

| Status Code | Meaning                                                | Example Response Body                                             |
| ----------- | ------------------------------------------------------ | ----------------------------------------------------------------- |
| `200`       | Success                                                | `{"Code": 200, "Status": "OK"}`                                   |
| `400`       | Bad Request – invalid column indices or missing params | `{"Code": 400, "Message": "Column index is out of range."}`       |
| `401`       | Unauthorized – invalid/expired token                   | `{"Code": 401, "Message": "Access token is invalid or expired."}` |
| `404`       | Not Found – workbook/worksheet does not exist          | `{"Code": 404, "Message": "Workbook 'test.xlsx' not found."}`     |
| `500`       | Internal Server Error                                  | `{"Code": 500, "Message": "An internal server error occurred."}`  |
