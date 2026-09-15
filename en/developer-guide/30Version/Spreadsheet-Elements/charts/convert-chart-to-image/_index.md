---
title: "Convert Excel Chart to Image – Aspose.Cells Cloud REST API"
type: docs
url: /charts/to-image/
aliases: [/convert-charts-to-image/]
date: 2024-03-15
lastmod: 2024-03-15
canonical_url: /charts/to-image/
description: "Convert Excel chart objects to PNG, SVG, JPEG, BMP, TIFF, or GIF using Aspose.Cells Cloud REST API. Includes JWT-authenticated endpoint, SDK examples for C#, Java, Python, Node.js, PHP, Ruby, Android, Go, and Perl, plus cURL commands."
keywords: "Aspose.Cells Cloud, Excel chart to image, convert chart to PNG, chart to JPEG, REST API, image export, EMF, SVG"
weight: 50
---

This REST API guide demonstrates how to convert an **Excel chart** to a wide range of image formats—including **PNG**, **SVG**, **JPEG**, **BMP**, **TIFF**, and **EMF**—using the **Aspose.Cells Cloud REST API**.

> **Note**: This API requires an Aspose Cloud account and a valid JWT token. A free trial with 100 monthly API calls is available at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

## API Endpoint

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

### Supported Image Formats

| Format | Extension | MIME Type         |
|--------|-----------|-------------------|
| PNG    | `.png`    | `image/png`       |
| JPEG   | `.jpg`    | `image/jpeg`      |
| BMP    | `.bmp`    | `image/bmp`       |
| TIFF   | `.tiff`   | `image/tiff`      |
| GIF    | `.gif`    | `image/gif`       |
| EMF    | `.emf`    | `image/x-emf`     |
| SVG    | `.svg`    | `image/svg+xml`   |

### Request Parameters

| Parameter Name | Type    | Location | Description                                      | Required |
|----------------|---------|----------|--------------------------------------------------|----------|
| `name`         | string  | path     | The document name (e.g., `input.xlsx`)          | Yes      |
| `sheetName`    | string  | path     | Worksheet name containing the chart              | Yes      |
| `chartNumber`  | integer | path     | Zero-based index of the chart (e.g., `0`, `1`)  | Yes      |
| `format`       | string  | query    | Target image format (case-insensitive)          | Yes      |
| `folder`       | string  | query    | Folder path where the document resides          | No       |
| `storageName`  | string  | query    | Custom storage name (if applicable)             | No       |

### Response

The endpoint returns the chart as a binary image stream. The response `Content-Type` header matches the requested format (e.g., `image/png`, `image/svg+xml`).

#### HTTP Status Codes

| Code | Meaning                | Description                                                  |
|------|------------------------|--------------------------------------------------------------|
| 200  | OK                     | Chart successfully converted and returned as image stream.  |
| 400  | Bad Request            | Invalid or missing parameters (e.g., unsupported format).   |
| 401  | Unauthorized           | Missing, expired, or invalid JWT token.                     |
| 404  | Not Found              | Document, worksheet, or chart not found.                    |
| 413  | Payload Too Large      | Document size exceeds the service limit.                    |
| 500  | Internal Server Error  | Unexpected error on the server side.                        |

## Authentication

All requests must include a valid JWT access token in the `Authorization` header:

```
Authorization: Bearer <your_jwt_token>
```

To obtain a token, follow our [JWT Authentication Guide](/total/quick-start/rest-api-overview/authenticating-api-requests/).

## cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/worksheets/Sheet5/charts/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."
```

> **Tip**: Replace `Sample_Test_Book.xlsx`, `Sheet5`, `0`, and the JWT token with your actual values.

## SDK Examples

Using an SDK is the recommended approach for production integrations. It handles authentication, serialization, and error handling automatically.

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Install Aspose.Cells Cloud SDK for .NET via NuGet
// Install-Package Aspose.Cells-Cloud -Version 22.8.0

var config = new Configuration { ClientId = "your_client_id", ClientSecret = "your_client_secret" };
var cellsApi = new CellsApi(config);

string fileName = "input.xlsx";
string sheetName = "Sheet5";
int chartIndex = 0;
string format = "png";

using var response = cellsApi.GetWorksheetChart(fileName, sheetName, chartIndex, format: format);
File.WriteAllBytes("output.png", response);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```php
// Install via Composer: composer require aspose-cells-cloud/aspose-cells-cloud-php

use Aspose\Cells\CellsApi;
use Aspose\Cells\Model\Requests\GetWorksheetChartRequest;

$clientId = "your_client_id";
$clientSecret = "your_client_secret";
$cellsApi = new CellsApi($clientId, $clientSecret);

$request = new GetWorksheetChartRequest(
    name: "input.xlsx",
    sheet_name: "Sheet5",
    chart_index: 0,
    format: "png"
);

$response = $cellsApi->getWorksheetChart($request);
file_put_contents("output.png", $response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```ruby
# gem install aspose_cells_cloud

require 'aspose_cells_cloud'

AsposeCellsCloud.configure do |config|
  config.client_id = "your_client_id"
  config.client_secret = "your_client_secret"
end

api_instance = AsposeCellsCloud::CellsApi.new
file = "input.xlsx"
sheet_name = "Sheet5"
chart_index = 0
format = "png"

begin
  result = api_instance.get_worksheet_chart(file, sheet_name, chart_index, format: format)
  File.write("output.png", result)
rescue => e
  puts "Error: #{e.message}"
end
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```javascript
// npm install @aspose-cells-cloud/aspose-cells-cloud-node

const { CellsApi } = require("@aspose-cells-cloud/aspose-cells-cloud-node");

const clientId = "your_client_id";
const clientSecret = "your_client_secret";
const cellsApi = new CellsApi(clientId, clientSecret);

const fileName = "input.xlsx";
const sheetName = "Sheet5";
const chartIndex = 0;
const format = "png";

try {
  const response = await cellsApi.getWorksheetChart(fileName, sheetName, chartIndex, format);
  require("fs").writeFileSync("output.png", response);
} catch (err) {
  console.error("Error:", err);
}
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# pip install asposecellscloud

from asposecellscloud.api import CellsApi
from asposecellscloud.models import GetWorksheetChartRequest

api = CellsApi(client_id="your_client_id", client_secret="your_client_secret")

request = GetWorksheetChartRequest(
    name="input.xlsx",
    sheet_name="Sheet5",
    chart_index=0,
    format="png"
)

response = api.get_worksheet_chart(request)
with open("output.png", "wb") as f:
    f.write(response)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```java
// Add Maven dependency: com.aspose:aspose-cells-cloud-android

import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetWorksheetChartRequest;

String clientId = "your_client_id";
String clientSecret = "your_client_secret";
CellsApi api = new CellsApi(clientId, clientSecret);

GetWorksheetChartRequest request = new GetWorksheetChartRequest(
    "input.xlsx", "Sheet5", 0, "png", null, null);

byte[] response = api.getWorksheetChart(request).getBody();
Files.write(Paths.get("output.png"), response);
```

{{< /tab >}}

{{< tab tabNum="7" >}}

Example coming soon.

{{< /tab >}}

{{< tab tabNum="8" >}}

```perl
# cpan install AsposeCellsCloud

use AsposeCellsCloud::CellsApi;
use LWP::UserAgent;

my $api = AsposeCellsCloud::CellsApi->new(
    -client_id => 'your_client_id',
    -client_secret => 'your_client_secret'
);

my $response = $api->get_worksheet_chart(
    -name => 'input.xlsx',
    -sheet_name => 'Sheet5',
    -chart_index => 0,
    -format => 'png'
);

open my $fh, '>', 'output.png';
print $fh $$response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22

import (
    "context"
    "os"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22"
)

cfg := cells.NewConfiguration()
cfg.ClientId = "your_client_id"
cfg.ClientSecret = "your_client_secret"
api := cells.NewAPIClient(cfg)

resp, r, err := api.CellsApi.GetWorksheetChart(
    context.Background(),
    "input.xlsx",
    "Sheet5",
    0,
).Format("png").Execute()

if err != nil {
    log.Fatal(err)
}
defer resp.Body.Close()

out, _ := os.Create("output.png")
io.Copy(out, resp.Body)
```

{{< /tab >}}

{{< /tabs >}}

> **Note**: All SDKs support the full list of image formats (including **SVG** and **EMF**). Check the [latest SDK releases on GitHub](https://github.com/aspose-cells-cloud).

## API Reference

- [OpenAPI Specification (v3.0)](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart)
- [Aspose.Cells Cloud API Explorer](https://apiconsole.aspose.cloud/applications)

## Frequently Asked Questions

### Q: Is there a free trial?
A: Yes — you can sign up for a free trial at [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/), which includes 100 monthly API calls.

### Q: Does the API preserve chart formatting?
A: Yes — Aspose.Cells Cloud maintains fonts, colors, axes, legends, and data series fidelity during conversion.

### Q: Can I convert multiple charts in one request?
A: No — each request converts one chart. Use a loop in your code to process multiple charts sequentially.

### Q: Is SVG output supported?
A: Yes — specify `format=svg` to export vector charts for scalable, high-resolution output.

## See Also

- [Convert Excel to PDF](/cells/net/convert-excel-to-pdf/)
- [Extract Chart Data](/cells/net/extract-chart-data/)
- [Authentication Overview](/total/quick-start/rest-api-overview/authenticating-api-requests/)
- [SDK Documentation](https://github.com/aspose-cells-cloud)

---

**Last updated**: 2024-03-15