---
title: "Aspose.Cells Cloud Data Exchange Web API - Swap Columns, Rows & Ranges"
second_title: "Document"
ArticleTitle: "Swap/Exchange Data Between Columns, Rows & Cells in Excel"
linktitle: "Swap Range"
type: docs
url: /swap-range/
keywords: "Excel swap columns API, exchange rows API, swap cell data API, range exchange API, Aspose Cells REST API, Excel data manipulation API, rearrange spreadsheet API, column switching API, row swapping API, Excel automation API, cloud data exchange, batch data rearrangement"
description: "Learn how to efficiently exchange or swap data between any two columns, rows, ranges, or individual cells in Excel. Step-by-step guide to rearrange your spreadsheet data without losing formatting or formulas. Perfect for data reorganization, column/row swapping, and spreadsheet optimization. The Swap Ranges for Excel API provides a powerful tool to interchange any two columns, rows, ranges, or individual cells within an Excel file. This API allows users to efficiently rearrange their tables, ensuring that the original data formatting is preserved and all existing formulas continue to function correctly. By leveraging this API, users can streamline their data manipulation tasks and maintain the integrity of their spreadsheets."
weight: 100
---

Automatically exchange data between any two columns, rows, ranges, or cells in Excel files using Aspose.Cells Cloud API. Our powerful API enables precise data swapping while preserving all formatting, formulas, and cell references. Supports complex data reorganization, batch processing, and seamless cloud integration for enterprise workflows.

## **Swap Range API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Spreadsheet | File | FormData | **Required**. The source Excel workbook file (e.g., `.xlsx`, `.xls`) that contains the data to be exchanged. |
| worksheet1 | String | Query | **Required**. The name of the source worksheet containing the first data area to be exchanged. |
| range1 | String | Query | **Required**. The cell range address (e.g., `"A1:D10"`) within `worksheet1` that defines the source data area for the exchange. |
| worksheet2 | String | Query | **Required**. The name of the target worksheet containing the second data area to be exchanged. This can be the same as `worksheet1` if exchanging ranges within a single sheet. |
| range2 | String | Query | **Required**. The cell range address (e.g., `"F1:I10"`) within `worksheet2` that defines the target data area for the exchange. **Important**: `range1` and `range2` must have identical dimensions (the same number of rows and columns). |
| outPath | String | Query | **Optional**. The target folder path in cloud storage where the modified workbook will be saved. If omitted or set to `null`, the file is saved in the default or source file directory. |
| outStorageName | String | Query | **Required**. The name of your configured cloud storage service (e.g., `MyCompanyStorage`) where the output file should be written. |
| region | String | Query | **Optional**. The locale setting (e.g., `en-US`, `ja-JP`) to apply during processing, which can affect data formatting. |
| password | String | Query | **Optional**. The password to decrypt a password-protected spreadsheet. Omit if the file is not encrypted. |

### **Response**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Swap Range API?

- **Financial Model Restructuring**: When reorganizing a financial model to swap entire data blocks between different sections (e.g., moving Q3 forecast data to Q4) while preserving all formulas, formatting, and conditional rules.
- **Data Pipeline & ETL Processes**: As part of an automated pipeline to swap raw data ranges with cleaned, processed data ranges in a staging worksheet before final output.
- **Error Correction & Data Recovery**: When data has been accidentally entered into the wrong section of a spreadsheet, this API can perform a precise swap to restore the correct layout without manual copy-pasting.

## Why should you use the Swap Range API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart rendering solutions, this significantly reduces the development workload.
- **Reduced Labor Costs**: Reduced the need for positions dedicated to document consolidation.
- **Pay-per-use**: No upfront investment, only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.

## How to Use the Swap Range API with SDKs

### Swap Range API Specification

The [Swap Range API Specification](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to swap range with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}
