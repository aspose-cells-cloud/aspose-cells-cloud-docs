---
title: "Convert Spreadsheet to PDF Using Aspose.Cells Cloud API"
secondtitle: "How to Convert a Local Spreadsheet to PDF Using Aspose.Cells Cloud API"
linktitle: "Convert Spreadsheet to PDF"
type: docs
url: /convert-spreadsheet-to-pdf/
keywords: "excel to pdf, aspose.cells cloud, rest api convert, spreadsheet conversion, cloud pdf generation"
description: "Learn how to convert local spreadsheets (XLS, XLSX, CSV, etc.) to PDF using the Aspose.Cells Cloud API v4.0. Includes request syntax, parameters, authentication, error handling, use cases, and SDK examples."
date: 2024-05-10
lastmod: 2024-06-01
weight: 100
ArticleTitle: "Convert Spreadsheet to PDF with Aspose.Cells Cloud API"
---
The **ConvertSpreadsheetToPdf** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf`) in Aspose.Cells Cloud enables direct conversion of a local spreadsheet file into a PDF document entirely on the cloud server—without requiring the file to be stored in cloud storage first—by accepting the source file as a multipart/form-data upload and returning the PDF as a binary response stream for immediate download or integration.

The API validates file existence, permissions, and conversion integrity, returning appropriate HTTP status codes and error messages for invalid input or processing failures.

---

## The Convert Spreadsheet to PDF Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### Authentication

The API requires [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). To obtain a token, first authenticate using your `client_id` and `client_secret`:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=YOUR_APP_SID&client_secret=YOUR_APP_KEY" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -s | jq -r '.access_token'
```

Then include the token in the `Authorization` header:

```bash
-H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

---

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

---

### Response

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

### Error Responses

| HTTP Code | Meaning               | Description                                                                    |
| :-------- | :-------------------- | :----------------------------------------------------------------------------- |
| `400`     | Bad Request           | Missing or invalid parameters (e.g., unsupported file type, oversized upload). |
| `401`     | Unauthorized          | Invalid, expired, or missing JWT token.                                        |
| `403`     | Forbidden             | Insufficient permissions to access the resource.                               |
| `404`     | Not Found             | Source file not found or inaccessible.                                         |
| `413`     | Payload Too Large     | File exceeds the 100 MB limit.                                                 |
| `500`     | Internal Server Error | Unexpected server-side failure during conversion.                              |

---

### Success (200 OK)

- **Content-Type**: `application/pdf`
- **Content-Disposition**: `attachment; filename="converted.pdf"`
- **Content-Length**: `<size in bytes>`

**Body**: Binary PDF stream

## Use Cases

- **Automated Reporting Pipelines**: Convert daily Excel reports to PDF for archival, email distribution, or compliance without local processing.
- **Document Management Systems (DMS)**: Store clean PDF snapshots after conversion while retaining originals client-side.
- **Web Export Features**: Enable end users to download a PDF of their edited spreadsheet in-browser—preserving formatting, charts, and formulas.
- **Audit & Compliance Workflows**: Generate immutable, unalterable PDF versions of financial spreadsheets without exposing raw data to cloud storage.
- **Multi-Format Conversion Chains**: Combine with other endpoints (e.g., [Convert Spreadsheet to CSV](/convert-spreadsheet-to-csv/)) for flexible archival or interoperability.

---

## Benefits

- ✅ **Zero-Upload Workflow**: Convert local files directly—no prior upload to cloud storage needed.
- ✅ **High-Fidelity Output**: Accurate rendering of complex layouts, formulas, charts, and formatting—matching desktop Excel.
- ✅ **Scalable & Secure**: Cloud infrastructure handles processing; no client-side dependencies required.
- ✅ **Simple REST Interface**: Single request, optional parameters, and immediate binary response simplify integration.

---

## cURL Example

```bash
# 1. Obtain JWT token
TOKEN=$(curl -s -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=YOUR_APP_SID&client_secret=YOUR_APP_KEY" \
  -H "Content-Type: application/x-www-form-urlencoded" | jq -r '.access_token')

# 2. Convert local file to PDF (streamed response)
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer $TOKEN" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  --output converted.pdf
```

> 💡 Tip: Use `-v` flag for verbose output to inspect headers (e.g., `Content-Disposition`).

---

## SDK Examples

Aspose.Cells Cloud provides SDKs for major languages to simplify integration. Below are representative snippets. For full code and additional features, see the [GitHub repository](https://github.com/aspose-cells-cloud).

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}

```csharp
// Install-Package Aspose.Cells-Cloud -Version 22.8.0
var config = new Configuration { ClientId = "YOUR_APP_SID", ClientSecret = "YOUR_APP_KEY" };
var cellsApi = new CellsApi(config);

using var fileStream = File.OpenRead("myWorkbook.xlsx");
var response = cellsApi.CellsSpreadsheetConvert(fileStream, format: "pdf");
File.WriteAllBytes("converted.pdf", response);
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```java
// Install: com.aspose:aspose-cells-cloud:22.8.0
ApiClient apiClient = new ApiClient("YOUR_APP_SID", "YOUR_APP_KEY", null);
CellsApi cellsApi = new CellsApi(apiClient);

File file = new File("myWorkbook.xlsx");
byte[] result = cellsApi.cellsSpreadsheetConvert(file, "pdf", null, null, null, null, null, null, null);
Files.write(Paths.get("converted.pdf"), result);
```

{{< /tab >}}
{{< tab tabNum="3" >}}

```php
// composer require aspose-cells-cloud/aspose-cells-cloud-php
$config = ['ClientId' => 'YOUR_APP_SID', 'ClientSecret' => 'YOUR_APP_KEY'];
$cellsApi = new \Aspose\Cells\CellsApi(null, null, null, null, $config);

$file = fopen('myWorkbook.xlsx', 'r');
$response = $cellsApi->cellsSpreadsheetConvert($file, 'pdf');
file_put_contents('converted.pdf', $response);
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```ruby
# gem 'aspose_cells_cloud'
require 'aspose_cells_cloud'

AsposeCellsCloud.configure do |config|
  config.client_id = 'YOUR_APP_SID'
  config.client_secret = 'YOUR_APP_KEY'
end

api = AsposeCellsCloud::CellsApi.new
file = File.open('myWorkbook.xlsx', 'rb')
File.binwrite('converted.pdf', api.cells_spreadsheet_convert(file, format: 'pdf'))
```

{{< /tab >}}
{{< tab tabNum="5" >}}

```typescript
// npm install @aspose/cells-cloud
import { CellsApi } from "@aspose/cells-cloud";

const cellsApi = new CellsApi("YOUR_APP_SID", "YOUR_APP_KEY");
const response = await cellsApi.cellsSpreadsheetConvert({
  file: fs.createReadStream("myWorkbook.xlsx"),
  format: "pdf",
});
fs.writeFileSync("converted.pdf", response as Buffer);
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```python
# pip install asposecellscloud
from asposecellscloud.api import CellsApi
from asposecellscloud.models import ConvertDocumentRequest

api = CellsApi(client_id="YOUR_APP_SID", client_secret="YOUR_APP_KEY")

with open("myWorkbook.xlsx", "rb") as f:
    response = api.cells_spreadsheet_convert(
        document=f, format="pdf"
    )
with open("converted.pdf", "wb") as out:
    out.write(response.read())
```

{{< /tab >}}
{{< tab tabNum="7" >}}

```perl
# cpan install LWP::UserAgent JSON
use LWP::UserAgent;
use JSON qw(decode_json);

my $ua = LWP::UserAgent->new;
my $resp = $ua->post("https://api.aspose.cloud/connect/token",
  Content_Type => "form",
  Content => [
    grant_type => "client_credentials",
    client_id => "YOUR_APP_SID",
    client_secret => "YOUR_APP_KEY"
  ]);

my $token = decode_json($resp->content)->{access_token};

$resp = $ua->put("https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf",
  Authorization => "Bearer $token",
  Content_Type => "multipart/form-data",
  Content => [ Spreadsheet => ["myWorkbook.xlsx"] ]);

open my $fh, '>', 'converted.pdf';
print $fh $resp->decoded_content;
close $fh;
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go
import (
  "os"
  "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v40"
)

config := cells.NewConfiguration()
config.ClientId = "YOUR_APP_SID"
config.ClientSecret = "YOUR_APP_KEY"
api := cells.NewCellsApiConfiguration(config)

file, _ := os.Open("myWorkbook.xlsx")
defer file.Close()

pdfBytes, _, err := api.CellsSpreadsheetConvert(context.Background(), "pdf", file, nil, nil, nil, nil, nil, nil, nil, nil)
if err != nil { log.Fatal(err) }
os.WriteFile("converted.pdf", pdfBytes, 0644)
```

{{< /tab >}}
{{< /tabs >}}
