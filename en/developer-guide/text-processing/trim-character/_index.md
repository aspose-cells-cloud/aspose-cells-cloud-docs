---
url: /trim-character/
title: "Aspose.Cells Cloud Trim Character API - Clean Excel Cell Data"
description: "Use Aspose.Cells Cloud TrimCharacter API to remove extra spaces, line breaks, and non-breaking spaces from Excel cells. Supports XLSX, CSV, ODS, and more via RESTful API. v4.0."
keywords: "excel, text-trimming, aspose.cells, cloud-api, data-cleaning"
date: 2024-04-18
weight: 10
draft: false
---

Clean Excel cell content by removing unnecessary spaces, line breaks, and special characters with the Aspose.Cells Cloud TrimCharacter API. This RESTful endpoint enables programmatic data normalization for improved consistency, accuracy, and professionalism in spreadsheets.

## Overview

The TrimCharacter API provides precise control over text formatting cleanup, supporting:

- **Leading/trailing whitespace removal**  
  Eliminate extra spaces at the start and end of cell values for consistent appearance.

- **Multiple space normalization**  
  Reduce consecutive spaces between words to a single space.

- **Non-breaking space handling**  
  Remove Unicode U+00A0 characters that resist standard `TRIM()` functions.

- **Line break management**  
  Selectively remove extra or all line breaks within cells.

- **Targeted scope control**  
  Apply trimming to a specific worksheet, range (e.g., `"A1:C10"`), or entire workbook.

This API is ideal for cleaning user inputs, customer data, report sources, and pre-migration datasets.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

> **Note**: This documentation applies to Aspose.Cells Cloud API v4.0. For migration guidance to v5.0, see [Aspose.Cells Cloud API Versioning](/cells/working-with-api-versions/).

## Authentication

All requests require a valid JWT access token with the **Cells** scope. Authenticate using your `client_id` and `client_secret` as described in the [REST API Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

Include the token in the `Authorization` header:

```http
Authorization: Bearer {access_token}
```

## Request Parameters

| Parameter                | Type      | Location     | Required | Default | Description |
|--------------------------|-----------|--------------|----------|---------|-------------|
| `Spreadsheet`            | File      | FormData     | ✅ Yes   | —       | Spreadsheet file to process (XLSX, XLS, ODS, CSV, etc.). |
| `trimContent`            | String    | Query        | ❌ No     | `" "`   | Characters or strings to trim (e.g., `" "`, `"#0"`, `"@"`). |
| `trimLeading`            | Boolean   | Query        | ❌ No     | `true`  | Trim content from the beginning of each cell. |
| `trimTrailing`           | Boolean   | Query        | ❌ No     | `true`  | Trim content from the end of each cell. |
| `trimSpaceBetweenWordTo1`| Boolean   | Query        | ❌ No     | `false` | Collapse multiple spaces between words to a single space. |
| `trimNonBreakingSpaces`  | Boolean   | Query        | ❌ No     | `false` | Remove non-breaking spaces (U+00A0). |
| `removeExtraLineBreaks`  | Boolean   | Query        | ❌ No     | `false` | Reduce consecutive line breaks to a single break. |
| `removeAllLineBreaks`    | Boolean   | Query        | ❌ No     | `false` | Remove all line break characters. |
| `worksheet`              | String    | Query        | ❌ No     | —       | Worksheet name to process (defaults to first visible sheet). |
| `range`                  | String    | Query        | ❌ No     | —       | Cell range (e.g., `"A1:C10"`); defaults to all used cells. |
| `outPath`                | String    | Query        | ❌ No     | —       | Destination folder path in cloud storage (default: source folder). |
| `outStorageName`         | String    | Query        | ❌ No     | —       | Cloud storage name for the output file. |
| `region`                 | String    | Query        | ❌ No     | —       | Locale setting (e.g., `"en-US"`, `"fr-FR"`); affects space/line behavior. |
| `password`               | String    | Query        | ❌ No     | —       | Password for protected workbooks. |

> **Best Practice**: Set `trimLeading` and `trimTrailing` explicitly to avoid unintended behavior when `trimContent` is customized.

## Example Request

```bash
curl -X PUT \
  'https://api.aspose.cloud/v4.0/cells/content/trim?trimContent=%20&trimLeading=true&trimTrailing=true&trimSpaceBetweenWordTo1=true&removeAllLineBreaks=true' \
  -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...' \
  -H 'Content-Type: multipart/form-data' \
  -F 'Spreadsheet=@"input.xlsx"'
```

## Response

**Success (HTTP 200)**: Returns a file stream containing the trimmed workbook.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

## Error Codes

| Code | Description |
|------|-------------|
| `400` | Invalid request (e.g., malformed parameters or unsupported file format). |
| `401` | Invalid or expired access token. |
| `403` | Insufficient permissions for the requested operation. |
| `404` | Spreadsheet file not found or inaccessible. |
| `500` | Internal server error during processing. |

## Use Cases

- **User Input Normalization**: Clean free-text entries in forms or surveys before storage.  
- **Customer Data Maintenance**: Standardize names, addresses, and contact fields.  
- **Report Automation**: Preprocess data sources to eliminate formatting artifacts.  
- **Data Migration**: Normalize legacy spreadsheets before loading into new systems.  

## Benefits

- **No Infrastructure Overhead**: Fully managed cloud service—no servers to maintain.  
- **Pay-as-you-go Pricing**: Only billed for API calls and storage used.  
- **Multi-Format Support**: Process XLSX, XLS, ODS, CSV, and more.  
- **Developer-Friendly**: Official SDKs for [C#](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet), [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java), [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python), [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node), [PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php), [Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby), [Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl), and [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).  

## SDK Examples

{{< tabs tabTotal="8" tabID="csharp,java,php,ruby,node,python,perl,go" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab id="csharp" >}}
```csharp
// See full example: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d/Example40_TrimTextInSpreadsheet.cs
var cellsApi = new CellsApi(clientId, clientSecret);
var result = cellsApi.CellsContentTrim("input.xlsx", 
    trimContent: " ", trimLeading: true, trimTrailing: true,
    trimSpaceBetweenWordTo1: true, removeAllLineBreaks: true);
```
{{< /tab >}}
{{< tab id="java" >}}
```java
// See full example: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f/Example40_TrimTextInSpreadsheet.java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
File result = cellsApi.cellsContentTrim("input.xlsx", 
    " ", true, true, true, true, null, null, null, null, null, null);
```
{{< /tab >}}
{{< tab id="php" >}}
```php
// See full example: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152/Example40_TrimTextInSpreadsheet.php
$cellsApi = new CellsApi($clientId, $clientSecret);
$result = $cellsApi->cellsContentTrim("input.xlsx",
    " ", true, true, true, true, null, null, null, null, null, null);
```
{{< /tab >}}
{{< tab id="ruby" >}}
```ruby
# See full example: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca/Example40_TrimTextInSpreadsheet.rb
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
result = cells_api.cells_content_trim('input.xlsx',
  trim_content: ' ', trim_leading: true, trim_trailing: true,
  trim_space_between_word_to1: true, remove_all_line_breaks: true)
```
{{< /tab >}}
{{< tab id="node" >}}
```typescript
// See full example: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0/Example40_TrimTextInSpreadsheet.ts
const cellsApi = new CellsApi(clientId, clientSecret);
const result = await cellsApi.cellsContentTrim("input.xlsx",
  " ", true, true, true, true, undefined, undefined, undefined, undefined, undefined, undefined);
```
{{< /tab >}}
{{< tab id="python" >}}
```python
# See full example: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1/Example40_TrimTextInSpreadsheet.py
cells_api = CellsApi(client_id, client_secret)
result = cells_api.cells_content_trim("input.xlsx",
    trim_content=" ", trim_leading=True, trim_trailing=True,
    trim_space_between_word_to1=True, remove_all_line_breaks=True)
```
{{< /tab >}}
{{< tab id="perl" >}}
```perl
# See full example: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca/Example40_TrimTextInSpreadsheet.pl
my $cells_api = CellsAPI->new(client_id => $clientId, client_secret => $clientSecret);
my $result = $cells_api->cells_content_trim("input.xlsx",
    " ", 1, 1, 1, 1, undef, undef, undef, undef, undef, undef);
```
{{< /tab >}}
{{< tab id="go" >}}
```go
// See full example: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185/Example40_TrimTextInSpreadsheet.go
cellsApi, _ := api.NewCellsApiWithCredentials(os.Getenv("ClientID"), os.Getenv("ClientSecret"))
result, _, _ := cellsApi.CellsContentTrim("input.xlsx",
    " ", true, true, true, true, "", "", "", "", "", "")
```
{{< /tab >}}
{{< /tabs >}}

## Related Resources

- [Authentication Guide](/total/working-with-authentication/)  
- [Cell Formatting API](/cells/text/format-text-in-excel/)  
- [Find & Replace Text](/cells/text/find-and-replace-text-in-excel/)  
- [SDK Documentation Hub](https://github.com/aspose-cells-cloud)  

## Changelog

| Date       | Version | Changes |
|------------|---------|---------|
| 2024-04-18 | v4.0    | Initial published documentation with full parameter coverage. |

---

> **Tip**: For large-scale data cleaning, combine TrimCharacter with [Batch Processing](/cells/batch-process-spreadsheets/) and [Webhook Notifications](/cells/working-with-webhooks/) for end-to-end automation.