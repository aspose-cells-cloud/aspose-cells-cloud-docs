---
title: "Aspose.Cells Cloud Excel Broken Links Detection Web API -  Scan & Validate Spreadsheet Links in Remote Spreadsheet"
second_title: "Document"
ArticleTitle: "Find & Fix Broken Links in Remote Excel - Cloud Spreadsheet Link Checker"
linktitle: "Search Remote Spreadsheets Broken Links"
type: docs
url: /search-broken-links-in-remote-spreadsheet/
keywords: "Excel broken links API, spreadsheet link validation API, cloud Excel audit API, remote link checker API, Aspose Cells REST API, Excel error detection API, external reference scanner, workbook validation API, formula error detection, cloud storage scanning API, automated spreadsheet QA"
description: "Efficiently find and fix broken links in Excel files stored in cloud storage. Scan specified ranges for invalid external references, broken formulas, and missing data sources. Cloud-based tool for auditing and repairing spreadsheet links without downloading files. Perfect for large workbooks and remote collaboration."
weight: 100
---

Automatically detect broken links in Excel files stored in cloud storage. Our API scans specified ranges for broken external references, invalid formulas, and missing data sources. Supports remote spreadsheet auditing, automated quality checks, and integration with cloud storage providers. RESTful API for enterprise workflow automation.

## **Search Broken Links In Remote Spreadsheet API**

### API Endpoint

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| name | String | Path | **Required**. The name of the Excel workbook file to be scanned for broken links. Include the file extension (e.g., `Quarterly_Report.xlsx`). |
| worksheet | String | Query | **Required**. The name of the target worksheet where the search operation will be performed. Specify the exact sheet name as it appears in the workbook. |
| cellArea | String | Query | **Required**. The cell range to be analyzed for broken links, specified in A1 notation (e.g., `C5:J50`). The API will search within this defined area only. |
| folder | String | Query | **Optional**. The path to the directory containing the workbook within your cloud storage. If not provided, the root directory is assumed. |
| storageName | String | Query | **Optional**. The name of your custom cloud storage configuration. If omitted, the system's default storage will be used for the operation. |
| region | String | Query | **Optional**. The locale setting to apply during processing (e.g., `en-US`). This can affect the interpretation of region-specific formula syntax or references. |
| password | String | Query | **Optional**. The password required to open an encrypted spreadsheet file. Omit this parameter if the file is not password-protected. |

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
          "Reference": "BrokenLink",
        },
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Search for broken links within the Spreadsheet API?

- **Regular Audit of Large Financial Models**: Before releasing monthly or quarterly reports, automatically scan the key calculation areas (such as `Dashboard!B5:K50`) that contain a large amount of external data references to ensure that all links point to valid source files.
- **Data Integration for Mergers and Acquisitions**: When merging multiple spreadsheet files representing business units, scan the "Overview" worksheet after the integration process to identify links that have become invalid due to changes in source file paths or permission issues.
- **Preparation of Investor Data Packages**: Before finalizing the presentation materials that contain charts and tables linked to external databases or market data sources, verify the validity of all links.

## Why should you use the Search for broken links within the Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Search for broken links within the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchController/SearchBrokenLinksInRemoteSpreadsheet) defines a publicly accessible programming interface and allows you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search broken within spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
