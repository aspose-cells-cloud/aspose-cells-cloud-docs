---  
title: "Search Spreadsheet Content – Aspose.Cells Cloud API (Find Text in Excel)"  
second_title: "Document"  
ArticleTitle: "Search Text in Local Excel Spreadsheets – Find Specific Data"  
linktitle: "Search Spreadsheet Content"  
type: docs  
url: /search-spreadsheet-content/  
keywords: "Aspose.Cells, Excel search API, spreadsheet content search, cloud spreadsheet API, text lookup"  
description: "Use Aspose.Cells Cloud API to search for text, numbers, or formulas in local Excel files. Supports case‑insensitive queries, worksheet‑level scope, and secure authentication."  
weight: 100  
---  

Programmatically search for specific text within any Excel spreadsheet using the Aspose.Cells Cloud API. The API can locate text, numbers, or formulas in local files stored in the cloud, enabling automated data discovery, content analysis, and spreadsheet‑auditing workflows.  

## **Search Spreadsheet Content API**  

### API Endpoint  

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```  

**Authentication** – The API requires an OAuth 2.0 access token. Include the token in the request header:  

```
Authorization: Bearer <access‑token>
```  

Obtain the token by sending a POST request to `https://api.aspose.cloud/connect/token` with your `client_id` and `client_secret`.  

### **Request Parameters**  

| Parameter      | Type    | Location   | Description                                                                 |
|----------------|---------|------------|-----------------------------------------------------------------------------|
| spreadsheet    | File    | FormData   | The Excel file to be searched.                                              |
| searchText     | String  | Query      | The text (or numeric value) to locate in the workbook.                     |
| ignoringCase   | Boolean | Query      | Set to `true` to perform a case‑insensitive search.                        |
| worksheet      | String  | Query      | Name of the worksheet to limit the search. If omitted, all worksheets are scanned. |
| cellArea       | String  | Query      | A‑1 style range (e.g., `A1:C10`) that restricts the search area.           |
| region         | String  | Query      | Geographic region of the service (e.g., `us-east-1`).                       |
| password       | String  | Query      | Password required to open a protected workbook.                            |

#### Sample cURL request  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer <access-token>" \
     -F "spreadsheet=@/path/to/Workbook.xlsx"
```  

### **Response**  

The API returns a `SearchResult` object that contains an array of matched cells. Each element provides the worksheet name, cell address, and the matched text.

```json
{
  "Code": 0,
  "Status": "OK",
  "Cells": [
    {
      "Worksheet": "Sheet1",
      "CellName": "B4",
      "Text": "Invoice"
    },
    {
      "Worksheet": "Sheet2",
      "CellName": "A12",
      "Text": "Invoice"
    }
  ]
}
```  

If no matches are found, `Cells` is an empty array while `Code` remains `0`.  

### Error Codes  

- **400 Bad Request** – The request URI or parameters are invalid.  
- **401 Unauthorized** – Missing or invalid access token, or incorrect client credentials.  
- **404 Not Found** – The specified spreadsheet cannot be accessed.  
- **500 Internal Server Error** – An unexpected server error occurred while processing the workbook.  

## Where should we use the Search content within the Spreadsheet API?  

- **Comprehensive Workbook Compliance Audit** – Scan the entire workbook to locate sensitive terms (e.g., “Confidential Clause”, “Internal Data”) for data‑security and compliance checks.  
- **Cross‑Sheet Data Association Query** – Find a project number or customer name that appears on multiple worksheets, enabling rapid cross‑sheet integration.  
- **Batch Template Content Verification** – After generating reports, verify that all placeholders such as `{{Date}}` have been correctly replaced across a batch of Excel files.  
- **Historical Data Archiving and Mining** – Search legacy Excel files for specific event codes or business terms to accelerate data archaeology and analysis.  

## Why should you use the Search content within the Spreadsheet API?  

- **Developer‑Friendly** – SDKs are available for many languages, reducing development effort compared with building a custom solution.  
- **Reduced Labor Costs** – Automates tasks that would otherwise require manual inspection of spreadsheets.  
- **Pay‑per‑Use** – You only pay for the API calls you actually make.  
- **Zero Maintenance** – No servers to manage, no software updates, and no compatibility concerns.  
- **Preserves Complex Formatting** – Results can be exported to PDF while retaining the original Excel layout.  

## How to Use the Search for broken links within the Spreadsheet API with SDKs  

### OpenAPI Specification  

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.  

### Use Aspose.Cells Cloud SDKs  

Using an SDK is the fastest way to integrate the search functionality. The SDK abstracts the HTTP layer, allowing you to call the API with minimal code. See the full list of SDKs in the [GitHub repository](https://github.com/aspose-cells-cloud).  

The following code examples demonstrate how to invoke the Search Spreadsheet Content operation with various SDKs:

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
{{< /tabs >}}