---
title: "Aspose.Cells Cloud Excel Text Search Web API – Find Text in Remote Spreadsheet Ranges"
second_title: "Document"
ArticleTitle: "Search Text in Remote Excel Spreadsheets – Find Data in Specific Ranges"
linktitle: "Search Remote Range Content"
type: docs
url: /search-content-in-remote-range/
keywords: "Aspose.Cells, Excel search API, remote range, cloud spreadsheet, text lookup"
description: "Search for text, numbers, or formulas in a specific range of an Excel workbook stored in Aspose Cloud."
weight: 100
---

## **Search Content In Remote Range**I

Programmatically search for specific text within any range of Excel spreadsheets using Aspose.Cells Cloud API. Find text, numbers, or formulas in remote files stored in cloud storage. RESTful API for automated data discovery, content analysis, and spreadsheet‑auditing workflows.

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### Request Parameters

| Parameter Name | Type    | Path/Query/String/HTTPBody | Description                                                                                                                                         |
| :------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Path                       | **Required**. The filename (including extension) of the Excel workbook to search, e.g., `customer_data.xlsx`.                                       |
| worksheet      | String  | Path                       | **Required**. The exact name of the worksheet within the workbook to search in, e.g., `Orders_2024`.                                                |
| cellArea       | String  | Path                       | **Required**. The target cell range for the search, specified in A1 notation (e.g., `B2:H100`). The search is confined to this area.                |
| searchText     | String  | Query                      | **Required**. The specific text string, number, or partial content to find within the defined cell area.                                            |
| ignoreCase     | Boolean | Query                      | **Optional**. When set to `true`, the search ignores case differences (e.g., “Report” matches “report”). Default is `false` (case‑sensitive).       |
| folder         | String  | Query                      | **Optional**. The directory path in your cloud storage where the workbook is located. If omitted, the root directory is used.                       |
| storageName    | String  | Query                      | **Optional**. The identifier for a custom cloud storage configuration. If not specified, the default storage for the account is used.               |
| region         | String  | Query                      | **Optional**. The culture/region setting (e.g., `en‑AU`) that may affect interpretation of region‑specific characters or formats during the search. |
| password       | String  | Query                      | **Optional**. The password to decrypt and access a password‑protected spreadsheet file. Omit if the file is not encrypted.                          |

### Response (Schema)

```json
{
  "Found": "Boolean – Indicates whether the search text was found.",
  "CellAddresses": [
    "String[] – List of cell addresses (A1 notation) where matches were located."
  ],
  "Occurrences": "Integer – Total number of matches found."
}
```

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid access token, client ID, or client secret.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – An unexpected condition prevented the server from fulfilling the request.

## Where should we use the Search content within the range of the Spreadsheet API?

- **Large‑scale Data Quality Check** – During the acceptance stage of the data‑warehouse ETL process, search for missing field descriptions, undefined abbreviations, or placeholder text (e.g., `"TBD"` or `"NULL"`) in the data‑mapping table (`DataDictionary!B2:F1000`) to identify incomplete data definitions.
- **Dynamic Report Generation and Content Extraction** – In automated reporting systems, intelligently search and extract current‑period data blocks marked with specific identifiers (e.g., `"[KPI]"`) from template worksheets containing mixed data (`Monthly_Metrics!C10:G50`) for assembling the final report.
- **Contract and Legal Document Analysis** – When reviewing spreadsheet appendices that contain many clauses, efficiently locate specific legal terms (e.g., `"liability limit"`), party names, or dates within a defined range (`Contract_Terms!A:A`) to accelerate the review process.

## Why should you use the Search content within the range of the Spreadsheet API?

- **Developer‑friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comprehensive documentation, which significantly reduces the development workload compared with building custom solutions.
- **Reduced labor costs** – Eliminates the need for dedicated positions handling document consolidation.
- **Pay‑per‑use** – No upfront investment; you only pay for the API calls actually used.
- **Zero maintenance costs** – No servers to maintain, no software updates, and no compatibility concerns.

## How to Use the Search Content within the range of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteRange) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search content within a range of spreadsheets for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
