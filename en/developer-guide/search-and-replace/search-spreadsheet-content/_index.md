---
url: /search-spreadsheet-content/
title: "Search Spreadsheet Content – Aspose.Cells Cloud API"
date: 2024-03-15T10:00:00Z
lastmod: 2024-03-15T10:00:00Z
draft: false
linktitle: "Search Spreadsheet Content"
type: docs
keywords: "Excel search API, spreadsheet content search, text lookup in Excel, cloud spreadsheet API, find text in Excel"
description: "Use Aspose.Cells Cloud REST API to search for text, numbers, or formulas in Excel files uploaded locally. Supports case-insensitive, worksheet-scoped, and range-limited searches with JWT-based security."
weight: 100
---

# Search Spreadsheet Content

Programmatically search for specific text within Excel spreadsheets using the Aspose.Cells Cloud API. This operation uploads a local file to the cloud service, performs a content search, and returns matched cells—including worksheet name, cell address, and matched text—without requiring prior storage in the cloud.

---

## Web API Endpoint

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

> **Note:** Authentication requires a valid JWT token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

---

## Request Parameters

| Parameter    | Type    | Location    | Required | Description |
|--------------|---------|-------------|----------|-------------|
| `spreadsheet` | File    | FormData    | Yes      | The Excel file to search. |
| `searchText`  | String  | Query       | Yes      | The text (or numeric value) to locate. |
| `ignoringCase`| Boolean | Query       | No       | Whether to ignore case in the search. Default: `true`. |
| `worksheet`   | String  | Query       | No       | Name of the worksheet to limit the search scope. If omitted, all worksheets are scanned. |
| `cellArea`    | String  | Query       | No       | A1-style range (e.g., `A1:C10`) to restrict the search area. |
| `region`      | String  | Query       | No       | Locale setting (e.g., `en-US`, `fr-FR`) affecting number/date parsing. |
| `password`    | String  | Query       | No       | Password for protected workbooks. |

---

## Response

The API returns a `SearchResponse` object containing an array of matched items.

### Example Response

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

Each `textItem` includes:
- `cellName`: A1-style cell reference (e.g., `"A1"`).
- `text`: The matched string.
- `occurrences`: Number of times the text appears in that cell.

---

## Error Handling

| Code | Description |
|------|-------------|
| `400 Bad Request` | Invalid URL, malformed parameters, or unsupported file format. |
| `401 Unauthorized` | Missing, expired, or invalid JWT token. |
| `404 Not Found` | The uploaded file cannot be accessed or does not exist. |
| `500 Internal Server Error` | Unexpected error during processing (e.g., corrupted workbook). |

---

## Use Cases

### Compliance & Security Audits
Scan workbooks for sensitive terms (e.g., `"Confidential"`, `"PII"`, `"Internal"`) to support data governance and regulatory compliance.

### Cross-Sheet Data Discovery
Find identifiers (e.g., project numbers, customer IDs) across multiple worksheets to map data relationships.

### Template Verification
Validate that placeholders like `{{Date}}` or `{{User}}` are fully replaced after batch report generation.

### Legacy Data Mining
Search historical Excel files for event codes, transaction types, or business terms to accelerate archival analysis.

---

## Benefits

- **No Infrastructure Overhead**: Search runs in the cloud—no local processing or storage required.
- **Flexible Scope**: Limit searches to specific worksheets, ranges, or the entire workbook.
- **Developer-Friendly SDKs**: Pre-built clients available for [C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go](https://github.com/aspose-cells-cloud).
- **Secure by Default**: All requests require JWT authentication; files are processed temporarily and not retained.

> **Note**: While no infrastructure management is needed for cloud-hosted usage, on-premises deployments (e.g., Aspose.Cells Cloud for Docker) may be required for air-gapped environments.

---

## SDK Integration

Using an SDK simplifies integration by handling HTTP requests and response parsing. Below are examples for common languages:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{</tabs >}}

> **Tip**: For production use, pin SDK versions and Gist commits to avoid breakage from upstream changes. See the [Aspose.Cells Cloud GitHub organization](https://github.com/aspose-cells-cloud) for the latest SDK releases.

---

## OpenAPI Specification

The API conforms to the OpenAPI 2.0 (Swagger) standard. You can view or download the full specification here:  
[OpenAPI Specification (Swagger JSON)](https://reference.aspose.cloud/cells/v2.0/cells/swagger.json)

---

## Related Operations

- [Export Excel to PDF](/export-excel-to-pdf/)
- [Convert Excel to CSV](/convert-excel-to-csv/)
- [Validate Excel Files](/validate-excel-files/)