---
url: /convert-spreadsheet/
title: "Convert Spreadsheet Using Aspose.Cells Cloud API"
description: "Free online tool & API documentation to convert Excel, CSV, and other spreadsheet formats (XLSX, PDF, ODS, etc.) via Aspose.Cells Cloud REST API."
second_title: "Aspose.Cells Cloud"
ArticleTitle: "Convert Spreadsheet"
linktitle: "Convert Spreadsheet"
type: docs
date: 2024-05-15
lastmod: 2024-06-20
weight: 20
tags: ["api", "rest", "conversion", "spreadsheet", "cloud"]
canonical: "/convert-spreadsheet/"
keywords: "Aspose, Aspose.Cells, spreadsheet conversion, Excel to PDF, Excel API, cloud file conversion"
description: "Convert a spreadsheet file to another format using the Aspose.Cells Cloud API."
---

Convert a local spreadsheet or Excel file to another format using the Aspose.Cells Cloud API. This cloud-native operation accepts your local file via `multipart/form-data`, performs conversion entirely on the server, and returns the result directly—no intermediate storage required.

## Convert Spreadsheet API

### API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### Authentication

Aspose.Cells Cloud APIs use [JWT token–based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include your access token in the `Authorization` header:

```http
Authorization: Bearer {your-access-token}
```

> **Note:** Replace `{your-access-token}` with your valid JWT access token. See [Authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

### Request Parameters

| Parameter Name     | Type   | Location        | Required | Description |
|--------------------|--------|-----------------|----------|-------------|
| `Spreadsheet`      | File   | FormData        | ✅ Yes   | Upload the spreadsheet file to be converted. |
| `format`           | String | Query           | ✅ Yes   | Desired output format (e.g., `"Xlsx"`, `"Pdf"`, `"Csv"`). Case-insensitive. |
| `outPath`          | String | Query           | ❌ No    | Folder path where the converted workbook will be stored. Default is `null`. |
| `outStorageName`   | String | Query           | ❌ No    | Name of the output file storage. |
| `fontsLocation`    | String | Query           | ❌ No    | Custom font directory for rendering. |
| `AutoRowsFit`      | Boolean| Query           | ❌ No    | (Optional) Auto-fit all rows in worksheets. Default: `false`. |
| `AutoColumnsFit`   | Boolean| Query           | ❌ No    | (Optional) Auto-fit all columns in worksheets. Default: `false`. |
| `region`           | String | Query           | ❌ No    | Locale setting (e.g., `"en-US"`, `"fr-FR"`), affecting number/date formatting. |
| `password`         | String | Query           | ❌ No    | Password for protected spreadsheets. |

### Supported Output Formats

| Format | Description |
|--------|-------------|
| `XLS`, `XLSX`, `XLSB`, `XLSM`, `XLT`, `XLTX`, `XLTM`, `XLSAM`, `XLAM` | Microsoft Excel formats (95–2021) |
| `CSV`, `TSV` | Comma/tab-separated values |
| `TXT` | Plain text (delimited) |
| `HTML`, `MHTML`, `XHTML` | Web formats |
| `ODS`, `OTS`, `SXC`, `FODS` | OpenDocument formats |
| `Numbers` | Apple Numbers documents |
| `JSON`, `XML`, `SQL`, `Markdown`, `DIF`, `DBF`, `XML` | Data interchange & markup formats |
| `PDF`, `XPS`, `SVG`, `TIFF`, `PNG`, `BMP`, `EMF`, `JPEG`, `GIF` | Document & image formats |
| `DOCX`, `PPTX` | Word & PowerPoint documents |
| `EPUB`, `AZW3` | E-book formats |

> **Note:** Format names should be used in uppercase (e.g., `PDF`, `XLSX`, `CSV`). For compatibility, the API accepts mixed-case equivalents (e.g., `pdf`, `xlsx`).

### Response

**Success Response (200 OK)**  
Returns the converted file as a binary stream.

- `Content-Type`: MIME type of the output format (e.g., `application/pdf`, `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`)
- `Content-Disposition`: `attachment; filename="output.pdf"`

**Example Response Headers**
```
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="converted.pdf"
Content-Length: 8423
```

### HTTP Status Codes

| Code | Meaning | Description |
|------|---------|-------------|
| `200` | OK | Conversion succeeded; response body contains the file stream. |
| `400` | Bad Request | Missing or invalid parameters (e.g., unsupported format, malformed request). |
| `401` | Unauthorized | Invalid or missing JWT token. |
| `413` | Payload Too Large | File exceeds maximum allowed size (100 MB). |
| `404` | Not Found | Source file not found or inaccessible (for cloud-stored paths). |
| `500` | Internal Server Error | Unexpected server error during conversion. |

### Error Handling

- **400 Bad Request**: Invalid URL, unsupported format, or invalid file structure.  
- **401 Unauthorized**: Authentication failed or credentials missing.  
- **404 Not Found**: Source file not found or inaccessible.  
- **500 Server Error**: Conversion failed due to internal anomaly (e.g., corrupted input, unsupported macro).

## Use Cases

- **Legacy System Migration**: Bulk convert XLS files to XLSX for modern Excel compatibility.  
- **Archive Standardization**: Normalize heterogeneous formats (XLS, ODS, CSV) to a single archival format (e.g., PDF/A or XLSX).  
- **Office Suite Interoperability**: Convert Excel files to ODS, Numbers, or CSV for LibreOffice, Google Sheets, or Apple Numbers.  
- **Data Ingestion**: Export to CSV, JSON, or XML for database or ETL pipeline ingestion.  
- **Web Publishing**: Generate HTML or PDF reports directly from Excel models.

## Key Features & Benefits

- ✅ **Cloud-Native Conversion**: Process local files without uploading to cloud storage.  
- ✅ **Reduced Resource Burden**: No need to store intermediate files in the cloud.  
- ✅ **Format Versatility**: Support for 40+ input and output formats.  
- ✅ **Simplified Workflow**: End-to-end conversion in a single API call.  
- ✅ **Data Fidelity**: Preserves formatting, formulas, charts, and embedded objects.

## Code Examples

### cURL Request

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf&region=en-US" \
  -H "Authorization: Bearer {your-access-token}" \
  -F "Spreadsheet=@/path/to/file.xlsx" \
  -o output.pdf
```

> Replace `{your-access-token}` with your valid JWT token.

### Using Aspose.Cells Cloud SDKs

SDKs are available for **C#**, **Java**, **PHP**, **Ruby**, **Node.js**, **Python**, **Perl**, and **Go**. See the [GitHub repository](https://github.com/aspose-cells-cloud) for source and examples.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
```csharp
var cellsApi = new CellsApi(clientId, clientSecret);
var response = cellsApi.CellsConvertSpreadsheet(
    "input.xlsx", 
    "PDF", 
    region: "en-US"
);
File.WriteAllBytes("output.pdf", response);
```
{{</tab>}}
{{<tab tabNum="2" >}}
```java
CellsApi api = new CellsApi(clientId, clientSecret);
File result = api.cellsConvertSpreadsheet(
    "input.xlsx", 
    "PDF", 
    null, 
    null, 
    "en-US", 
    null, 
    null, 
    null, 
    null, 
    null
);
```
{{</tab>}}
{{<tab tabNum="3" >}}
```php
$api = new CellsApi($clientId, $clientSecret);
$result = $api->cellsConvertSpreadsheet("input.xlsx", "PDF", region: "en-US");
file_put_contents("output.pdf", $result);
```
{{</tab>}}
{{<tab tabNum="4" >}}
```ruby
api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
result = api.cells_convert_spreadsheet('input.xlsx', 'PDF', region: 'en-US')
File.write('output.pdf', result)
```
{{</tab>}}
{{<tab tabNum="5" >}}
```typescript
const cellsApi = new CellsApi(clientId, clientSecret);
const result = await cellsApi.cellsConvertSpreadsheet('input.xlsx', 'PDF', { region: 'en-US' });
fs.writeFileSync('output.pdf', result as Buffer);
```
{{</tab>}}
{{<tab tabNum="6" >}}
```python
api = CellsApi(client_id, client_secret)
result = api.cells_convert_spreadsheet('input.xlsx', 'PDF', region='en-US')
with open('output.pdf', 'wb') as f:
    f.write(result)
```
{{</tab>}}
{{<tab tabNum="7" >}}
```perl
my $api = AsposeCellsCloud::API->new(
    client_id => $clientId,
    client_secret => $clientSecret
);
my $result = $api->cells_convert_spreadsheet(
    'input.xlsx',
    'PDF',
    { region => 'en-US' }
);
```
{{</tab>}}
{{<tab tabNum="8" >}}
```go
api := cells.NewCellsApi(os.Getenv("CLIENT_ID"), os.Getenv("CLIENT_SECRET"))
result, _, err := api.CellsConvertSpreadsheet(
    context.Background(),
    "input.xlsx",
    "PDF",
    &cells.CellsConvertSpreadsheetOpts{
        Region: stringPtr("en-US"),
    },
)
```
{{</tab>}}
{{< /tabs >}}

## API Specification

- [REST API Reference](https://reference.aspose.cloud/cells/?urls.primaryName=API%20v4#/Conversion/ConvertSpreadsheet)

## Feedback

Was this page helpful?  
[✅ Yes] [❌ No]  
Contact support: [support@aspose.cloud](mailto:support@aspose.cloud)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Convert a spreadsheet file to another format using Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
      "description": "Convert a spreadsheet to the specified format."
    }
  ]
}
</script>