---
title: "Aspose.Cells Cloud – Swap Columns, Rows & Ranges (v4.0)"
second_title: "Document"
ArticleTitle: "Swap/Exchange Data Between Columns, Rows, and Cells in Excel"
linktitle: "Swap Range"
type: docs
url: /swap-range/
keywords: "Aspose Cells, Excel API, swap range, column swap, row swap, cloud spreadsheet"
description: "Swap columns, rows or ranges in Excel files with Aspose.Cells Cloud API. Preserve formatting, formulas, and cell references in a single request."
weight: 100
---

Automatically exchange data between any two columns, rows, ranges, or cells in Excel files using Aspose.Cells Cloud API. The Swap Range API enables precise data swapping while preserving all formatting, formulas, and cell references. It supports complex data re‑organization, batch processing, and seamless cloud integration for enterprise workflows.

## **Swap Range API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **Request Parameters**

| Parameter Name     | Type   | Location | Description                                                                                                                                   |
| ------------------ | ------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File   | FormData | **Required.** The source Excel workbook file (`.xlsx`, `.xls`).                                                                               |
| **worksheet1**     | String | Query    | **Required.** Name of the worksheet that contains the first data area.                                                                        |
| **range1**         | String | Query    | **Required.** Cell range (e.g., `A1:D10`) in `worksheet1` to be swapped.                                                                      |
| **worksheet2**     | String | Query    | **Required.** Name of the worksheet that contains the second data area (can be the same as `worksheet1`).                                     |
| **range2**         | String | Query    | **Required.** Cell range (e.g., `F1:I10`) in `worksheet2` to be swapped. **Important:** `range1` and `range2` must have identical dimensions. |
| **outPath**        | String | Query    | **Optional.** Cloud storage folder where the modified workbook will be saved.                                                                 |
| **outStorageName** | String | Query    | **Required.** Name of the configured cloud storage service (e.g., `MyCompanyStorage`).                                                        |
| **region**         | String | Query    | **Optional.** Locale setting (e.g., `en-US`, `ja-JP`) that may affect formatting.                                                             |
| **password**       | String | Query    | **Optional.** Password to decrypt a protected spreadsheet. Omit if not encrypted.                                                             |

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

| Code                 | Description                                                        |
| -------------------- | ------------------------------------------------------------------ |
| **400 Bad Request**  | Invalid request URI or mismatched range dimensions.                |
| **401 Unauthorized** | Invalid or expired access token; client‑id or secret is incorrect. |
| **404 Not Found**    | The specified spreadsheet file cannot be accessed.                 |
| **500 Server Error** | An internal error occurred while processing the workbook.          |

## Where Should We Use the Swap Range API?

- **Financial Model Restructuring** – Re‑organize data blocks (e.g., move Q3 forecast to Q4) while preserving formulas and conditional formatting.
- **Data Pipeline & ETL Processes** – Swap raw‑data ranges with cleaned ranges in a staging worksheet before final output.
- **Error Correction & Data Recovery** – Quickly correct misplaced data without manual copy‑pasting.

## Why Use the Swap Range API?

- **Developer‑Friendly** – SDKs are available for multiple languages, reducing development effort compared with building custom solutions.
- **Reduces Labor Costs** – Automates data reshuffling, decreasing the need for manual consolidation.
- **Pay‑per‑Use** – You only pay for the API calls you actually make.
- **Zero Maintenance** – No servers to manage, no software updates, and no compatibility concerns.

## Quick‑Start: Step‑by‑Step Guide

1. **Upload** the source workbook to your configured cloud storage (if it is not already there).
2. **Obtain** an OAuth 2.0 access token and set the `Authorization` header.
3. **Call** the **Swap Range API** with the required parameters (`worksheet1`, `range1`, `worksheet2`, `range2`).
4. **Specify** `outPath`/`outStorageName` if you want the modified file saved automatically; otherwise, read the file stream from the response.
5. **Download** the swapped workbook from the location you specified or directly from the response payload.

## How to Use the Swap Range API with SDKs

### Swap Range API Specification

The [Swap Range API Specification](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to swap ranges with concise code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
