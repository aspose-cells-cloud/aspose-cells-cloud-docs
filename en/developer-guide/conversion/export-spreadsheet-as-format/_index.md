---
title: "Export Remote Excel Worksheet to Other Formats"
linktitle: "Export Spreadsheet as Format"
type: docs
url: /export-spreadsheet-as-format/
description: "Convert Excel workbooks stored in Aspose Cloud to PDF, XLSX, CSV, HTML, JSON, ODS, and other formats using the ExportSpreadsheetAsFormat REST API. Includes cURL examples and SDK code for C#, Java, Python, PHP, Ruby, Node.js, Perl, and Go."
keywords: "Aspose.Cells Cloud, Excel to PDF conversion, REST API export, spreadsheet format conversion, XLSX, CSV, HTML, JSON, ODS, cloud API, SDK examples"
date: 2024-03-15
lastmod: 2024-06-20
sitemap:
  changefreq: monthly
  priority: 0.8
robots: index, follow
draft: false
---

## Overview

The **ExportSpreadsheetAsFormat** API enables you to convert Excel workbooks stored in Aspose Cloud to a wide range of formats—including PDF, XLSX, CSV, HTML, JSON, ODS, and TIFF—directly in the cloud. The operation processes the file remotely, eliminating local downloads and preserving formatting, formulas, and styling.

This document provides full API details, usage examples, best practices, and SDK integrations for rapid development.

---

## Prerequisites

- An active [Aspose Cloud account](https://dashboard.aspose.cloud/)
- App SID and App Key (available in your Aspose Cloud Dashboard)
- A workbook uploaded to your cloud storage (e.g., `MyWorkbook.xlsx`)

> 💡 **Tip**: Use the [Cloud Explorer](https://dashboard.aspose.cloud/storage) to manage files in cloud storage.

---

## API Endpoint

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}&AutoRowsFit={autoRowsFit}&AutoColumnsFit={autoColumnsFit}
```

| Parameter | Type | Location | Required | Description |
|:----------|:-----|:---------|:---------|:------------|
| `name` | string | Path | ✅ | Name of the source workbook (e.g., `MyWorkbook.xlsx`). |
| `format` | string | Query | ✅ | Target format: `PDF`, `XLSX`, `CSV`, `HTML`, `JSON`, `ODS`, `TIFF`, `TXT`, `XLS`, `MHTML`, `XLSB`, `XLTM`, `XLT`, `XLTX`, `DOTX`, `DOCX`, `EPUB`, `MD`, `PNG`, `JPEG`, `BMP`, `SVG`, `XPS`, `PS`, `EMF`. |
| `folder` | string | Query | ❌ | Folder path containing the workbook. Defaults to root. |
| `storageName` | string | Query | ❌ | Custom storage name. Uses default storage if omitted. |
| `outPath` | string | Query | ❌ | Destination folder for the output file. Defaults to same as source. |
| `outStorageName` | string | Query | ❌ | Storage name for output file. Uses `storageName` or default if omitted. |
| `fontsLocation` | string | Query | ❌ | Custom folder containing fonts required for rendering. |
| `region` | string | Query | ❌ | Locale setting (e.g., `en-US`, `fr-FR`). Affects number/date formatting. |
| `password` | string | Query | ❌ | Password for encrypted Excel files. |
| `AutoRowsFit` | boolean | Query | ❌ | Whether to autofit all rows before export. Default: `false`. |
| `AutoColumnsFit` | boolean | Query | ❌ | Whether to autofit all columns before export. Default: `false`. |

---

## Authentication

All requests require a valid JWT token. Obtain one using your App SID and App Key via OAuth 2.0:

```bash
curl -v "https://api.aspose.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=YOUR_APP_SID&client_secret=YOUR_APP_KEY" \
  -H "Content-Type: application/x-www-form-urlencoded"
```

Include the token in the `Authorization: Bearer <ACCESS_TOKEN>` header.

---

## cURL Example

Export a workbook to PDF, saving the result in the same folder:

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx?format=PDF&outPath=exported/MyWorkbook.pdf" \
  -H "Authorization: Bearer <ACCESS_TOKEN>" \
  -H "Accept: application/octet-stream" \
  -o MyWorkbook.pdf
```

> ✅ **Best Practice**: Replace `<ACCESS_TOKEN>` with your actual token. Use `-o` to save the response stream directly to a file.

---

## SDK Examples

### C#

```csharp
using Aspose.Cells.Cloud.Sdk;

var configuration = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var cellsApi = new CellsApi(configuration);

var result = cellsApi.ExportSpreadsheetAsFormat(
    "MyWorkbook.xlsx",
    "PDF",
    folder: null,
    storage: null,
    outPath: "exported/MyWorkbook.pdf"
);

Console.WriteLine($"Exported to: {result}");
```

### Java

```java
import com.aspose.cells.cloud.*;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

CellsApi cellsApi = new CellsApi(config);

String result = cellsApi.exportSpreadsheetAsFormat(
    "MyWorkbook.xlsx",
    "PDF",
    null, // folder
    null, // storage
    "exported/MyWorkbook.pdf"
);

System.out.println("Exported to: " + result);
```

### Python

```python
from asposecellscloud.api import CellsApi
from asposecellscloud.configuration import Configuration

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api = CellsApi(config)

result = api.export_spreadsheet_as_format(
    'MyWorkbook.xlsx',
    'PDF',
    out_path='exported/MyWorkbook.pdf'
)

print(f"Exported to: {result}")
```

### PHP

```php
require_once('vendor/autoload.php');

use Aspose\Cells\CellsApi;
use Aspose\Cells\Configuration;

$config = new Configuration();
$config->setAppSid("YOUR_APP_SID");
$config->setAppKey("YOUR_APP_KEY");

$cellsApi = new CellsApi(null, $config);

$result = $cellsApi->exportSpreadsheetAsFormat(
    "MyWorkbook.xlsx",
    "PDF",
    null, // folder
    null, // storage
    "exported/MyWorkbook.pdf"
);

echo "Exported to: " . $result . "\n";
```

### Node.js (TypeScript)

```typescript
import { CellsApi } from "aspose-cells-cloud";

const config = new Configuration({
  appSid: "YOUR_APP_SID",
  appKey: "YOUR_APP_KEY"
});

const cellsApi = new CellsApi(config);

const result = await cellsApi.exportSpreadsheetAsFormat(
  "MyWorkbook.xlsx",
  "PDF",
  undefined,
  undefined,
  "exported/MyWorkbook.pdf"
);

console.log(`Exported to: ${result}`);
```

### Ruby

```ruby
require 'aspose_cells_cloud'

configuration = AsposeCellsCloud::Configuration.new
configuration.app_sid = 'YOUR_APP_SID'
configuration.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::CellsApi.new(configuration)

result = api_instance.export_spreadsheet_as_format(
  'MyWorkbook.xlsx',
  'PDF',
  out_path: 'exported/MyWorkbook.pdf'
)

puts "Exported to: #{result}"
```

### Perl

```perl
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new(
  app_sid => 'YOUR_APP_SID',
  app_key => 'YOUR_APP_KEY'
);

my $api = AsposeCellsCloud::CellsApi->new(config => $config);

my $result = $api->export_spreadsheet_as_format(
  'MyWorkbook.xlsx',
  'PDF',
  out_path => 'exported/MyWorkbook.pdf'
);

print "Exported to: $result\n";
```

### Go

```go
import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22"
)

config := cells.NewConfiguration()
config.AppSid = "YOUR_APP_SID"
config.AppKey = "YOUR_APP_KEY"

client := cells.NewCellsApiClient(config)

resp, _, err := client.ExportSpreadsheetAsFormat(
    context.Background(),
    "MyWorkbook.xlsx",
    "PDF",
    nil, nil, "exported/MyWorkbook.pdf",
)

if err != nil {
    log.Fatal(err)
}
fmt.Printf("Exported to: %s\n", *resp)
```

> 📚 See the full [SDK repository on GitHub](https://github.com/aspose-cells-cloud) for installation, authentication, and advanced usage.

---

## Supported Output Formats

| Format | Description | Use Case |
|:-------|:------------|:---------|
| `PDF` | Portable Document Format | Sharing, archiving, printing |
| `XLSX` | Excel Open XML | Modern Excel compatibility |
| `CSV` | Comma-Separated Values | Data import/export, ETL |
| `HTML` | HyperText Markup Language | Web publishing |
| `JSON` | JavaScript Object Notation | API consumption, NoSQL ingestion |
| `ODS` | OpenDocument Spreadsheet | LibreOffice, LibreOffice Online |
| `TIFF` | Tagged Image File Format | Image-based archival, OCR prep |
| `TXT` | Plain Text | Simple data extraction |
| `MHTML` | MIME HTML | Email-ready documents |

> 🔍 Full list of supported formats: [Aspose.Cells Cloud Format Support](/supported-formats/)

---

## HTTP Responses

| Code | Meaning | Description |
|:-----|:--------|:------------|
| `200` | OK | Export successful; file stream returned. |
| `400` | Bad Request | Invalid request parameters (e.g., unsupported format, missing `name`). |
| `401` | Unauthorized | Invalid or missing JWT token. |
| `404` | Not Found | Source file not found in storage. |
| `500` | Internal Server Error | Conversion failed (e.g., corrupted file, unsupported encryption). |

---

## Error Handling

| Error | Cause | Resolution |
|:------|:------|:-----------|
| `400 Bad Request` | Missing `format` or `name`, invalid format value | Validate parameters; use supported formats |
| `401 Unauthorized` | Token expired or malformed | Refresh token; ensure `Bearer` prefix |
| `404 Not Found` | File doesn’t exist in storage | Verify `folder` and `name` path |
| `500 Server Error` | File corrupted, password mismatch, or internal issue | Check file integrity; try unencrypted version first |

---

## Use Cases

✅ **Legacy System Migration**  
Convert thousands of `.xls` files to `.xlsx` for modern Excel support.

✅ **Data Pipeline Normalization**  
Standardize `.ods`, `.xls`, `.csv` inputs to `.json` or `.csv` for ingestion into databases.

✅ **Web Publishing**  
Export financial models to `.html` for embedding in dashboards.

✅ **Archival Standardization**  
Convert all spreadsheets to `.pdf/a` for long-term compliance.

✅ **Interoperability**  
Generate `.ods` for LibreOffice users or `.xlsx` for Google Sheets import.

---

## Why Use This API?

- ✅ **Cloud-Native**: No local processing—entire conversion happens in the cloud.
- ✅ **Zero Infrastructure**: No servers to maintain, scale, or patch.
- ✅ **Pay-as-you-go**: Only pay for actual conversions (no fixed costs).
- ✅ **High Fidelity**: Preserves formatting, formulas, charts, and macros.
- ✅ **Developer Friendly**: SDKs in 8+ languages with full documentation.
- ✅ **Secure**: TLS 1.2+ encryption; JWT authentication; GDPR-compliant data handling.

---

## When *Not* to Use This API

- ❌ **Offline/Local Use**: Prefer local SDKs (e.g., Aspose.Cells for .NET/Java) for air-gapped environments.
- ❌ **Very Large Files (>2 GB)**: Use batch processing or local conversion for files exceeding cloud memory limits.
- ❌ **Real-Time Rendering**: For real-time chart generation, consider image conversion APIs (e.g., `/cells/{name}/worksheets/{sheetName}/render`).

---

## Related Documentation

- [Convert Excel to PDF](/convert-excel-to-pdf/)
- [Compare Two Excel Files](/compare-spreadsheets/)
- [Export Excel to Images (PNG/JPEG)](/convert-excel-to-image/)
- [REST API Overview](/rest-api-overview/)
- [Aspose.Cells Cloud SDKs](https://github.com/aspose-cells-cloud)

---

## Support & Feedback

- 💬 [Aspose.Cells Cloud Forum](https://forum.aspose.cloud/c/cells-cloud)
- 🐛 Report issues: [GitHub Issues](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/issues)
- 📧 Enterprise support: [contact sales](https://www.aspose.cloud/contact-us)

---

> © 2024 Aspose Pty Ltd. All rights reserved. Aspose.Cells Cloud is a registered trademark of Aspose Pty Ltd.