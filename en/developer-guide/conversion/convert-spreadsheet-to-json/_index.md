---
title: "Convert Spreadsheet to JSON Using Aspose.Cells Cloud API"
date: 2024-06-15
last_modified_date: 2024-06-15
linktitle: "Convert Spreadsheet to JSON"
url: "/convert-spreadsheet-to-json/"
keywords:
  [
    "Aspose.Cells Cloud",
    "convert Excel to JSON",
    "spreadsheet to JSON API",
    "REST API conversion",
    "Excel to JSON example",
    "JSON export from spreadsheet",
  ]
description: "Convert Excel, CSV, and other spreadsheet formats to JSON using Aspose.Cells Cloud API securely and server-side."
api_version: "v4.0"
weight: 100
type: docs
ArticleTitle: "Convert Excel to JSON with Aspose.Cells Cloud API - Secure, Server-Side Conversion"
---
The **ConvertSpreadsheetToJson** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json`) in Aspose.Cells Cloud converts a local spreadsheet file—such as `.xls`, `.xlsx`, or `.xlsm`—directly to JSON format without requiring prior upload to cloud storage, enabling efficient, low-latency conversion for data pipelines and web applications by processing the file entirely on the cloud server.

## The Convert Spreadsheet to JSON Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### Authentication

All requests require a valid JWT access token in the `Authorization` header:

```http
Authorization: Bearer <your_jwt_token>
```

See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Example Request (cURL — Direct Stream Response)

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
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json" \
  -H "Authorization: Bearer <your_token>" \
  -F "Spreadsheet=@MyWorkbook.xlsx" \
  --output result.json
```

### Example Request (cURL)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json&region=en-US" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -F "Spreadsheet=@MyWorkbook.xlsx"
```

### Response

The API returns the converted JSON as a file stream (or saves it to storage if `outPath` is provided).

**Success (200 OK)**

- Body: JSON content (as `application/json` stream)
- Status: `"Conversion successful; JSON returned in response stream."`

**Error Responses**

## Use Cases

- ✅ **Data Migration** – Convert legacy Excel reports to JSON for ingestion into MongoDB, DynamoDB, or data lakes.
- ✅ **Web/Mobile Apps** – Allow users to upload spreadsheets; convert to JSON client-ready format _without_ storing originals.
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
  process.env.CELLS_CLOUD_CLIENT_SECRET!,
);

const file = require("fs").createReadStream("MyWorkbook.xlsx");

try {
  const res = await cellsApi.cellsWorkbookPutConvertWorkbook(
    file,
    "json",
    undefined,
    "output/result.json",
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
