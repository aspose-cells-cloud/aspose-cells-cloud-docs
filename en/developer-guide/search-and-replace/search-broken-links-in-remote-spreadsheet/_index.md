---  
title: "Aspose.Cells Cloud – Excel Broken Links Detection API – Scan & Validate Spreadsheet Links in Remote Workbooks"  
second_title: "Document"  
ArticleTitle: "Find & Fix Broken Links in Remote Excel – Cloud Spreadsheet Link Checker"  
linktitle: "Search Remote Spreadsheets Broken Links"  
type: docs  
url: /search-broken-links-in-remote-spreadsheet/  
keywords: "Excel, broken links, API, cloud, spreadsheet, validation, Aspose.Cells"  
description: "Use Aspose.Cells Cloud API to scan remote Excel workbooks for broken external links, invalid formulas, and missing data sources."  
weight: 100  
---  

Automatically detect broken links in Excel files stored in cloud storage. Our API scans specified ranges for broken external references, invalid formulas, and missing data sources. It supports remote spreadsheet auditing, automated quality checks, and integration with cloud‑storage providers. Use the RESTful API to automate enterprise‑level workflow automation.  

## **Search Broken Links In Remote Spreadsheet API**  

### API Endpoint  

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```  

**Authentication** – Before calling the endpoint, obtain an OAuth 2.0 access token using your Aspose Cloud client‑id and client‑secret (`POST https://api.aspose.cloud/connect/token`). Include the token in the `Authorization: Bearer <token>` header of every request.  

### **Request Parameters:**  

| Parameter Name | Type   | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| name | String | Path | **Required.** The name of the Excel workbook file to be scanned for broken links (e.g., `Quarterly_Report.xlsx`). |
| worksheet | String | Query | **Required.** The name of the worksheet where the search operation will be performed. Specify the exact sheet name as it appears in the workbook. |
| cellArea | String | Query | **Required.** The cell range to be analyzed for broken links, expressed in A1 notation (e.g., `C5:J50`). The API searches only within this area. |
| folder | String | Query | **Optional.** The path to the directory containing the workbook in your cloud storage. If omitted, the root directory is assumed. |
| storageName | String | Query | **Optional.** The name of your custom cloud‑storage configuration. If omitted, the system’s default storage is used. |
| region | String | Query | **Optional.** Locale setting applied during processing (e.g., `en-US`). It can affect the interpretation of region‑specific formula syntax or references. |
| password | String | Query | **Optional.** Password required to open an encrypted spreadsheet. Omit if the file is not password‑protected. |

### **Response**  

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```  

### Error Codes  

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Invalid access token, client ID, or client secret.  
- **404 Not Found** – The spreadsheet file is not accessible.  
- **500 Server Error** – An anomaly occurred while obtaining calculation data.  

## Where should we use the Search for broken links within the Spreadsheet API?  

- **Regular audit of large financial models** – Before releasing monthly or quarterly reports, automatically scan key calculation areas (e.g., `Dashboard!B5:K50`) that contain many external data references to ensure all links point to valid source files.  
- **Data integration for mergers and acquisitions** – When merging multiple spreadsheets representing business units, scan the “Overview” worksheet after integration to identify links that have become invalid due to changed file paths or permission issues.  
- **Preparation of investor data packages** – Before finalising presentation materials that contain charts and tables linked to external databases or market‑data sources, verify the validity of all links.  

## Why should you use the Search for broken links within the Spreadsheet API?  

- **Developer‑friendly** – Aspose.Cells Cloud provides SDK libraries in multiple languages, enabling rapid development with comprehensive documentation. Compared with building a custom solution, this significantly reduces development effort.  
- **Reduced labor costs** – Automates link validation, eliminating the need for dedicated staff to manually consolidate documents.  
- **Pay‑per‑use** – No upfront investment; you only pay for the API calls you actually use.  
- **Zero maintenance costs** – No servers to maintain, no software updates, and no compatibility concerns.  

## How to Use the Search for broken links within the Spreadsheet API with SDKs  

### OpenAPI Specification  

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchController/SearchBrokenLinksInRemoteSpreadsheet) defines a publicly accessible programming interface and allows you to perform REST interactions directly from a web browser.  

### Use Aspose.Cells Cloud SDKs  

Using an SDK is the most efficient way to accelerate development. The SDK abstracts the underlying HTTP details, allowing you to implement broken‑link detection with minimal code. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.  

The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:  

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}  