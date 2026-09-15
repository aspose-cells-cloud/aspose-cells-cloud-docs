---
url: /search-spreadsheet-broken-links/
title: "Search Spreadsheet Broken Links – Aspose.Cells Cloud API"
second_title: "Reference"
ArticleTitle: "Find & Fix Broken Links in Excel – Cloud Spreadsheet Link Checker"
linktitle: "Search Broken Links"
keywords: "Excel link checker, broken reference detector, cloud spreadsheet audit, Aspose.Cells Cloud API, external reference validation"
description: "Use Aspose.Cells Cloud API to programmatically detect broken Excel links—including external references, formulas, and data sources—in workbooks. Get structured JSON results for automated quality assurance in financial modeling, M&A due diligence, and investor reporting."
date: 2023-11-15T10:00:00Z
lastmod: 2024-05-20T14:30:00Z
canonicalURL: /search-spreadsheet-broken-links/
type: docs
weight: 100
---

## Detect Broken Links in Excel Workbooks

Use the **Search Spreadsheet Broken Links** API endpoint to identify broken hyperlinks, invalid external references, and malformed formulas in Excel workbooks. The operation runs server-side in the cloud—no local processing or cloud storage required. Results are returned in a structured JSON format for integration into CI/CD pipelines, audit tools, or compliance workflows.

### API Endpoint

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

### Request Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1&cellArea=B2:D10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@sample.xlsx"
```

### Request Parameters

| Parameter | Type   | Location   | Required | Description |
|-----------|--------|------------|----------|-------------|
| `Spreadsheet` | File | FormData (multipart) | Yes | Excel workbook (`.xlsx`, `.xls`, `.xlsb`, `.xlsm`, `.ods`, etc.) to analyze. |
| `worksheet` | String | Query | No | Name of the worksheet to scan. Defaults to the first visible sheet. |
| `cellArea` | String | Query | No | Target cell range in A1 notation (e.g., `B2:D10`). If omitted, the used range is scanned. |
| `region` | String | Query | No | Locale identifier (e.g., `en-US`, `fr-FR`). Affects date/number parsing and formula interpretation. |
| `password` | String | Query | No | Password for encrypted workbooks. Omit if the file is unprotected. |

### Authentication

All requests require a valid [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include the token in the `Authorization` header as a Bearer token:

```http
Authorization: Bearer {access_token}
```

### Response Structure

A successful response returns a `BrokenLinksResponse` object:

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "File not found",
      "Status": "Broken"
    },
    {
      "CellName": "C12",
      "Link": "https://httpstat.us/404",
      "ErrorMessage": "404 Not Found",
      "Status": "Broken"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

#### BrokenLink Object

| Field | Type | Description |
|-------|------|-------------|
| `CellName` | String | Cell address (e.g., `B5`) containing the broken link. |
| `Link` | String | Original URL or file path referenced in the cell. |
| `ErrorMessage` | String | Human-readable error (e.g., `"File not found"`, `"404 Not Found"`). |
| `Status` | String | Always `"Broken"` for entries in the `BrokenLinks` array. |

### Error Codes

| Code | Description |
|------|-------------|
| `400 Bad Request` | Invalid request URI, malformed parameters, or unsupported file format. |
| `401 Unauthorized` | Missing, expired, or invalid access token or credentials. |
| `404 Not Found` | Specified file not accessible or upload failed. |
| `429 Too Many Requests` | Rate limit exceeded (60 calls/minute). |
| `500 Server Error` | Internal server error during link resolution or file processing. |

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

### Best Practices

- **Use `cellArea` to limit scope**: Scanning a large workbook can increase latency. Specify only the ranges under audit.  
- **Validate with `region`**: If your workbook uses locale-specific date/number formats, set the `region` parameter to avoid false positives (e.g., `en-GB` for `dd/mm/yyyy` vs `en-US` for `mm/dd/yyyy`).  
- **Handle encrypted files securely**: Pass the `password` parameter only over HTTPS. Avoid hardcoding credentials in scripts.  
- **Automate cleanup**: Feed `BrokenLinks` results into a script that attempts to refresh links or flag cells for manual review.

### Related Documentation

- [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Cloud Storage Integration](/cells/cloud/storage-integration/)  
- [SDK Installation Guide](/cells/sdk-overview/)