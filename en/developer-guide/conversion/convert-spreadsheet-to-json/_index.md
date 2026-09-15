---
title: "Convert Spreadsheet to JSON Using Aspose.Cells Cloud API"
date: 2024-06-15
last_modified_date: 2024-06-15
linktitle: "Convert Spreadsheet to JSON"
url: "/convert-spreadsheet-to-json/"
keywords: ["Aspose.Cells Cloud", "convert Excel to JSON", "spreadsheet to JSON API", "REST API conversion", "Excel to JSON example", "JSON export from spreadsheet"]
description: "Securely convert local Excel/CSV files to JSON format using Aspose.Cells Cloud API. Includes cURL, SDK examples (Python, Node.js, Java, C#, PHP, Ruby, Perl, Go), query parameter options (password, region, fonts), and best practices for server-side conversion."
api_version: "v4.0"
weight: 100
---

Convert local spreadsheets (`.xls`, `.xlsx`, `.xlsm`) directly to JSON on Aspose.Cells Cloud without storing files in cloud storage first. This cloud-native conversion eliminates intermediate steps, reduces latency and storage costs, and simplifies integration for data pipelines, web/mobile apps, and serverless functions.

## Prerequisites

- Aspose Cloud account with valid **JWT access token**  
- Supported spreadsheet format (`.xls`, `.xlsx`, `.xlsm`, `.xlsb`, `.ods`)  
- For password-protected files: the correct password  
- *(Optional)* Custom fonts folder if workbook uses non-default fonts  

> 💡 **Tip**: Generate a free JWT token via the [Cloud Dashboard](https://dashboard.aspose.cloud/).

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

## Authentication

All requests require a valid JWT access token in the `Authorization` header:

```http
Authorization: Bearer <your_jwt_token>
```

See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

## Request Parameters

| Parameter        | Type     | Location | Required | Description |
|------------------|----------|----------|----------|-------------|
| `Spreadsheet`    | File     | FormData | Yes      | Local spreadsheet file to convert (e.g., `myfile.xlsx`). Use `curl -F "Spreadsheet=@file.xlsx"`. |
| `outPath`        | String   | Query    | No       | Path to save the output JSON in cloud storage (e.g., `/output/result.json`). Omit to return JSON in response stream. |
| `outStorageName` | String   | Query    | No       | Cloud storage name (e.g., `AmazonS3`, `AzureBlob`). Required only if `outPath` uses non-default storage. |
| `fontsLocation`  | String   | Query    | No       | Custom fonts folder path (e.g., `/fonts`) if workbook uses non-default fonts. |
| `region`         | String   | Query    | No       | Locale (e.g., `en-US`, `fr-FR`, `de-DE`). Affects date/number/currency formatting. |
| `password`       | String   | Query    | No       | Password for protected workbooks. Omit for unprotected files. |
| `AutoRowsFit`    | Boolean  | Query    | No       | `true` to autofit all rows in worksheets before conversion. Default: `false`. |
| `AutoColumnsFit` | Boolean  | Query    | No       | `true` to autofit all columns before conversion. Default: `false`. |

### Example Request (cURL)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json&region=en-US" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -F "Spreadsheet=@MyWorkbook.xlsx"
```

### Example Request (cURL — Direct Stream Response)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json" \
  -H "Authorization: Bearer <your_token>" \
  -F "Spreadsheet=@MyWorkbook.xlsx" \
  --output result.json
```

## Response

The API returns the converted JSON as a file stream (or saves it to storage if `outPath` is provided).

**Success (200 OK)**  
- Body: JSON content (as `application/json` stream)  
- Status: `"Conversion successful; JSON returned in response stream."`

**Error Responses**

| Code | Meaning              | Description |
|------|----------------------|-------------|
| 400  | Bad Request          | Invalid parameters (e.g., unsupported file type, missing file) |
| 401  | Unauthorized         | Invalid, expired, or missing JWT token |
| 404  | Not Found            | Source file inaccessible or path invalid |
| 413  | Payload Too Large    | File exceeds 2 GB upload limit |
| 500  | Internal Server Error| Unexpected error during conversion |

## Use Cases

- ✅ **Data Migration** – Convert legacy Excel reports to JSON for ingestion into MongoDB, DynamoDB, or data lakes.  
- ✅ **Web/Mobile Apps** – Allow users to upload spreadsheets; convert to JSON client-ready format *without* storing originals.  
- ✅ **Automated Reporting** – Feed JSON payloads to BI tools (Power BI, Tableau, Looker) or analytics pipelines.  
- ✅ **Serverless Functions** – Use in AWS Lambda/Azure Functions for on-demand conversions with zero storage overhead.

## Why Use This API?

- **Cloud-native processing** — No local resource usage; conversion happens entirely on Aspose’s servers.  
- **Single-step workflow** — Upload and receive JSON in one request (no intermediate storage).  
- **Full locale & format support** — Handle password-protected, region-specific, and complex workbooks.  
- **Scalable & reliable** — Handles large files and formula recalculation efficiently.

## SDK Examples

Use our official SDKs to simplify integration. All SDKs include type safety, automatic retries, and error handling.

{{< tabs tabTotal="8" tabID="sdk-tabs" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
```csharp
// Install-Package Aspose.Cells-Cloud -Version 22.8.0

var cellsApi = new CellsApi(clientId: "your_client_id", clientSecret: "your_client_secret");
using var file = File.OpenRead("MyWorkbook.xlsx");
var response = await cellsApi.CellsWorkbookPutConvertWorkbookAsync(
    file: file,
    format: "json",
    outPath: "output/result.json"
);
Console.WriteLine($"Conversion succeeded: {response.StatusCode}");
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```java
// compile: javac -cp "aspose-cells-cloud-22.8.0.jar" Example.java

import com.aspose.cells.cloud.*;

public class Example {
    public static void main(String[] args) {
        try {
            CellsApi api = new CellsApi(System.getenv("CELLS_CLOUD_CLIENT_ID"), 
                                        System.getenv("CELLS_CLOUD_CLIENT_SECRET"));
            File file = new File("MyWorkbook.xlsx");
            SpreadsheetDocumentResponse result = api.cellsWorkbookPutConvertWorkbook(
                file, "json", "output/result.json", null, null, null);
            System.out.println("Conversion successful: " + result.getCode());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```
{{< /tab >}}
{{< tab tabNum="3" >}}
```php
<?php
require_once("vendor/autoload.php");

use Aspose\Cells\CellsApi;
use GuzzleHttp\Client;

$client = new Client([
    'headers' => ['Content-Type' => 'multipart/form-data']
]);

$cellsApi = new CellsApi(getenv("CELLS_CLOUD_CLIENT_ID"), getenv("CELLS_CLOUD_CLIENT_SECRET"));
$file = realpath("MyWorkbook.xlsx");

try {
    $response = $cellsApi->cellsWorkbookPutConvertWorkbook(
        $file, 'json', null, 'output/result.json'
    );
    echo "Converted JSON saved to: " . $response->getHref();
} catch (Exception $e) {
    echo "Error: " . $e->getMessage();
}
```
{{< /tab >}}
{{< tab tabNum="4" >}}
```ruby
# gem install aspose_cells_cloud

require 'aspose_cells_cloud'

AsposeCellsCloud.configure do |config|
  config.client_data['ClientSecret'] = ENV['CELLS_CLOUD_CLIENT_SECRET']
  config.client_data['ClientId']     = ENV['CELLS_CLOUD_CLIENT_ID']
end

api_instance = AsposeCellsCloud::CellsApi.new
file = 'MyWorkbook.xlsx'

begin
  result = api_instance.cells_workbook_put_convert_workbook(
    file, format: 'json', out_path: 'output/result.json'
  )
  puts "Success: #{result.code}"
rescue => e
  puts "Error: #{e.message}"
end
```
{{< /tab >}}
{{< tab tabNum="5" >}}
```typescript
// npm install @aspose-cells-cloud

import { CellsApi } from "@aspose-cells-cloud";

const cellsApi = new CellsApi(
  process.env.CELLS_CLOUD_CLIENT_ID!,
  process.env.CELLS_CLOUD_CLIENT_SECRET!
);

const file = require("fs").createReadStream("MyWorkbook.xlsx");

try {
  const res = await cellsApi.cellsWorkbookPutConvertWorkbook(
    file, "json", undefined, "output/result.json"
  );
  console.log("Conversion completed:", res.status);
} catch (err) {
  console.error("Error:", err);
}
```
{{< /tab >}}
{{< tab tabNum="6" >}}
```python
# pip install asposecellscloud

from asposecellscloud.api import CellsApi
from asposecellscloud.models import ConvertDocumentRequest

api = CellsApi(
    client_id= "your_client_id",
    client_secret= "your_client_secret"
)

with open("MyWorkbook.xlsx", "rb") as f:
    response = api.cells_workbook_put_convert_workbook(
        file=f, format="json", out_path="output/result.json"
    )
    print(f"Success: {response.status_code}")
```
{{< /tab >}}
{{< tab tabNum="7" >}}
```perl
use AsposeCellsCloud::Client::CellsApi;
use File::Slurper qw(read_binary);

my $api = AsposeCellsCloud::Client::CellsApi->new(
    -client_id => $ENV{CELLS_CLOUD_CLIENT_ID},
    -client_secret => $ENV{CELLS_CLOUD_CLIENT_SECRET}
);

my $file = read_binary('MyWorkbook.xlsx');

eval {
  my $result = $api->cells_workbook_put_convert_workbook(
    { file => $file, format => 'json', out_path => 'output/result.json' }
  );
  print "Converted: " . $result->{Code};
};
die "Error: $@" if $@;
```
{{< /tab >}}
{{< tab tabNum="8" >}}
```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go

package main

import (
	"os"
	"fmt"
	"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22"
)

func main() {
	client := cells.NewCellsService(
		os.Getenv("CELLS_CLOUD_CLIENT_ID"),
		os.Getenv("CELLS_CLOUD_CLIENT_SECRET"),
	)

	file, err := os.Open("MyWorkbook.xlsx")
	if err != nil { panic(err) }
	defer file.Close()

	resp, err := client.CellsWorkbookPutConvertWorkbook(
		file, "json", nil, "output/result.json")
	if err != nil {
		fmt.Println("Error:", err)
		return
	}
	fmt.Printf("Success: %d\n", resp.StatusCode)
}
```
{{< /tab >}}
{{< /tabs >}}

> 📦 **All SDKs**: [GitHub Organization](https://github.com/aspose-cells-cloud)  
> 🔧 **Live Demo**: [API Explorer](https://products.aspose.cloud/cells/parser/) — test conversions directly in browser.

## Related Resources

- [Convert JSON to Excel](/convert-json-to-excel/)  
- [Handle Password-Protected Spreadsheets](/password-protected-files/)  
- [Supported File Formats](/supported-file-formats/)  
- [Optimize Large Workbook Conversion](/optimizing-large-file-conversions/)  

## Changelog

| Version | Date       | Notes |
|---------|------------|-------|
| v4.0    | 2024-06-15 | Added `AutoRowsFit`, `AutoColumnsFit` parameters; updated error handling; clarified `outPath` behavior. |

---

> ⚠️ **Note**: This endpoint requires the source file to be provided via `multipart/form-data`. It does *not* read files from cloud storage — use [UploadFile](/upload-file/) first if you prefer cloud-based workflows.