---
title: "Search Spreadsheet Broken Links – Aspose.Cells Cloud API"
second_title: "Document"
ArticleTitle: "Find & Fix Broken Links in Excel – Cloud Spreadsheet Link Checker"
linktitle: "Search Spreadsheet Broken Links"
type: docs
url: /search-spreadsheet-broken-links/
keywords: "Aspose Cells API, broken links detection, spreadsheet link validation, Excel API, cloud spreadsheet audit"
description: "Detect and fix broken links in Excel workbooks via Aspose.Cells Cloud API. Scan ranges, get detailed JSON results, and integrate with any language SDK."
weight: 100
---

Automatically detect broken links in Excel files. Our API scans specified ranges for broken external references, invalid formulas, and missing data sources. Supports remote spreadsheet auditing, automated quality checks, and integration with cloud storage providers. RESTful API for enterprise workflow automation.

**Summary:** Use this endpoint to quickly identify and repair invalid links in workbooks, ensuring data integrity across financial models, M&A data sets, and investor‑ready packages.

**Prerequisites:**  
- Aspose.Cells Cloud SDK v4.0 or later (or direct REST calls).  
- A valid OAuth 2.0 access token (see the *Authentication* section).  
- Sufficient storage quota (maximum workbook size 150 MB).  

## **Search Spreadsheet Broken Links API**

### API Endpoint

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

### Authentication

Obtain an OAuth 2.0 token from the token endpoint:

```bash
POST https://api.aspose.cloud/connect/token \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

Include the token in the request header:

```
Authorization: Bearer <access_token>
```

### Request Parameters

| Parameter Name | Type   | Location                | Description |
|----------------|--------|-------------------------|-------------|
| Spreadsheet    | File   | FormData (multipart)    | **Required.** The Excel workbook file (`.xlsx`, `.xls`, etc.) to be analyzed. |
| worksheet      | String | Query                   | **Optional.** The name of the worksheet to analyse. If omitted, the first worksheet is used. |
| cellArea       | String | Query                   | **Optional.** Target cell range in A1 notation (e.g., `B2:D10`). If not specified, the entire used range is analysed. |
| region         | String | Query                   | **Optional.** Locale setting (e.g., `en‑GB`) that may affect date, number, or currency interpretation. |
| password       | String | Query                   | **Optional.** Password for encrypted workbooks. Leave empty if the file is not protected. |

#### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1&cellArea=B2:D10" \
     -H "Authorization: Bearer <access_token>" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Response

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
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Not Found",
      "Status": "Broken"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid access token, client ID, or client secret.  
- **404 Not Found** – The spreadsheet file is not accessible.  
- **429 Too Many Requests** – Rate limit exceeded (60 calls / minute).  
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.  

### Limits & Throttling

- Maximum workbook size: **150 MB**.  
- Rate limit: **60 requests per minute** per account.  
- If you receive a `429` response, wait at least one minute before retrying.

## Where should we use the Search broken links within the Spreadsheet API?

- **Regular Audit of Large Financial Models**: Before releasing monthly or quarterly reports, automatically scan key calculation areas (e.g., `Dashboard!B5:K50`) that contain many external data references to ensure all links point to valid source files.  
- **Data Integration for Mergers and Acquisitions**: When merging multiple spreadsheet files representing business units, scan the “Overview” worksheet after integration to identify links that have become invalid due to changed file paths or permission issues.  
- **Preparation of Investor Data Packages**: Before finalizing presentation materials that contain charts and tables linked to external databases or market data sources, verify the validity of all links.  

## Why should you use the Search broken links within the Spreadsheet API?

- **Developer‑Friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.  
- **Reduced Labor Costs** – Eliminates the need for dedicated staff to manually verify document links.  
- **Pay‑per‑Use** – No upfront investment; you only pay for the API calls you actually use.  
- **Zero Maintenance Costs** – No servers to maintain, no software updates, and no compatibility issues.  
- **Preserves Complex Excel Formatting** – Results are returned in a universally accessible JSON format while retaining the original workbook’s layout.  

## How to Use the Search for broken links within the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks) defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search‑broken‑links functionality with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}

**Next Steps**

1. Generate an OAuth 2.0 token.  
2. Upload the workbook using the `PUT /cells/search/broken-links` endpoint (or the SDK equivalent).  
3. Parse the `BrokenLinks` array in the JSON response to locate and repair invalid references.  