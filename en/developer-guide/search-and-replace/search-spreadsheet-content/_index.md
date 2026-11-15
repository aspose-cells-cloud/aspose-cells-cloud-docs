---
url: /search-spreadsheet-content/
title: "Search Spreadsheet Content – Aspose.Cells Cloud API"
linktitle: "Search Spreadsheet Content"
type: docs
keywords: "Excel search API, spreadsheet content search, text lookup in Excel, cloud spreadsheet API, find text in Excel"
description: "Use Aspose.Cells Cloud API to search Excel files for text, numbers, or formulas locally—no cloud storage needed."
weight: 100
ArticleTitle: "Search Excel Content with Aspose.Cells Cloud API – Text, Range & Worksheet Search"
---

The **SearchSpreadsheetContent** API (`PUT https://api.aspose.cloud/v4.0/cells/search/content`) in Aspose.Cells Cloud enables developers to programmatically search for specified text within a local Excel spreadsheet uploaded via the request body, returning matched cell locations—including worksheet name, cell address, and matched text—without requiring prior storage in the cloud; the operation supports refining results with options like case-insensitive matching, worksheet or cell-area scoping, and password-protected file handling.

---

## The Search Spreadsheet Content Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                                                                                             |
| -------------- | ------- | -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File    | FormData                   | Upload spreadsheet file.                                                                                                                |
| searchText     | String  | Query                      | The searched text.                                                                                                                      |
| ignoringCase   | Boolean | Query                      | Ignore the text of the search.                                                                                                          |
| worksheet      | String  | Query                      | Specify the worksheet for the lookup.                                                                                                   |
| cellArea       | String  | Query                      | Specify the cell area for the lookup                                                                                                    |
| region         | String  | Query                      | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String  | Query                      | The password for opening spreadsheet file.                                                                                              |

---

### Response

```json
[
  {
    "Name": "SearchResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "SearchResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

The API returns a `SearchResponse` object containing an array of matched items.

**HTTP Status Codes**

| Code | Meaning           | Description                                                   |
| ---- | ----------------- | ------------------------------------------------------------- |
| 200  | OK                | The request completed successfully.                           |
| 400  | Bad Request       | Invalid url.                                                  |
| 401  | Unauthorized      | Authentication has failed, or no credentials were provided.   |
| 404  | Not Found         | Source file not accessible.                                   |
| 413  | Payload Too Large | The uploaded file exceeds the allowed size limit.             |
| 500  | Server Error      | The spreadsheet has encountered an anomaly in obtaining data. |

### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

> **Note:** Authentication requires a valid JWT token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

---

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

## Use Cases

### Compliance & Security Audits

Scan workbooks for sensitive terms (e.g., `"Confidential"`, `"PII"`, `"Internal"`) to support data governance and regulatory compliance.

### Cross-Sheet Data Discovery

Find identifiers (e.g., project numbers, customer IDs) across multiple worksheets to map data relationships.

### Template Verification

Validate that placeholders like `{{Date}}` or `{{User}}` are fully replaced after batch report generation.

### Legacy Data Mining

Search historical Excel files for event codes, transaction types, or business terms to accelerate archival analysis.

## How to Use the Search Spreadsheet Broken Links API with SDKs?

### Search Spreadsheet Content API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchSpreadsheetContent" rel="noopener noreferrer">Search Spreadsheet Content API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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
