---
title: "Aspose.Cells Cloud – Excel Broken Links Detection API – Scan & Validate Spreadsheet Links in Remote Worksheets"
second_title: "Document"
ArticleTitle: "Find & Fix Broken Links in Remote Excel Worksheet – Cloud Spreadsheet Link Checker"
linktitle: "Search Remote Worksheet Broken Links"
type: docs
url: /search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, broken links, Excel API, cloud spreadsheet, link validation"
description: "Detect and fix broken external links in Excel worksheets stored in cloud storage. Use the Aspose.Cells Cloud API to scan ranges, return link details, and automate quality checks."
weight: 100
---

## **Search Broken Links in Remote Worksheet API**

Automatically detect broken links in an Excel worksheet stored in cloud storage. Our API scans specified ranges to locate broken external references, invalid formulas, and missing data sources. Supports remote spreadsheet auditing, automated quality checks, and integration with cloud‑storage providers. RESTful API for enterprise workflow automation.

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                                                                                                                                                                                                |
| :------------- | :----- | :-------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | **Required.** The filename (with extension) of the Excel workbook to search for broken links (e.g., `Annual_Report.xlsx`).                                                                                                                 |
| worksheet      | String | Path                        | **Required.** The exact name of the worksheet where the link scanning will be performed (e.g., `DataSheet1`).                                                                                                                              |
| folder         | String | Query                       | **Optional.** The directory path within your cloud storage where the target workbook is located. If omitted, the root folder is used.                                                                                                      |
| storageName    | String | Query                       | **Optional.** The identifier of your custom‑configured cloud storage. If not provided, the API uses the account’s default storage.                                                                                                         |
| region         | String | Query                       | **Optional.** The locale setting to apply during the search (e.g., `fr-FR`). This may influence the interpretation of certain formulas or regional data formats. _Supported locale codes include `en-US`, `fr-FR`, `de-DE`, `es-ES`, etc._ |
| password       | String | Query                       | **Optional.** The decryption password for a password‑protected spreadsheet. Omit if the file is not encrypted.                                                                                                                             |

### **Response**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Source file not found"
    }
  ]
}
```

The response object is of type **BrokenLinksResponse** and contains:

- **BrokenLinks** – a collection of `BrokenLink` items, each describing the problematic reference (address, error code, and message).
- **Code** – numeric status code returned by the service.
- **Status** – textual description of the result.

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid or missing access token.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – An anomaly occurred while obtaining calculation data.

## Where should we use the Search for broken links within the worksheet of Spreadsheet API?

- **Regular Audit of Large Financial Models**: Before releasing monthly or quarterly reports, automatically scan the key calculation areas (such as `Dashboard!B5:K50`) that contain a large amount of external data references to ensure that all links point to valid source files.
- **Data Integration for Mergers and Acquisitions**: When merging multiple spreadsheet files representing business units, scan the "Overview" worksheet after the integration process to identify links that have become invalid due to changes in source file paths or permission issues.
- **Preparation of Investor Data Packages**: Before finalizing the presentation materials that contain charts and tables linked to external databases or market data sources, verify the validity of all links.

## Why should you use the Search for broken links within the worksheet of Spreadsheet API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces the development workload.
- **Reduces Labor Costs**: Cuts the need for personnel dedicated to manual document consolidation and link verification.
- **Pay‑per‑Use**: No upfront investment; you only pay for the API calls you actually use.
- **Zero Maintenance Costs**: No servers to maintain, no software updates, and no compatibility issues to manage.
- **Preserves Complex Excel Formatting** in universally accessible PDF format.

## How to Use the Search for broken links within the worksheet of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinksInRemoteWorksheet) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search‑broken‑links within worksheets of spreadsheets with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}
