---
title: "Aspose.Cells Cloud Excel Text Search Web API - Find Text in Remote Spreadsheet"
second_title: "Document"
ArticleTitle: "Search Text in Remote Excel Spreadsheets - Find Data in Specific"
linktitle: "Search Remote Spreadsheet Content"
type: docs
url: /search-content-in-remote-spreadsheet/
keywords: "Excel search API, text search API, find in spreadsheet API, range search API, Aspose Cells search API, remote Excel search, cloud spreadsheet search API, text lookup API, Excel data discovery API, workbook search API, API text finder"
description: "Easily search for specific text within any remote Excel spreadsheets stored in cloud storage. Find data, formulas, or text across entire workbooks or specific cell ranges. Cloud-based search tool for quick data discovery without downloading files."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Match all blank cells in an Excel worksheet, remote spreadsheet search, cloud storage search
---

Programmatically search for specific text within any Excel spreadsheets using Aspose.Cells Cloud API. Find text, numbers, or formulas in files stored in cloud storage. RESTful API for automated data discovery, content analysis, and spreadsheet auditing workflows.


### **Search Content in Remote Spreadsheet API**

### API Endpoint

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| name | String | Path | **Required**. The filename of the Excel workbook (including extension) where the text search will be performed, e.g., `sales_data.xlsx`. |
| searchText | String | Query | **Required**. The exact string, number, or partial content to locate across the entire workbook or worksheet(s). |
| ignoringCase | Boolean | Query | **Optional**. Determines search case-sensitivity. Set to `true` for case-insensitive matching (e.g., "Report" matches "REPORT"); default is typically `false`. |
| folder | String | Query | **Optional**. The directory path within your cloud storage that contains the target workbook. If omitted, the root folder is assumed. |
| storageName | String | Query | **Optional**. The name identifier for a custom-configured cloud storage service. If not specified, the API uses the default storage associated with the account. |
| region | String | Query | **Optional**. The locale setting (e.g., `es-ES`) to apply during the search, which may affect text normalization or collation rules. |
| password | String | Query | **Optional**. The decryption password required to access a password-protected Excel file. Omit this parameter if the file is not encrypted. |

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

## Where should we use the Search content within the Spreadsheet API?

- **Comprehensive Workbook Compliance Audit**: Quickly scan the entire Excel file to identify all sensitive terms (such as "Confidential Clause", "Internal Data"), which is used for enterprise data security and compliance checks.
- **Cross-Sheet Data Association Query**: When project information is scattered across multiple worksheets, simply search for a specific project number or customer name, and immediately locate all related data to achieve cross-sheet information integration.
- **Batch Template Content Verification**: After automated report generation, scan multiple Excel files in batches to confirm that all preset placeholders (such as `{{Date}}`) have been correctly replaced, ensuring the completeness and accuracy of the report.
- **Historical Data Archiving and Mining**: Analyze historical data files exported from the old system, search for specific event codes or business terms, quickly understand the historical business logic, and conduct data archaeology and analysis.

## Why should you use the Search content within the Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Search for broken links within the range of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteSpreadsheet) defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search content within spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
