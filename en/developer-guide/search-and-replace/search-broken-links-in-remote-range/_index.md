---
title: "Aspose.Cells Cloud – Detect Broken Links in Excel Range (API)"
second_title: "Document"
ArticleTitle: "Find & Fix Broken Links in Remote Excel Range – Cloud Spreadsheet Link Checker"
linktitle: "Search Remote Range Broken Links"
type: docs
url: /search-broken-links-in-remote-range/
keywords: "Aspose Cells, broken links API, Excel range validation, cloud spreadsheet, external reference checker"
description: "Use Aspose.Cells Cloud API to scan a specific Excel range for broken external links, invalid formulas, or missing data sources. Secure, fast, and cloud‑based."
weight: 100
---

## **Search Broken Links in Remote Range API**

Automatically detect broken links in the range data of Excel files stored in cloud storage. Our API scans specified ranges for broken external references, invalid formulas, and missing data sources. Supports remote spreadsheet auditing, automated quality checks, and integration with cloud storage providers. RESTful API for enterprise workflow automation.

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### Request Parameters

| Parameter Name | Type   | Location | Description                                                                                                                                                          |
| -------------- | ------ | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path     | **Required.** The name of the Excel workbook file (e.g., `financial_report.xlsx`) stored in cloud storage that you want to scan for broken links.                    |
| worksheet      | String | Path     | **Required.** The name of the specific worksheet (e.g., `Sheet1`, `Q4_Data`) within the workbook where the search for broken links should be performed.              |
| cellArea       | String | Path     | **Required.** The target cell range address (e.g., `A1:F100`) within the specified worksheet to be scanned for broken external references, formulas, or links.       |
| folder         | String | Query    | **Optional.** The directory path in your cloud storage where the target workbook is located. If omitted, the root directory is assumed.                              |
| storageName    | String | Query    | **Optional.** The name of your configured cloud storage service (e.g., `DropboxBusiness`, `S3Bucket`). If not specified, the API uses the account’s default storage. |
| region         | String | Query    | **Optional.** The locale setting (e.g., `en-GB`, `de-DE`) to apply for regional‑specific data interpretation during the scan.                                        |
| password       | String | Query    | **Optional.** The decryption password required to access a password‑protected workbook. Leave empty if the file is not encrypted.                                    |

### Response

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

The `BrokenLinks` collection contains objects of type **BrokenLink**. Each object provides the following properties:

- **CellName** – The address of the cell that contains the broken reference (e.g., `B12`).
- **LinkType** – The type of link that is broken (e.g., `ExternalReference`, `Formula`).
- **ErrorMessage** – A description of why the link is considered broken.

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid access token, client ID, or client secret.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.

## Where should we use the Search for broken links within the range of the Spreadsheet API?

- **Regular audit of large financial models** – Before releasing monthly or quarterly reports, automatically scan key calculation areas (e.g., `Dashboard!B5:K50`) that contain many external data references to ensure all links point to valid source files.
- **Data integration for mergers and acquisitions** – When merging multiple spreadsheet files representing business units, scan the “Overview” worksheet after integration to identify links that have become invalid due to changed file paths or permission issues.
- **Preparation of investor data packages** – Before finalising presentation materials that contain charts and tables linked to external databases or market‑data sources, verify the validity of all links.

## Why should you use the Search for broken links within the range of the Spreadsheet API?

- **Developer‑friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development with comprehensive documentation. Compared with building a custom solution, this significantly reduces development effort.
- **Reduced labour costs** – Eliminates the need for dedicated personnel to manually consolidate documents.
- **Pay‑per‑use** – No upfront investment; you only pay for the API calls you actually make.
- **Zero maintenance costs** – No servers to maintain, no software updates, and no compatibility concerns.
- **Preserves complex Excel formatting** – Results can be exported to universally accessible PDF format without losing styling.

## How to Use the Search for broken links within the range of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinksInRemoteRange) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to implement “search broken links in a range” with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}
