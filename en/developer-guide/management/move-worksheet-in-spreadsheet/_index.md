---
url: /move-worksheet-in-spreadsheet/
title: Move Worksheet in Spreadsheet – Aspose.Cells Cloud REST API
linktitle: Move Worksheet
type: docs
description: Rearrange Excel worksheet order programmatically using the Aspose.Cells Cloud REST API. Includes cURL and SDK examples (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl) for moving a worksheet to a specified zero-indexed position.
keywords: move worksheet API, rearrange sheets API, change sheet order API, Excel tab management API, Aspose Cells REST API, automate sheet positioning, workbook organization API, spreadsheet structure API, cloud Excel automation, batch sheet rearrangement
weight: 100
date: 2024-04-23
lastmod: 2024-04-23
api_version: v4.0
ArticleTitle: "Move Worksheet in Excel via Aspose.Cells Cloud REST API"
---
The **MoveWorksheetInSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet`) in Aspose.Cells Cloud enables developers to programmatically reposition a specified worksheet within an Excel workbook by name and target index, supporting dynamic report structuring and logical data flow without manual intervention.

## The Move Worksheet in Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### Authentication

All requests require a JWT access token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | The current name of the worksheet to be moved. |
| position | Integer | Query | Move the worksheet to the position |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

> ⚠️ **Important**:
>
> - `position` must be within valid range: `0 ≤ position ≤ (Worksheets.Count - 1)`.
> - File size must not exceed 2 GB.

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?worksheet=Sheet1&position=0&outPath=output.xlsx&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: multipart/form-data" \
  -F "Spreadsheet=@/path/to/input.xlsx"
```

✅ **Response (200 OK)**  
Returns the modified workbook as a binary stream (file download).

## Response Schema

```json
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
  "fileDownloadName": "output.xlsx"
}
```

### HTTP Status Codes

| Code | Meaning               | Description                                                                                 |
| ---- | --------------------- | ------------------------------------------------------------------------------------------- |
| 200  | OK                    | Worksheet moved successfully.                                                               |
| 400  | Bad Request           | Invalid parameter (e.g., invalid `position`, missing `worksheet`, unsupported file format). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token.                                                     |
| 404  | Not Found             | Source file not found in storage.                                                           |
| 413  | Payload Too Large     | Uploaded file exceeds 2 GB limit.                                                           |
| 500  | Internal Server Error | Unexpected error during processing.                                                         |

## SDK Examples

Using an SDK is recommended for production use—it handles authentication, request formatting, and error parsing.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}

```csharp
// Install-Package Aspose.Cells.Cloud.Sdk -Version 23.3.0
var cellsApi = new CellsApi("client_id", "client_secret");
var result = cellsApi.CellsWorksheetMoveToPosition(
    "input.xlsx",
    worksheetName: "Sheet1",
    position: 0,
    outPath: "output.xlsx",
    storage: "MyStorage"
);
Console.WriteLine($"Moved Sheet1 to position 0 → saved to {result.Path}");
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```java
// Install: com.aspose:aspose-cells-cloud:23.3
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File result = cellsApi.cellsWorksheetMoveToPosition(
    "input.xlsx",
    "Sheet1",
    0,
    "output.xlsx",
    "MyStorage",
    null,  // folder
    null,  // region
    null   // password
);
System.out.println("Worksheet moved: " + result.getName());
```

{{< /tab >}}
{{< tab tabNum="3" >}}

```php
// composer require aspose-cells-cloud/aspose-cells-cloud-php
$cellsApi = new CellsApi("client_id", "client_secret");
$response = $cellsApi->CellsWorksheetMoveToPosition(
    "input.xlsx",
    "Sheet1",
    0,
    "output.xlsx",
    "MyStorage"
);
echo "Moved Sheet1 → position 0\n";
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```ruby
# gem install aspose_cells_cloud
require 'aspose_cells_cloud'
api = AsposeCellsCloud::CellsApi.new("client_id", "client_secret")
result = api.cells_worksheet_move_to_position(
  "input.xlsx", worksheet_name: "Sheet1", position: 0,
  out_path: "output.xlsx", storage: "MyStorage"
)
puts "Moved Sheet1 to position 0"
```

{{< /tab >}}
{{< tab tabNum="5" >}}

```typescript
// npm install @aspose-cells-cloud/aspose-cells-cloud-node
import { CellsApi } from "@aspose-cells-cloud/aspose-cells-cloud-node";
const cellsApi = new CellsApi("client_id", "client_secret");
const res = await cellsApi.cellsWorksheetMoveToPosition(
  "input.xlsx",
  "Sheet1",
  0,
  "output.xlsx",
  "MyStorage",
);
console.log("Moved Sheet1 to position 0");
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```python
# pip install aspose-cells-cloud
from asposecellscloud.api import CellsApi
api = CellsApi(client_id="client_id", client_secret="client_secret")
response = api.cells_worksheet_move_to_position(
    name="input.xlsx",
    worksheet_name="Sheet1",
    position=0,
    out_path="output.xlsx",
    storage="MyStorage"
)
print("Moved Sheet1 to position 0")
```

{{< /tab >}}
{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
my $api = AsposeCellsCloud::CellsApi->new(
    -client_id => "client_id",
    -client_secret => "client_secret"
);
my $result = $api->cells_worksheet_move_to_position(
    "input.xlsx", "Sheet1", 0,
    "output.xlsx", "MyStorage"
);
print "Moved Sheet1 to position 0\n";
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go
import (
    "context"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
conf := cells.NewConfiguration()
conf.SetClientID("client_id")
conf.SetClientSecret("client_secret")
api := cells.NewAPIClient(conf)
resp, _, err := api.CellsAPI.CellsWorksheetMoveToPosition(
    context.Background(),
    "input.xlsx", "Sheet1", 0,
    "output.xlsx", "MyStorage",
)
if err != nil { log.Fatal(err) }
fmt.Println("Moved Sheet1 to position 0")
```

{{< /tab >}}
{{< /tabs >}}
