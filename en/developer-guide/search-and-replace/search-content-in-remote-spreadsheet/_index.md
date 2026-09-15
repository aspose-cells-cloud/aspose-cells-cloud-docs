---
url: /search-content-in-remote-spreadsheet/
title: "Search Text in Remote Excel Spreadsheets – Aspose.Cells Cloud API"
second_title: "Search Content in Remote Spreadsheet API"
linktitle: "Search Remote Spreadsheet Content"
date: 2024-03-15T09:00:00Z
lastmod: 2024-05-20T14:30:00Z
description: "Learn how to programmatically search text, numbers, or formulas in Excel files stored in cloud storage using Aspose.Cells Cloud REST API — with case-insensitive matching, folder support, and password handling."
keywords: "Aspose.Cells, Excel search API, cloud spreadsheet, text search, REST"
weight: 100
---

## Search Content in Remote Spreadsheet API

Programmatically search for specific text, numbers, or formulas in Excel workbooks stored in cloud storage using the Aspose.Cells Cloud REST API. This operation scans all worksheets and cells remotely—no file download required—and returns precise locations of matches, enabling automated data discovery, compliance auditing, and template validation workflows.

## Prerequisites

Before using this API, ensure you have:

- An active [Aspose.Cells Cloud account](https://dashboard.aspose.cloud/)  
- Your **Client ID** and **Client Secret** from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/)  
- A workbook uploaded to your cloud storage (see [Upload Files to Cloud Storage](/cloud-storage/upload-file/))  
- SDK or HTTP client configured for JWT authentication  

## Web API Endpoint

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

## Authentication

All requests require a valid JWT Bearer token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

```http
Authorization: Bearer {access_token}
```

## Request Parameters

| Parameter     | Type    | Location | Required | Description |
|---------------|---------|----------|----------|-------------|
| `name`        | string  | Path     | ✅ Yes   | Filename of the Excel workbook (e.g., `sales_data.xlsx`). |
| `searchText`  | string  | Query    | ✅ Yes   | Text, number, or partial string to locate. |
| `ignoringCase`| boolean | Query    | ❌ No    | `true` for case-insensitive matching (default: `true`). |
| `folder`      | string  | Query    | ❌ No    | Directory path in cloud storage (default: root). |
| `storageName` | string  | Query    | ❌ No    | Custom storage identifier (default: configured account storage). |
| `region`      | string  | Query    | ❌ No    | Locale (e.g., `en-US`, `fr-FR`) affecting number/date parsing and text collation. |
| `password`    | string  | Query    | ❌ No    | Decryption password for password-protected files. Omit if not encrypted. |

## Example Request (cURL)

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/sales_data.xlsx/search/content?searchText=Q3&ignoringCase=true&folder=Reports" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json"
```

## Response

Returns a `SearchResponse` object with HTTP status `200 OK`, containing an array of match results.

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "sales_data.xlsx",
      "Worksheet": "Q3_Summary",
      "Position": "B5",
      "Content": "Q3 Revenue: $1.2M"
    },
    {
      "Filename": "sales_data.xlsx",
      "Worksheet": "Notes",
      "Position": "D12",
      "Content": "Q3 launch target met"
    }
  ]
}
```

### Response Fields

| Field      | Type   | Description |
|------------|--------|-------------|
| `Filename` | string | Source workbook name. |
| `Worksheet`| string | Worksheet containing the match. |
| `Position` | string | Cell address (e.g., `B5`) of the match. |
| `Content`  | string | Full cell value where the match occurred. |

> ⚠️ If no matches are found, `TextItems` is an empty array (`[]`), but the request still returns HTTP `200 OK`.

## Error Handling

| Status Code | Error Code | Description |
|-------------|------------|-------------|
| `400` | `Invalid request URI` | Malformed URL or invalid parameter. |
| `401` | `Invalid access token` | Missing, expired, or invalid JWT token. |
| `404` | `File not found` | Workbook does not exist or path is incorrect. |
| `500` | `Internal server error` | Unexpected server-side failure (e.g., unsupported file format). |

## Use Cases

### Compliance & Security Auditing
Scan entire workbooks for sensitive terms (e.g., `"Confidential"`, `"PII"`, `"GDPR"`) to enforce data governance and detect policy violations.

### Cross-Worksheet Data Linking
Locate project IDs, customer names, or SKUs across multiple sheets to validate data consistency and trace dependencies.

### Template Validation
After report automation, verify placeholder replacement (e.g., `{{Date}}`) across hundreds of files to ensure output integrity.

### Historical Data Mining
Search legacy archives for event codes (e.g., `"Bankruptcy"`, `"Merger"`) to extract business logic and support legacy system migration.

## Benefits

- **Developer-Friendly** – SDKs for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go accelerate integration  
- **Zero Infrastructure** – Fully managed cloud service; no servers, updates, or compatibility overhead  
- **Cost-Effective** – Pay-per-use pricing model with no upfront investment  
- **Format Preservation** – Search results retain original Excel formatting; export to PDF or other formats if needed  

## Code Examples

Using Aspose.Cells Cloud SDKs is the recommended approach for development. Below are minimal examples in each supported language.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
```csharp
// See full example at: 
// https://github.com/aspose-cells-cloud/aspose-cells-cloud-csharp/blob/master/Examples/Cells/SearchTextInRemoteSpreadsheet.cs

var cellsApi = new CellsApi(clientId, clientSecret);
var result = await cellsApi.SearchContentInRemoteSpreadsheet(
    name: "sales_data.xlsx",
    searchText: "Q3",
    ignoringCase: true,
    folder: "Reports"
);
Console.WriteLine($"Found {result.TextItems?.Count ?? 0} matches.");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
// Full example: 
// https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Examples/src/main/java/com/aspose/cells/cloud/examples/Cells/SearchTextInRemoteSpreadsheet.java

CellsApi cellsApi = new CellsApi(clientId, clientSecret);
SearchResponse result = cellsApi.searchContentInRemoteSpreadsheet(
    "sales_data.xlsx",
    "Q3",
    true,
    "Reports",
    null,
    null,
    null
);
System.out.println("Matches found: " + result.getTextItems().size());
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
// Full example: 
// https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/examples/Cells/SearchTextInRemoteSpreadsheet.php

$cellsApi = new CellsApi($clientId, $clientSecret);
$result = $cellsApi->SearchContentInRemoteSpreadsheet(
    "sales_data.xlsx",
    "Q3",
    true,
    "Reports"
);
echo "Matches: " . count($result->getTextItems());
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
# Full example: 
# https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/blob/master/examples/cells/search_text_in_remote_spreadsheet.rb

cells_api = AsposeCellsCloud::CellsApi.new(client_id: client_id, client_secret: client_secret)
result = cells_api.search_content_in_remote_spreadsheet(
  name: 'sales_data.xlsx',
  search_text: 'Q3',
  ignoring_case: true,
  folder: 'Reports'
)
puts "Found #{result.text_items.length} matches"
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```typescript
// Full example: 
// https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/blob/master/examples/cells/searchTextInRemoteSpreadsheet.ts

const cellsApi = new CellsApi(clientId, clientSecret);
const result = await cellsApi.searchContentInRemoteSpreadsheet(
  'sales_data.xlsx',
  'Q3',
  true,
  'Reports'
);
console.log(`Matches: ${result.body.textItems?.length ?? 0}`);
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```python
# Full example: 
# https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/blob/master/examples/cells/search_text_in_remote_spreadsheet.py

cells_api = CellsApi(client_id, client_secret)
result = cells_api.search_content_in_remote_spreadsheet(
    'sales_data.xlsx',
    'Q3',
    ignoring_case=True,
    folder='Reports'
)
print(f"Matches: {len(result.body.text_items or [])}")
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```perl
# Full example: 
# https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/blob/master/examples/Cells/SearchTextInRemoteSpreadsheet.pl

my $cells_api = AsposeCellsCloud::CellsApi->new(
    -client_id => $client_id,
    -client_secret => $client_secret
);
my $result = $cells_api->search_content_in_remote_spreadsheet(
    'sales_data.xlsx',
    'Q3',
    1,
    'Reports'
);
print "Matches: " . scalar(@{$result->{TextItems}}) . "\n";
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```go
// Full example: 
// https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/blob/master/examples/cells/search_text_in_remote_spreadsheet.go

cellsAPI, _, _ := cells.NewCellsApiClient(clientID, clientSecret)
result, _, err := cellsAPI.SearchContentInRemoteSpreadsheet(
    context.Background(),
    "sales_data.xlsx",
    &cells.SearchContentInRemoteSpreadsheetOptions{
        SearchText:   to.String("Q3"),
        IgnoringCase: to.Bool(true),
        Folder:       to.String("Reports"),
    },
)
fmt.Printf("Matches: %d\n", len(*result.TextItems))
```
{{< /tab >}}

{{< /tabs >}}

> 💡 **Note**: All examples use SDK v23.5+ and require valid credentials. Replace placeholder values (`clientId`, `clientSecret`, `name`, `searchText`, `folder`) with your own.

## OpenAPI Reference

Explore the full API specification and test directly in your browser:  
[Aspose.Cells Cloud API Reference – SearchContentInRemoteSpreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet)

## See Also

- [Upload Files to Cloud Storage](/cloud-storage/upload-file/)  
- [Convert Excel to PDF](/convert-excel/)  
- [Save As Options](/save-as/)  
- [Excel File Security Best Practices](/security/)  

<!-- alt="Search API workflow: Developer → Auth Token → PUT /cells/{name}/search/content → Cloud Storage → Response with TextItems array" -->