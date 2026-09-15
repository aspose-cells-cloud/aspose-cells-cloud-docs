---
title: "Convert Worksheet to PDF, PNG, JPEG, SVG, TIFF & More – Aspose.Cells Cloud API"
description: "Convert Excel worksheets to PDF, PNG, JPEG, SVG, TIFF, BMP, EMF, or other formats using the Aspose.Cells Cloud REST API. Includes cURL, SDK examples (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl), parameter reference, and best practices."
keywords: "worksheet conversion, Excel to image, Aspose.Cells Cloud API, convert worksheet to PNG, Excel to PDF, REST API export, SDK examples"
date: 2024-06-15
type: docs
url: /cells/convert-worksheet/
aliases:
  - /cells/convert-worksheet-to-image/
  - /worksheets/conversion/
weight: 130
---

## Overview

Aspose.Cells Cloud’s `GetWorksheetWithFormat` API enables you to convert a single worksheet from an Excel workbook (XLS, XLSX, XLSB, CSV, etc.) into over 15 output formats — including high-fidelity images (PNG, JPEG, SVG, TIFF, BMP, EMF), PDF, and document formats (CSV, TXT, XPS, OTS, NUMBERS, FODS).

This API is ideal for:
- Generating report snapshots (e.g., dashboards → PNG for web embedding)
- Archiving specific sheets as PDF for compliance
- Converting financial data to CSV for downstream processing
- Exporting charts or tables as scalable vector graphics (SVG) for responsive UIs

> **Prerequisites**  
> - An active [Aspose.Cells Cloud account](https://purchase.aspose.cloud/trial)  
> - Valid `Client ID` and `Client Secret` (see [Getting Started](https://docs.aspose.cloud/total/getting-started/))  
> - Workbook uploaded to Aspose Cloud storage (e.g., `Default` storage)  
> - JWT access token for authentication (see [Authenticating Requests](https://docs.aspose.cloud/total/quick-start/authenticating-requests/))

---

## Supported Formats

| Category       | Formats                                                                 |
|----------------|-------------------------------------------------------------------------|
| **Input (Read)** | XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT                              |
| **Output (Write)** | PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS, CSV, TXT |

> 💡 **Note**:  
> - For image formats (PNG, JPEG, SVG, etc.), resolution can be controlled via `verticalResolution`/`horizontalResolution`.  
> - SVG is an *image* format (vector), **not** a page description language.

---

## REST API Endpoint

### Request

`GET /cells/{name}/worksheets/{sheetName}`

#### Path Parameters

| Parameter | Type   | Required | Description               |
|-----------|--------|----------|---------------------------|
| `name`    | string | Yes      | The Excel workbook filename (e.g., `report.xlsx`). |
| `sheetName` | string | Yes    | The worksheet name (e.g., `Sheet1`). |

#### Query Parameters

| Parameter                | Type    | Required | Default | Allowed Values              | Description                                                                 |
|--------------------------|---------|----------|---------|-----------------------------|-----------------------------------------------------------------------------|
| `format`                 | string  | No       | —       | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, numbers, fods, ots, xps, dif | Target output format.                                                       |
| `verticalResolution`     | integer | No       | 0 (auto) | 72–600                      | Vertical DPI for image output. Set to `0` for default Excel rendering.     |
| `horizontalResolution`   | integer | No       | 0 (auto) | 72–600                      | Horizontal DPI for image output. Set to `0` for default Excel rendering.   |
| `area`                   | string  | No       | —       | e.g., `"A1:D10"`            | Cell range to convert (e.g., `"B2:E20"`).                                  |
| `pageIndex`              | integer | No       | 0       | ≥0                          | Page index for multi-page output (e.g., PDF).                              |
| `onePagePerSheet`        | boolean | No       | false   | `true`/`false`              | If `true`, renders each sheet on one page (PDF only).                      |
| `printHeadings`          | boolean | No       | false   | `true`/`false`              | Include row/column headings in output.                                     |
| `folder`                 | string  | No       | —       | —                           | Cloud folder containing the workbook (e.g., `/Reports/Q2`).               |
| `storageName`            | string  | No       | `"Default"` | —                         | Storage name (e.g., `"MyCloudStorage"`).                                   |

> ⚠️ **Important**:  
> - For image formats, set `verticalResolution` and `horizontalResolution` to ≥96 for high-quality output.  
> - Omitting `format` defaults to the workbook’s original format (e.g., XLSX).  
> - `pageIndex` and `onePagePerSheet` only apply to page-based formats (PDF, XPS, TIFF).

---

### Example Request (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=150&horizontalResolution=150" \
  -X GET \
  -H "Authorization: Bearer <your_jwt_token>" \
  -H "Accept: application/octet-stream" \
  -o "converted_sheet.png"
```

> ✅ **Tip**: Use `-H "Accept: application/octet-stream"` to ensure the binary image is saved directly.

---

### Response

| Status Code | Description                                      | Return Type                |
|-------------|--------------------------------------------------|----------------------------|
| **200**     | Conversion succeeded; binary output returned.    | `application/octet-stream` |
| **400**     | Invalid parameters (e.g., unsupported format).   | JSON error object          |
| **401**     | Missing/invalid JWT token.                       | JSON error object          |
| **404**     | Workbook or worksheet not found.                 | JSON error object          |
| **500**     | Server-side processing failure.                  | JSON error object          |

#### Sample Response (HTTP 200)
```
[Binary PNG stream — save to file as `converted_sheet.png`]
```

---

## SDK Examples

Aspose.Cells Cloud provides SDKs for 8+ languages. All SDKs handle authentication, serialization, and error handling automatically.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Install-Package Aspose.Cells.Cloud.Sdk -Version 23.5.0
var config = new Configuration { ClientId = "YOUR_CLIENT_ID", ClientSecret = "YOUR_CLIENT_SECRET" };
var cellsApi = new CellsApi(config);
var result = cellsApi.GetWorksheetWithFormat(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    format: "png",
    verticalResolution: 150,
    horizontalResolution: 150,
    folder: "input",
    storage: "Default"
);
File.WriteAllBytes("output.png", result);
```
{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Add dependency: com.aspose:aspose-cells-cloud:23.5.0
Configuration config = new Configuration();
config.setClientId("YOUR_CLIENT_ID");
config.setClientSecret("YOUR_CLIENT_SECRET");
CellsApi cellsApi = new CellsApi(config);

File result = cellsApi.getWorksheetWithFormat(
    "myWorkbook.xlsx", 
    "Sheet1", 
    "png", 
    150, 
    150, 
    null, 
    null, 
    null, 
    null, 
    "input", 
    "Default"
);
System.out.println("Saved to: " + result.getAbsolutePath());
```
{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// composer require aspose-cells-cloud/aspose-cells-cloud-php
$config = new Configuration();
$config->setClientId("YOUR_CLIENT_ID")->setClientSecret("YOUR_CLIENT_SECRET");
$cellsApi = new CellsApi($config);

$result = $cellsApi->getWorksheetWithFormat(
    "myWorkbook.xlsx",
    "Sheet1",
    "png",
    150,
    150,
    null,
    null,
    null,
    null,
    "input",
    "Default"
);
file_put_contents("output.png", $result);
```
{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# gem 'aspose_cells_cloud'
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api = AsposeCellsCloud::CellsApi.new(config)

result = api.get_worksheet_with_format(
  name: "myWorkbook.xlsx",
  sheet_name: "Sheet1",
  format: "png",
  vertical_resolution: 150,
  horizontal_resolution: 150,
  folder: "input",
  storage_name: "Default"
)
File.write("output.png", result)
```
{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
// npm install @aspose/cells-cloud
import { CellsApi, Configuration } from "@aspose/cells-cloud";

const config = new Configuration({
  clientId: "YOUR_CLIENT_ID",
  clientSecret: "YOUR_CLIENT_SECRET"
});
const cellsApi = new CellsApi(config);

const result = await cellsApi.getWorksheetWithFormat(
  "myWorkbook.xlsx",
  "Sheet1",
  "png",
  150,
  150,
  undefined,
  undefined,
  undefined,
  undefined,
  "input",
  "Default"
);
require('fs').writeFileSync("output.png", Buffer.from(result as Uint8Array));
```
{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# pip install asposecellscloud
from asposecellscloud.api import CellsApi
from asposecellscloud.models import *

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api = CellsApi(config)

result = api.get_worksheet_with_format(
    name="myWorkbook.xlsx",
    sheet_name="Sheet1",
    format="png",
    vertical_resolution=150,
    horizontal_resolution=150,
    folder="input",
    storage_name="Default"
)
with open("output.png", "wb") as f:
    f.write(result)
```
{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# cpan install AsposeCellsCloud
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new(
  client_id => "YOUR_CLIENT_ID",
  client_secret => "YOUR_CLIENT_SECRET"
);
my $api = AsposeCellsCloud::CellsApi->new(config => $config);

my $result = $api->get_worksheet_with_format(
  name => "myWorkbook.xlsx",
  sheet_name => "Sheet1",
  format => "png",
  vertical_resolution => 150,
  horizontal_resolution => 150,
  folder => "input",
  storage_name => "Default"
);
open my $fh, '>', 'output.png';
binmode $fh;
print $fh $result;
close $fh;
```
{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go
import (
  "context"
  "os"
  "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)

config := cells.NewConfiguration()
config.ClientId = "YOUR_CLIENT_ID"
config.ClientSecret = "YOUR_CLIENT_SECRET"
api := cells.NewCellsApiClient(config)

opt := &cells.GetWorksheetWithFormatOptions{
  Format:          cells.String("png"),
  VerticalResolution: cells.Int(150),
  HorizontalResolution: cells.Int(150),
  Folder:          cells.String("input"),
  StorageName:     cells.String("Default"),
}

result, _, err := api.GetWorksheetWithFormat(
  context.Background(),
  "myWorkbook.xlsx",
  "Sheet1",
  opt,
)
if err != nil { panic(err) }
os.WriteFile("output.png", result, 0644)
```
{{< /tab >}}

{{< /tabs >}}

---

## Best Practices & Troubleshooting

### ✅ Recommendations
- **For high-quality images**: Use `verticalResolution=300` and `horizontalResolution=300` for print-ready outputs.
- **Preserve formatting**: Set `printHeadings=true` to include row/column labels in PDF/image exports.
- **Limit output range**: Use `area="A1:D50"` to avoid converting empty columns/rows.
- **Error handling**: Always validate JWT tokens and storage paths before conversion.

### ⚠️ Common Issues
| Issue | Solution |
|-------|----------|
| **400: Invalid format** | Check `format` against [supported values](#supported-formats). |
| **404: Worksheet not found** | Verify `sheetName` matches exactly (case-sensitive). |
| **401: Unauthorized** | Regenerate JWT token; ensure scopes include `write:storage` and `read:document`. |
| **Distorted output** | Set explicit `verticalResolution`/`horizontalResolution`; avoid `0` for images. |

---

## Related Resources

- [Convert Entire Workbook to PDF](/cells/convert-workbook-to-pdf/)  
- [Export Chart to Image](/cells/export-chart/)  
- [Aspose.Cells Cloud SDK Documentation](https://github.com/aspose-cells-cloud)  
- [Free Online Worksheet Converter](https://products.aspose.cloud/cells/conversion/)  

> 💬 **Need help?**  
> Contact support at [support@aspose.cloud](mailto:support@aspose.cloud) or post in our [community forum](https://forum.aspose.cloud/).