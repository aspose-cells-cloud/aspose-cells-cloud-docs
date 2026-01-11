---
title: "Aspose.Cells Cloud Excel Text Search Web API - Find Text in Remote Spreadsheet Worksheet"
second_title: "Document"
ArticleTitle: "Search Text in Remote Excel Spreadsheet Worksheet - Find Data in Specific"
linktitle: "Search Remote Worksheet Content"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Excel search API, text search API, find in spreadsheet API, range search API, Aspose Cells search API, remote Excel search, cloud spreadsheet search API, text lookup API, Excel data discovery API, workbook search API, API text finder"
description: "Easily search for specific text within any remote Excel spreadsheet worksheet stored in cloud storage. Find data, formulas, or text across entire workbooks or specific cell ranges. Cloud-based search tool for quick data discovery without downloading files."
weight: 100
---

Programmatically search for specific text within any Excel spreadsheet worksheet using Aspose.Cells Cloud API. Find text, numbers, or formulas in remote files stored in cloud storage. RESTful API for automated data discovery, content analysis, and spreadsheet auditing workflows.

## **Search Content in Remote Worksheet**

### API Endpoint

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| name | String | Path | **Required**. The filename of the target Excel workbook (e.g., `annual_report.xlsx`) stored in cloud storage. |
| worksheet | String | Path | **Required**. The specific worksheet name within the workbook where the search will be performed. |
| searchText | String | Query | **Required**. The exact text string or number to find within the specified worksheet. |
| ignoringCase | Boolean | Query | **Optional**. When set to `true`, performs a case-insensitive search (e.g., "Data" matches "data"). Defaults to `false`. |
| folder | String | Query | **Optional**. The directory path in cloud storage containing the workbook file. If omitted, searches in the root directory. |
| storageName | String | Query | **Optional**. The name of a custom-configured cloud storage service. If not provided, the account's default storage is used. |
| region | String | Query | **Optional**. The locale setting (e.g., `ja-JP`) to apply, which may influence text comparison and collation rules. |
| password | String | Query | **Optional**. The password required to decrypt a password-protected spreadsheet. Omit if the file is not encrypted. |

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

## Where should we use the Search content within the worksheet of the Spreadsheet API?

- **Comprehensive Workbook Compliance Audit**: Quickly scan the entire Excel file to identify all sensitive terms (such as "Confidential Clause", "Internal Data"), which is used for enterprise data security and compliance checks.
- **Cross-Sheet Data Association Query**: When project information is scattered across multiple worksheets, simply search for a specific project number or customer name, and immediately locate all related data to achieve cross-sheet information integration.
- **Batch Template Content Verification**: After automated report generation, scan multiple Excel files in batches to confirm that all preset placeholders (such as `{{Date}}`) have been correctly replaced, ensuring the completeness and accuracy of the report.
- **Historical Data Archiving and Mining**: Analyze historical data files exported from the old system, search for specific event codes or business terms, quickly understand the historical business logic, and conduct data archaeology and analysis.

## Why should you use the Search content within the worksheet of the Spreadsheet API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in universally accessible PDF format.

## How to Use the Search for broken links within the worksheet of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search content within worksheet of spreadsheets for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
