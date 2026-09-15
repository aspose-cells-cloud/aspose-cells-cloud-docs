---
url: /remove-characters-by-position/
title: Remove Characters by Position in Excel – Aspose.Cells Cloud API v4
date: 2024-03-15T10:00:00Z
description: "Use Aspose.Cells Cloud Web API to precisely delete characters from Excel cells by position — first/last N characters, before/after markers, or between delimiters. Includes SDK examples in 8 languages."
keywords:
  - "Aspose.Cells Cloud"
  - "remove characters by position"
  - "Excel text cleaning"
  - "delete first N characters"
  - "delete last N characters"
  - "remove text before marker"
  - "remove text after marker"
  - "between values removal"
weight: 100
canonical: /remove-characters-by-position/
---

## Introduction

Remove unwanted characters from Excel cells based on positional rules. Aspose.Cells Cloud Web API supports five deletion modes: first N characters, last N characters, before/after a substring, or between two delimiters. This enables precise text cleaning without complex regex, ideal for data standardization, log parsing, and batch preprocessing.

## Position Modes

The API supports the following position-based removal strategies:

| Mode | Description |
|------|-------------|
| `theFirstNCharacters` | Removes the first *N* characters from each selected cell. |
| `theLastNCharacters` | Removes the last *N* characters from each selected cell. |
| `allCharactersBeforeText` | Deletes all text before the first occurrence of the specified substring. |
| `allCharactersAfterText` | Deletes all text after the first occurrence of the specified substring. |
| `BetweenValues` | Removes the substring between two delimiters. Optionally excludes the delimiters themselves using the `includingDelimiters` parameter (see [Options](#options)). |

## Options

| Option | Type | Description |
|--------|------|-------------|
| `caseSensitive` | Boolean | Controls case sensitivity for `allCharactersBeforeText`, `allCharactersAfterText`, and `BetweenValues`. Default: `false`. |
| `includingDelimiters` | Boolean *(not exposed in query params)* | Applies only to `BetweenValues` mode. When `false`, the delimiter strings themselves are retained; when `true`, they are removed along with the inner content. *(Note: This option is internal to the API service and may be set via SDK or body payload in future versions.)* |

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### Security and Authentication

The API requires [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name | Type | Location | Required | Description |
|----------------|------|----------|----------|-------------|
| `Spreadsheet` | File | FormData | ✅ Yes | The Excel file to process (XLSX, XLS, ODS, CSV, etc.). |
| `theFirstNCharacters` | Integer | Query | ❌ No | Number of leading characters to remove. |
| `theLastNCharacters` | Integer | Query | ❌ No | Number of trailing characters to remove. |
| `allCharactersBeforeText` | String | Query | ❌ No | Remove all text before the first occurrence of this substring. |
| `allCharactersAfterText` | String | Query | ❌ No | Remove all text after the first occurrence of this substring. |
| `caseSensitive` | Boolean | Query | ❌ No | Whether substring matching is case-sensitive. |
| `worksheet` | String | Query | ❌ No | Target worksheet name. Defaults to the first worksheet. |
| `range` | String | Query | ❌ No | Cell range (e.g., `"A1:C10"`). Defaults to all used cells in the worksheet. |
| `outPath` | String | Query | ❌ No | Cloud storage path for output file. If omitted, saved in source folder. |
| `outStorageName` | String | Query | ❌ No | Name of the cloud storage for output. |
| `region` | String | Query | ❌ No | Locale setting (e.g., `"en-US"`, `"zh-CN"`), affecting text encoding and parsing. |
| `password` | String | Query | ❌ No | Password for protected workbooks. |

> **Note**: Only one primary mode (`theFirstNCharacters`, `theLastNCharacters`, `allCharactersBeforeText`, `allCharactersAfterText`, or `BetweenValues`) should be specified per request. Combining modes yields undefined behavior.

### Response

On success, returns the cleaned workbook as a binary stream (`Content-Type: application/octet-stream`).

```json
{
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

### Error Codes

| Status Code | Description |
|-------------|-------------|
| `200 OK` | Request succeeded; cleaned file returned. |
| `400 Bad Request` | Invalid parameter values or malformed request URI. |
| `401 Unauthorized` | Invalid or expired access token. |
| `404 Not Found` | Specified file or storage path not found. |
| `500 Server Error` | Internal error during file processing. |

## Use Cases

- **Data Standardization**: Strip leading zeros from product codes or country codes from phone numbers.
- **Log Parsing**: Extract messages by removing timestamps or prefixes (e.g., `[INFO] `).
- **Filename Organization**: Remove uniform date prefixes or suffixes from bulk file lists.
- **Structured Text Extraction**: Isolate content between delimiters (e.g., `[id:12345]` → `12345`).
- **Database Import Prep**: Clean imported CSV/Excel fields (e.g., remove trailing commas, leading quotes).

## Benefits

- **Precision**: Position-based logic avoids regex complexity and false positives.
- **Batch Efficiency**: Apply rules across entire worksheets or ranges in a single request.
- **Preservation**: Formatting, formulas, and data validation remain intact.
- **Developer Experience**: Prebuilt SDKs for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go accelerate integration.

> Customers report up to **90% reduction** in text-cleaning time for large workbooks compared to manual or spreadsheet-native approaches. *(See [Aspose.Cells Cloud Case Studies](https://www.aspose.com/cloud/case-studies/) for verified examples.)*

## OpenAPI Specification

The public OpenAPI definition for this endpoint is available at the [Aspose.Cells Cloud API Reference](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet).

## SDK Examples

Using an SDK is recommended for production use. The SDK handles authentication, serialization, and error handling.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
```csharp
// See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/blob/master/Examples/Cells/TextProcessing/RemoveCharactersByPosition.cs
var cellsApi = new CellsApi(clientId, clientSecret);
var response = await cellsApi.CellsContentRemoveCharactersByPositionAsync(
    file: new FileInfo("input.xlsx"),
    theFirstNCharacters: 3,
    worksheet: "Sheet1",
    range: "A1:A10"
);
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```java
// See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Examples/src/main/java/com/aspose/cells/examples/TextProcessing/RemoveCharactersByPosition.java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
File response = cellsApi.cellsContentRemoveCharactersByPosition(
    "input.xlsx",
    3, // theFirstNCharacters
    "Sheet1", // worksheet
    "A1:A10" // range
);
```
{{< /tab >}}
{{< tab tabNum="3" >}}
```php
// See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/Samples/TextProcessing/RemoveCharactersByPosition.php
$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->cellsContentRemoveCharactersByPosition(
    "input.xlsx",
    3,
    "Sheet1",
    "A1:A10"
);
```
{{< /tab >}}
{{< tab tabNum="4" >}}
```ruby
# See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/blob/master/examples/remove_characters_by_position.rb
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
response = cells_api.cells_content_remove_characters_by_position(
  "input.xlsx",
  the_first_n_characters: 3,
  worksheet: "Sheet1",
  range: "A1:A10"
)
```
{{< /tab >}}
{{< tab tabNum="5" >}}
```typescript
// See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/blob/master/examples/text-processing/remove-characters-by-position.ts
const cellsApi = new CellsApi(clientId, clientSecret);
const response = await cellsApi.cellsContentRemoveCharactersByPosition(
  "input.xlsx",
  3,
  "Sheet1",
  "A1:A10"
);
```
{{< /tab >}}
{{< tab tabNum="6" >}}
```python
# See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/blob/master/examples/text_processing/remove_characters_by_position.py
cells_api = CellsApi(client_id, client_secret)
response = cells_api.cells_content_remove_characters_by_position(
    "input.xlsx",
    the_first_n_characters=3,
    worksheet="Sheet1",
    range="A1:A10"
)
```
{{< /tab >}}
{{< tab tabNum="7" >}}
```perl
# See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/blob/master/examples/remove-characters-by-position.pl
my $cells_api = AsposeCellsCloud::API->new(
    client_id => $client_id,
    client_secret => $client_secret
);
my $response = $cells_api->cells_content_remove_characters_by_position(
    "input.xlsx",
    the_first_n_characters => 3,
    worksheet => "Sheet1",
    range => "A1:A10"
);
```
{{< /tab >}}
{{< tab tabNum="8" >}}
```go
// See full example at: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/blob/master/examples/textprocessing/removecharactersbyposition.go
cfg := cells.NewConfiguration(clientId, clientSecret)
api := cells.NewAPIClient(cfg)
resp, _, err := api.CellsApi.CellsContentRemoveCharactersByPosition(
    context.Background(),
    "input.xlsx",
    cellsApi.CellsContentRemoveCharactersByPositionOpts{
        TheFirstNCharacters: 3,
        Worksheet:           "Sheet1",
        Range:               "A1:A10",
    },
)
```
{{< /tab >}}
{{< /tabs >}}

> Explore the full SDK source and examples at [GitHub](https://github.com/aspose-cells-cloud).

## See Also

- [Batch Text Processing API](/batch-text-processing/)
- [Replace Text in Excel](/replace-text/)
- [Find and Replace](/find-replace/)
- [Extract Text from Excel](/extract-text/)

## License

Aspose.Cells Cloud APIs are available under the [Aspose Cloud Terms of Use](https://www.aspose.com/legal/terms-of-use/). Free trial accounts include 100 free API calls per day and 2 GB storage.