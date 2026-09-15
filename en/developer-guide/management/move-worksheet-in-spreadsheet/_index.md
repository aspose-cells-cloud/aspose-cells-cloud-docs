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
---

Rearrange Excel worksheet order programmatically using the Aspose.Cells Cloud REST API. This operation moves a specified worksheet to a new position within the workbook, enabling standardized report layouts, logical data processing structures, and user-customized workbook delivery.

## Prerequisites

Before using the Move Worksheet API, ensure you have:

- An [Aspose.Cloud account](https://dashboard.aspose.cloud/)  
- Valid `Client ID` and `Client Secret` from the [Aspose.Cloud Dashboard](https://dashboard.aspose.cloud/authorization)  
- A workbook with at least two worksheets  
- Understanding of zero-based worksheet indexing (e.g., `0` = first sheet)

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

## Request Parameters

| Parameter       | Type    | Location | Required | Description |
|-----------------|---------|----------|----------|-------------|
| `Spreadsheet`   | File    | FormData | Yes      | The source Excel workbook (`.xlsx`, `.xls`, etc.) containing the worksheet to move. |
| `worksheet`     | String  | Query    | Yes      | The exact name of the worksheet to move (e.g., `Sheet1`, `RawData_2024`). |
| `position`      | Integer | Query    | Yes      | The zero-based target index. For example, `0` moves the sheet to first position; `2` moves it to third. Must satisfy `0 ≤ position < Worksheets.Count`. |
| `outPath`       | String  | Query    | No       | Folder path in cloud storage where the modified workbook is saved. Defaults to the source file’s directory if omitted. |
| `outStorageName`| String  | Query    | No       | Name of your configured cloud storage (e.g., `TeamDrive`). Required if using custom storage. |
| `region`        | String  | Query    | No       | Locale for formatting (e.g., `en-US`, `fr-FR`). Affects number/date parsing and output formatting. |
| `password`      | String  | Query    | No       | Password for encrypted workbooks. Omit if the file is not protected. |

> ⚠️ **Important**:  
> - `position` must be within valid range: `0 ≤ position ≤ (Worksheets.Count - 1)`.  
> - File size must not exceed 2 GB.

## Authentication

All requests require a JWT access token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

```bash
-H "Authorization: Bearer {access_token}"
```

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

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Worksheet moved successfully. |
| 400  | Bad Request           | Invalid parameter (e.g., invalid `position`, missing `worksheet`, unsupported file format). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token. |
| 404  | Not Found             | Source file not found in storage. |
| 413  | Payload Too Large     | Uploaded file exceeds 2 GB limit. |
| 500  | Internal Server Error | Unexpected error during processing. |

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
  "input.xlsx", "Sheet1", 0,
  "output.xlsx", "MyStorage"
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

> ℹ️ SDKs are maintained in the [Aspose.Cells Cloud GitHub Organization](https://github.com/aspose-cells-cloud) (last updated: 2024-04-23).

## Use Cases

### Standardized Report Generation  
After generating monthly reports, move the `Executive_Summary` worksheet to the first position to ensure key insights appear on first load.

### Data Processing Pipelines  
In ETL workflows, move the `Processed_Data` worksheet into the middle of the workbook—e.g., after raw data sheets and before analysis sheets—to reflect logical data flow.

### User-Defined Layouts  
Allow users to customize workbook structure via UI (e.g., drag-and-drop sheet tabs). Rearrange programmatically on the server before delivering the file.

## Related Operations

- [Create Worksheet](/create-worksheet/)  
- [Delete Worksheet](/delete-worksheet/)  
- [List Worksheets](/list-worksheets/)

## Troubleshooting

| Issue | Resolution |
|-------|------------|
| `400 Bad Request`: `position` out of range | Ensure `0 ≤ position < Worksheets.Count` |
| `404 Not Found`: File not accessible | Verify `outPath` and `outStorageName`; confirm file exists in storage |
| `401 Unauthorized`: Invalid token | Refresh token using `grant_type=client_credentials` |
| Worksheet name mismatch | Use exact case-sensitive sheet name (check via [List Worksheets](/list-worksheets/)) |

## Version Notes

- **v4.0 (current)**: Supports all modern Excel formats (XLSX, XLS, CSV, ODS).  
- **v5.0 (preview)**: In development; introduces batch operations and schema validation. See [changelog](https://docs.aspose.cloud/total/release-notes/) for updates.