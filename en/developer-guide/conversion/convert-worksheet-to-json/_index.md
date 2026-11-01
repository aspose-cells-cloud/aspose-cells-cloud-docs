---
url: /convert-worksheet-to-json/
title: "Aspose.Cells Cloud Web API – Convert Worksheet to JSON"
date: 2024-03-15
lastmod: 2024-03-15
articleTitle: "How to Convert a Spreadsheet Worksheet to JSON Using Aspose.Cells Cloud API"
linktitle: "Convert Worksheet to JSON"
keywords: "Aspose.Cells, worksheet to JSON, Excel conversion, cloud API, API v4, data export"
description: "Convert Excel worksheets to JSON instantly using Aspose.Cells Cloud API v4. Zero-upload workflow, password protection support, regional formatting, and SDK examples for C#, Java, Python, and more."
weight: 100
type: docs
---

The **ConvertWorksheetToJson** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json`) enables Aspose.Cells Cloud users to convert a specified worksheet from a local spreadsheet file directly into JSON format without uploading to cloud storage. The operation requires a multipart form-data file upload and the worksheet name as a query parameter, supporting password-protected files, custom fonts, regional settings, and optional autofit configurations for rows and columns, ensuring accurate and efficient export of structured worksheet data for downstream applications.

## **Convert Worksheet to JSON API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){rel="noopener noreferrer"}.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
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
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

> **Last updated**: March 15, 2024  
> **API version**: v4.0  
> **SDK status**: Fully supported across all official Aspose.Cells Cloud SDKs.

## Where to Use the Convert Worksheet to JSON API

- **Web dashboards** – Export worksheet data to JSON for client‑side charting libraries (e.g., Chart.js, D3.js).
- **Data migration** – Move legacy Excel data into NoSQL databases or REST services that consume JSON.
- **Mobile or offline apps** – Convert worksheet content to JSON on the server, then sync the lightweight payload to mobile devices.
- **Reporting pipelines** – Feed worksheet data directly into analytics engines that accept JSON input without intermediate CSV steps.

## Why Use the Convert Worksheet to JSON API?

- ✅ **Zero-upload workflow** – Process local files in the cloud without first uploading them to storage, saving bandwidth and storage costs.
- ✅ **Full‑featured conversion** – Supports password‑protected workbooks, custom fonts, regional formatting, and optional row/column autofit.
- ✅ **Fast, scalable execution** – Leverages Aspose.Cells’ high‑performance engine on cloud infrastructure, handling large worksheets efficiently.
- ✅ **Simplified integration** – Single PUT call returns a ready‑to‑use JSON file or stores it directly, reducing code complexity.

## How to Use the Convert Worksheet to JSON API

### Using cURL

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1&region=en-US" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "ewogICJyb3dzIjogWwogICAgeyJjb2x1bW5fMSI6ICJWYWx1ZTEiLCAiY29sdW1uXzIiOiAiVmFsdWUyIn0KICBdCn0=",
  "contentType": "application/json",
  "fileDownloadName": "Sheet1.json"
}
```

{{< /tab >}}
{{< /tabs >}}

### Using Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details and lets you work with spreadsheets using concise code. See the [GitHub repository](https://github.com/aspose-cells-cloud){rel="noopener noreferrer"} for a complete list of Aspose.Cells Cloud SDKs.

{{< tabs tabTotal="8" tabID="2" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}

```csharp
var cellsApi = new CellsApi(clientId, clientSecret);
var response = cellsApi.ConvertWorksheetToJson(
    "myWorkbook.xlsx",
    worksheet: "Sheet1",
    region: "en-US",
    file: File.OpenRead("myWorkbook.xlsx")
);
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
File response = cellsApi.convertWorksheetToJson(
    "myWorkbook.xlsx",
    "Sheet1",
    "en-US",
    null,
    null,
    null,
    null,
    null
);
```

{{< /tab >}}
{{< tab tabNum="3" >}}

```php
$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->convertWorksheetToJson(
    "myWorkbook.xlsx",
    "Sheet1",
    "en-US"
);
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```ruby
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
response = cells_api.convert_worksheet_to_json(
  'myWorkbook.xlsx',
  worksheet: 'Sheet1',
  region: 'en-US'
)
```

{{< /tab >}}
{{< tab tabNum="5" >}}

```typescript
const cellsApi = new CellsApi(clientId, clientSecret);
const response = await cellsApi.convertWorksheetToJson(
  "myWorkbook.xlsx",
  "Sheet1",
  "en-US",
);
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```python
cells_api = CellsApi(client_id, client_secret)
response = cells_api.convert_worksheet_to_json(
    'myWorkbook.xlsx',
    worksheet='Sheet1',
    region='en-US'
)
```

{{< /tab >}}
{{< tab tabNum="7" >}}

```perl
my $cells_api = AsposeCellsCloud::API->new(
    client_id => $client_id,
    client_secret => $client_secret
);
my $response = $cells_api->cells_convert_worksheet_to_json(
    'myWorkbook.xlsx',
    worksheet => 'Sheet1',
    region => 'en-US'
);
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```go
cellsApi, _, _ := NewConfig().NewClient(clientId, clientSecret)
response, _, _ := cellsApi.ConvertWorksheetToJson(
    context.Background(),
    "myWorkbook.xlsx",
    &ConvertWorksheetToJsonOptions{
        Worksheet: stringPtr("Sheet1"),
        Region:    stringPtr("en-US"),
    },
)
```

{{< /tab >}}
{{< /tabs >}}
