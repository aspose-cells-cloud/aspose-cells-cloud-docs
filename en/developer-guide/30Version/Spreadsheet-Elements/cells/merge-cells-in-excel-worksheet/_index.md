---
title: "How to Merge Cells in an Excel Worksheet – Aspose.Cells Cloud API (v3.0)"
date: 2024-03-15T10:00:00Z
lastmod: 2024-05-20T14:30:00Z
draft: false
tags: ["excel", "cells-merge", "rest-api", "cloud", "aspose.cells", "worksheet"]
categories: ["aspose.cells-cloud", "tutorials"]
description: "Step-by-step guide to merge cells in Excel worksheets using Aspose.Cells Cloud REST API, with cURL and SDK examples (C#, Java, Python, Node.js, PHP, Ruby, Perl, Go)."
keywords: "merge cells, Excel, Aspose.Cells Cloud, REST API, v3.0, worksheet merge, cURL, SDK"
canonical: "https://docs.aspose.cloud/cells/merge-cells-in-excel-worksheet/"
weight: 110
---

# Merge Cells in Excel with Aspose.Cells Cloud API

Aspose.Cells Cloud REST API enables you to merge a rectangular block of cells into a single cell that spans the specified rows and columns. This operation is useful for creating formatted reports, dashboards, and templates in Excel files stored in the cloud.

> **Note**: This guide applies to Aspose.Cells Cloud API v3.0 (released March 2024). For v2.0, see [Legacy Merge Documentation](/docs/cells/merge-cells-v2/).

## Prerequisites

- A valid JWT token for authentication. See [Authentication Overview](/docs/total/getting-started/authentication/) for details.
- The workbook must already exist in the specified storage folder.
- Storage configuration (folder and storage name) must be set up in your Aspose.Cloud account.

## API Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### Request Parameters

| Name          | Type    | Location | Required | Description                                      |
|---------------|---------|----------|----------|--------------------------------------------------|
| `name`        | string  | path     | Yes      | The workbook name.                               |
| `sheetName`   | string  | path     | Yes      | The worksheet name.                              |
| `startRow`    | integer | query    | Yes      | Zero-based index of the first row (0 = first row). |
| `startColumn` | integer | query    | Yes      | Zero-based index of the first column (0 = first column). |
| `totalRows`   | integer | query    | Yes      | Number of rows to merge.                         |
| `totalColumns`| integer | query    | Yes      | Number of columns to merge.                      |
| `folder`      | string  | query    | No       | The folder that contains the workbook.           |
| `storageName` | string  | query    | No       | The storage name.                                |

> ✅ **No request body is required** for this operation.

### Security and Authentication

The Aspose.Cells Cloud APIs use [JWT token-based authentication](/docs/total/getting-started/authentication/). Ensure your requests include a valid `Authorization: Bearer <token>` header.

## Response

Returns a `CellsCloudResponse` object.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### HTTP Status Codes

| Code | Meaning               | Description                                      |
|------|-----------------------|--------------------------------------------------|
| 200  | OK                    | Merge operation completed successfully.          |
| 400  | Bad Request           | Missing or invalid parameters (e.g., out-of-range indices). |
| 401  | Unauthorized          | Invalid or missing JWT token.                    |
| 413  | Payload Too Large     | Request exceeds size limits (not applicable here). |
| 500  | Internal Server Error | Unexpected server-side failure.                  |

## cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=2&totalColumns=3" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your JWT token>"
```

### Expected Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## SDK Examples

Using an SDK is the recommended approach for development—it handles authentication, serialization, and error handling automatically. Below are examples in major programming languages.

{{< tabs tabTotal="8" tabID="sdk-tabs" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/blob/master/Examples/Cells/PostWorksheetMerge.cs

var cellsApi = new CellsApi(clientId, clientSecret, apiVersion, basePath);
var result = await cellsApi.PostWorksheetMerge(
    name: "input.xlsx",
    sheetName: "Sheet1",
    startRow: 10,
    startColumn: 10,
    totalRows: 2,
    totalColumns: 3,
    folder: "input",
    storage: "MyStorage"
);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Examples/src/main/java/com/aspose/cells/examples/Cells/MergeCells.java

CellsApi cellsApi = new CellsApi(clientId, clientSecret);
CellsApi.PostWorksheetMergeResponse response = cellsApi.postWorksheetMerge(
    "input.xlsx",
    "Sheet1",
    10, 10, 2, 3,
    "input",
    "MyStorage",
    null
);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/Samples/Cells/MergeCells.php

$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->postWorksheetMerge(
    "input.xlsx",
    "Sheet1",
    10, 10, 2, 3,
    "input",
    "MyStorage"
);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/blob/master/samples/cells/post_worksheet_merge.rb

cells_api = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)
response = cells_api.post_worksheet_merge(
  name: 'input.xlsx',
  sheet_name: 'Sheet1',
  start_row: 10,
  start_column: 10,
  total_rows: 2,
  total_columns: 3,
  folder: 'input',
  storage: 'MyStorage'
)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/blob/master/Examples/cells/merge-cells.ts

import { CellsApi } from "asposecellscloud";

const cellsApi = new CellsApi(process.env.CLIENT_ID!, process.env.CLIENT_SECRET!);
await cellsApi.postWorksheetMerge(
  "input.xlsx",
  "Sheet1",
  10, 10, 2, 3,
  "input",
  "MyStorage"
);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/blob/master/Examples/Cells/MergeCells.py

from asposecellscloud.api import CellsApi
from asposecellscloud.models import CellsCloudResponse

cells_api = CellsApi(client_id, client_secret, base_url)
response: CellsCloudResponse = cells_api.post_worksheet_merge(
    name="input.xlsx",
    sheet_name="Sheet1",
    start_row=10,
    start_column=10,
    total_rows=2,
    total_columns=3,
    folder="input",
    storage="MyStorage"
)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/blob/master/examples/MergeCells.pl

my $cells_api = AsposeCellsCloud::API->new(
    client_id => $client_id,
    client_secret => $client_secret,
);

my $response = $cells_api->post_worksheet_merge(
    name => 'input.xlsx',
    sheet_name => 'Sheet1',
    start_row => 10,
    start_column => 10,
    total_rows => 2,
    total_columns => 3,
    folder => 'input',
    storage => 'MyStorage'
);
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/blob/master/examples/merge_cells.go

import (
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22.9/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22.9/request"
)

cellsAPI := api.NewCellsAPIWithBaseURL("https://api.aspose.cloud")
_, err := cellsAPI.PostWorksheetMerge(
    &request.PostWorksheetMergeRequest{
        Name:         "input.xlsx",
        SheetName:    "Sheet1",
        StartRow:     10,
        StartColumn:  10,
        TotalRows:    2,
        TotalColumns: 3,
        Folder:       "input",
        StorageName:  "MyStorage",
    },
)
```

{{< /tab >}}

{{< /tabs >}}

> 🔐 **Security Note**: When using GitHub links for SDK examples (e.g., [aspose-cells-cloud](https://github.com/aspose-cells-cloud){rel="noopener noreferrer"}), always verify repository authenticity and avoid executing unreviewed code.

## Related Operations

- [Split Cells in Excel](/docs/cells/split-cells-in-excel/)  
- [Protect Worksheet](/docs/cells/protect-worksheet/)  
- [Convert Excel to PDF](/docs/cells/convert-excel-to-pdf/)

## See Also

- [Aspose.Cells Cloud API Reference](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge)
- [Full SDK Source Code](https://github.com/aspose-cells-cloud)

---

> **Last Updated**: 2024-05-20