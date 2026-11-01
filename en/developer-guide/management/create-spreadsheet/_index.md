---
title: "Create Spreadsheet API – Aspose.Cells Cloud (v4.0) | Generate Excel Files"
description: "Use Aspose.Cells Cloud REST API to create blank or template-based Excel (XLSX, ODS, CSV) workbooks programmatically."
linktitle: "Create Spreadsheet"
type: docs
url: /create-spreadsheet/
keywords: "Aspose.Cells, spreadsheet API, create Excel, cloud, XLSX, ODS, CSV, template, SDK, automation, REST API"
weight: 100
canonical: "https://reference.aspose.cloud/cells/create-spreadsheet/"
robots: "index, follow"
ArticleTitle: "Aspose.Cells Cloud REST API: Create Excel Spreadsheets (XLSX, ODS, CSV)"
---
The **CreateSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create`) enables developers to programmatically generate new Excel workbooks using Aspose.Cells Cloud, supporting both blank file creation and initialization from optional templates stored in cloud storage; it accepts query parameters such as `format` for the new spreadsheet’s name, `template` for predefined content or formatting, and `region` for locale-specific formatting, allowing efficient automation of report generation and document workflows.

## The Create Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### Security and Authentication

All requests require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){rel="noopener noreferrer"}.

To obtain a JWT token, send a POST request to:

```http
POST https://api.aspose.cloud/connect/token
```

With form data:

```
grant_type=client_credentials&client_id={ClientID}&client_secret={ClientSecret}
```

Include the resulting `access_token` in the `Authorization: Bearer` header for subsequent requests.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| format | String | Query | Specifies the name of the new spreadsheet. This name will be used to identify the spreadsheet in the system. |
| template | String | Query | template: Optional.If provided, the new spreadsheet will be created based on the specified template.This can be useful for applying predefined layouts and styles. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

The API returns the generated file as a binary stream in the response body.

### Example: cURL Request

```bash
# 1. Obtain JWT token
TOKEN=$(curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=xxxxx&client_secret=xxxxx" \
  -H "Content-Type: application/x-www-form-urlencoded" | jq -r '.access_token')

# 2. Create new XLSX spreadsheet
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer $TOKEN" \
  -o new_report.xlsx
```

### Example: SDK Usage

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}

```csharp
// Install-Package Aspose.Cells.Cloud.Sdk -Version 23.3.0

var cellsApi = new CellsApi("xxxxx", "xxxxx");
var response = cellsApi.CellsSpreadsheetCreate("XLSX", outStorageName: "MyStorage");

if (response != null && response.FileContents != null)
{
    File.WriteAllBytes("new_report.xlsx", response.FileContents);
}
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```java
// Install: com.aspose:aspose-cells-cloud:23.3.0

CellsApi cellsApi = new CellsApi("xxxxx", "xxxxx");
FileContentResult response = cellsApi.cellsSpreadsheetCreate("XLSX", "MyStorage", null, null, null, null);

Files.write(Paths.get("new_report.xlsx"), response.getFileContents());
```

{{< /tab >}}
{{< tab tabNum="3" >}}

```php
// composer require aspose/cells-cloud-php

$cellsApi = new \Aspose\Cells\CellsApi("xxxxx", "xxxxx");
$response = $cellsApi->cellsSpreadsheetCreate("XLSX", "MyStorage");

file_put_contents("new_report.xlsx", $response->getFileContents());
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```ruby
# gem install aspose_cells_cloud

api = AsposeCellsCloud::CellsApi.new("xxxxx", "xxxxx")
response = api.cells_spreadsheet_create("XLSX", out_storage_name: "MyStorage")

File.write("new_report.xlsx", response.file_contents)
```

{{< /tab >}}
{{< tab tabNum="5" >}}

```typescript
// npm install @aspose/cells-cloud

import { CellsApi } from "@aspose/cells-cloud";

const cellsApi = new CellsApi("xxxxx", "xxxxx");
const response = await cellsApi.cellsSpreadsheetCreate("XLSX", {
  outStorageName: "MyStorage",
});

await fs.promises.writeFile(
  "new_report.xlsx",
  Buffer.from(response.fileContents),
);
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```python
# pip install asposecellscloud

from asposecellscloud.api import CellsApi
from asposecellscloud.models import *

cells_api = CellsApi(client_id="xxxxx", client_secret="xxxxx")
response = cells_api.cells_spreadsheet_create(
    format="XLSX",
    out_storage_name="MyStorage"
)

with open("new_report.xlsx", "wb") as f:
    f.write(response.file_contents)
```

{{< /tab >}}
{{< tab tabNum="7" >}}

```perl
# cpan install AsposeCellsCloud

my $config = AsposeCellsCloud::Configuration->new(
    client_id => "xxxxx",
    client_secret => "xxxxx"
);
my $api = AsposeCellsCloud::API::CellsApi->new(config => $config);

my $response = $api->cells_spreadsheet_create(
    format => "XLSX",
    out_storage_name => "MyStorage"
);

open(my $fh, '>', 'new_report.xlsx');
binmode $fh;
print $fh $response->{file_contents};
close $fh;
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go/v23

import (
    "os"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v23/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v23/request"
)

config := api.NewConfig()
config.AppSid = "xxxxx"
config.AppKey = "xxxxx"

cellsApi := api.NewCellsApi(config)
response, _, err := cellsApi.CellsSpreadsheetCreate(
    "XLSX",
    &request.CellsSpreadsheetCreateOptions{OutStorageName: "MyStorage"},
)

if err == nil {
    os.WriteFile("new_report.xlsx", response.FileContents, 0644)
}
```

{{< /tab >}}
{{< /tabs >}}

## Where to Use the Create Spreadsheet API?

### Initialization of Automated Reporting Systems

Create a new blank workbook or generate a report file from a standard template at the start of each daily/weekly automation cycle.

### User Self-Service Portals

Allow customers to select a template (e.g., quotation, project schedule) and instantly download a customized Excel file without developer involvement.

### Batch Data Export and Distribution

Produce separate workbooks with a uniform format for each exported dataset, simplifying downstream processing and distribution.

## Why Use the Create Spreadsheet API?

- **Developer Efficiency**  
  Reduces integration time by 65% compared to custom solutions, with pre-built SDKs for 8+ languages.

- **Cost-Effective Scaling**  
  Pay-per-use pricing model with no upfront licensing fees. Scales automatically with demand.

- **Managed Service**  
  Fully hosted cloud infrastructure eliminates server maintenance, patching, and scaling overhead.

- **Template-Based Consistency**  
  Enforce brand standards and formatting rules using reusable templates stored in cloud storage.

- **Locale-Aware Formatting**  
  Automatically adapt number, date, and currency formats based on the `region` parameter (e.g., `fr-FR` for French conventions).

## Error Handling

| Code | Scenario                                            | Resolution                                                                                  |
| ---- | --------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| 400  | Missing required parameter (e.g., `outStorageName`) | Validate request parameters; ensure `outStorageName` is provided and storage is configured. |
| 404  | Template file not found                             | Confirm the template filename and path are correct in cloud storage.                        |
| 401  | Invalid or expired token                            | Re-authenticate and refresh the JWT token.                                                  |
| 500  | Internal server error                               | Retry the request; if persistent, contact Aspose support with request ID and timestamp.     |

## Best Practices

1. **Use `region` for Localization**  
   Specify `region` (e.g., `en-US`, `de-DE`) to ensure correct date/number formatting per locale.

2. **Secure Template Files**  
   Protect sensitive templates with passwords and pass `password` in the request.

3. **Validate File Formats**  
   Only use supported formats: `XLSX`, `XLS`, `ODS`, `CSV`. Avoid unsupported extensions.

4. **Error Handling in SDKs**  
   Wrap API calls in try-catch blocks and log detailed error responses for debugging.

5. **Caching Templates**  
   Store frequently used templates in cloud storage and reference them by name to avoid re-uploads.
