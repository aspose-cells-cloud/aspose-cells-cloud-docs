---
title: "Aspose.Cells Cloud Add Text API – Add Text to Multiple Excel Cells at Once – Insert Prefixes, Suffixes & Labels"
second_title: "Document"
ArticleTitle: "Bulk Text Insertion for Excel – Add Prefixes, Suffixes & Custom Text to Cells – Step‑by‑Step Guide"
linktitle: "AddText"
type: docs
url: /add-text/
keywords: "Aspose Cells API, add text Excel, bulk text insertion, prefix suffix Excel, spreadsheet text replace"
description: "Insert prefixes, suffixes, or custom labels into many Excel cells in one call with Aspose.Cells Cloud. Choose start, end, before or after any text. Supports range, worksheet, and empty‑cell handling."
weight: 100
---

Insert text into multiple Excel cells in one operation. Add prefixes, suffixes, labels, or custom characters at the beginning, end, or before/after specific text within cells using Aspose.Cells API.

## Overview

One‑call bulk insert of prefixes, suffixes, or anchored strings into every cell of a target range—no formulas, no helper columns.

- Insert custom text at **any position** inside each cell  

| Value            | Description |
|------------------|-------------|
| `None`           | Replace the original content |
| `AtTheBeginning` | Insert at start (prefix) |
| `AtTheEnd`       | Insert at end (suffix) |
| `BeforeText`     | Insert **before** first occurrence of `selectText`; skip if not found |
| `AfterText`      | Insert **after** first occurrence of `selectText`; skip if not found |

- Four location modes: prefix, suffix, before/after a substring.  
- Skip blank cells to avoid clutter.  
- The API touches only **string‑type** values; numbers, booleans, and formulas are first converted to text.  
- **Empty cells**  
  - `skipEmptyCells = true` → empty cells are skipped.  
  - `skipEmptyCells = false` → empty cells are filled with the insert text (cell becomes text type).  

- **Anchor not found**: When `position = BeforeText | AfterText` and `selectText` does **not** exist, the cell value remains unchanged.

## **AddText API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/content/add/text
```

### The request parameters of the **AddText** API are

| Parameter Name | Type   | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| Spreadsheet | File | FormData | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc. |
| text | String | Query | The text content to be added to the specified cells in the spreadsheet. |
| position | String | Query | Specifies where to insert the text relative to the existing cell content. Options: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`. |
| selectText | String | Query | *(Optional)* If provided, the text will be added only in cells that contain this exact substring. Used in conjunction with the `position` parameter. |
| skipEmptyCells | Boolean | Query | If `true`, empty cells are skipped; if `false`, text is added to empty cells. |
| worksheet | String | Query | *(Optional)* The name of the worksheet where text will be added. If omitted, the operation applies to the first worksheet by default. |
| range | String | Query | *(Optional)* The cell range where text will be added (e.g., `"A1:C10"`). If omitted, the operation applies to all used cells in the specified worksheet. |
| outPath | String | Query | *(Optional)* The cloud storage folder path where the processed workbook will be saved. If omitted, the file is saved in the source folder. |
| outStorageName | String | Query | The name of the cloud storage where the output file will be stored. |
| region | String | Query | *(Optional)* Sets the locale for formatting numbers, dates, and currency in the output file (e.g., `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password | String | Query | *(Optional)* If the uploaded spreadsheet is password‑protected, provide the password to open and process the file. |

### **Response**

```json
{
  "file": "output.xlsx",
  "size": 12345
}
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized**: Invalid access token or invalid client ID and secret.  
- **404 Not Found**: The spreadsheet file is not accessible.  
- **500 Server Error**: The spreadsheet encountered an anomaly while obtaining calculation data.

## Where should we use the Add Text for Spreadsheet API?

- **Dynamic Report Labeling**: Add dynamic titles, date tags, or notes to automatically generated financial statements and sales reports.  
- **Batch File Watermarking**: Add company logos, confidentiality watermarks, or version information to a batch of Excel files.  
- **Template Data Filling**: Automatically fill in client names, amounts, and other text in designated positions of contract or invoice templates.  
- **Data Classification Tagging**: Automatically add classification tags or status labels (e.g., “Pending Review”, “Approved”) to data rows based on analysis results.  
- **Data Quality Annotation**: Add notes for problematic data during data cleaning.  
- **Batch Text Formatting**: Uniformly add prefixes or suffixes to product names or client names.

## Why should you use the Add Text for Spreadsheet API?

- **Batch Text Addition**: Add text to hundreds of cells or files at once, saving up to 95 % of the time compared to manual work.  
- **Precise Position Control**: Supports inserting text accurately at six positions, including the start, end, or before/after specific text within a cell.  
- **Smart Conditional Handling**: Decide whether to add text based on whether a cell is empty or contains specific text.  
- **Multi‑Position Strategy Support**:  
  - `AtTheBeginning`: Add the same text before the content of all selected cells.  
  - `AtTheEnd`: Add text after the content of all selected cells.  
  - `BeforeText` / `AfterText`: Add text only before or after cells containing specific text.  
  - `None`: Replace the original content.  
- **Precise Range Control**: Allows specifying particular worksheets or cell ranges for operations.  
- **Conditional Skip Option**: Supports skipping empty cells to avoid unnecessary text addition.  
- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared to building custom chart‑rendering solutions, this significantly reduces development workload.  
- **Cost‑Effective**: You can append text in a cell without first uploading the workbook, which saves storage space and reduces costs.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/AddText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Add Text for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}