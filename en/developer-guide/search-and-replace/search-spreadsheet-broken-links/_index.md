---
url: /search-spreadsheet-broken-links/
title: "Search Spreadsheet Broken Links – Aspose.Cells Cloud API"
second_title: "Reference"
ArticleTitle: "Find & Fix Broken Links in Excel – Cloud Spreadsheet Link Checker"
linktitle: "Search Broken Links"
keywords: "Excel link checker, broken reference detector, cloud spreadsheet audit, Aspose.Cells Cloud API, external reference validation"
description: "Detect broken Excel links—external refs, hyperlinks, formulas—with Aspose.Cells Cloud API for CI/CD and audit workflows."
type: docs
weight: 100
---
The **SearchSpreadsheetBrokenLinks** API (`PUT https://api.aspose.cloud/v4.0/cells/search/broken-links`) in Aspose.Cells Cloud identifies broken hyperlinks, invalid external references, and malformed formulas within a local Excel workbook uploaded via form data. The operation runs server-side in the cloud—no local processing or cloud storage required—and returns results in structured JSON, enabling integration into CI/CD pipelines, audit tools, or compliance workflows.

## The Search Spreadsheet Broken Links Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

### Authentication

All requests require a valid [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include the token in the `Authorization` header as a Bearer token:

```http
Authorization: Bearer {access_token}
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | Specify the worksheet for the replace. |
| cellArea | String | Query | Specify the cell area for the replace. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response Structure

```json
[
  {
    "Name": "BrokenLinksResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "BrokenLinksResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

A successful response returns a `BrokenLinksResponse` object:


#### BrokenLink Object

| Field          | Type   | Description                                                         |
| -------------- | ------ | ------------------------------------------------------------------- |
| `CellName`     | String | Cell address (e.g., `B5`) containing the broken link.               |
| `Link`         | String | Original URL or file path referenced in the cell.                   |
| `ErrorMessage` | String | Human-readable error (e.g., `"File not found"`, `"404 Not Found"`). |
| `Status`       | String | Always `"Broken"` for entries in the `BrokenLinks` array.           |

### Error Codes

| Code                    | Description                                                            |
| ----------------------- | ---------------------------------------------------------------------- |
| `400 Bad Request`       | Invalid request URI, malformed parameters, or unsupported file format. |
| `401 Unauthorized`      | Missing, expired, or invalid access token or credentials.              |
| `404 Not Found`         | Specified file not accessible or upload failed.                        |
| `429 Too Many Requests` | Rate limit exceeded (60 calls/minute).                                 |
| `500 Server Error`      | Internal server error during link resolution or file processing.       |

Use the **Search Spreadsheet Broken Links** API endpoint to identify broken hyperlinks, invalid external references, and malformed formulas in Excel workbooks. The operation runs server-side in the cloud—no local processing or cloud storage required. Results are returned in a structured JSON format for integration into CI/CD pipelines, audit tools, or compliance workflows.

### Request Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1&cellArea=B2:D10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@sample.xlsx"
```

### Use Cases

- **Financial Model Auditing**: Before releasing monthly/quarterly reports, scan key dashboard ranges (e.g., `Dashboard!B5:K50`) to verify all external data references remain valid.
- **M&A Due Diligence**: After consolidating business-unit spreadsheets, run a quality check on the “Overview” worksheet to catch broken cross-file links caused by renamed paths or permissions.
- **Investor Package Validation**: Ensure charts, tables, and executive summaries referencing external market data sources (e.g., Bloomberg, Yahoo Finance) resolve correctly before distribution.

### Implementation Guidance

#### SDK Support

Aspose.Cells Cloud provides SDKs for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go. Using an SDK simplifies authentication, request formatting, and response parsing.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{< /tab >}}
{{< /tabs >}}

#### OpenAPI Specification

The endpoint is defined in the public [OpenAPI spec](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks). Use this to generate client libraries or integrate with API-gateway tools.