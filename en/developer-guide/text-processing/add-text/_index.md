---
title: "Aspose.Cells Cloud Web API - Add text"
second_title: " Aspose.Cells Cloud – Online, Short-Code,"
linktitle: "Add Text"
type: docs
url: /add-text/
keywords: ""
description: "Specify appending text to multiple cells at once, allowing you to add prefixes, suffixes, labels, or any specific characters. You can choose the exact position of the text—in the beginning, at the end, or before or after certain characters in the cell. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

Specify appending text to multiple cells at once, allowing you to add prefixes, suffixes, labels, or any specific characters. You can choose the exact position of the text—in the beginning, at the end, or before or after certain characters in the cell.

## Overview

One-call bulk insert of prefixes, suffixes, or anchored strings into every cell of a target range—no formulas, no helper columns.

- Insert custom text at **any position** inside each cell  

| Value            | Description |
|------------------|-------------|
| `None`           | No insert (placeholder) |
| `AtTheBeginning` | Insert at start (prefix) |
| `AtTheEnd`       | Insert at end (suffix) |
| `BeforeText`     | Insert **before** first occurrence of `selectText`; skip if not found |
| `AfterText`      | Insert **after** first occurrence of `selectText`; skip if not found |

- Four location modes: prefix, suffix, before/after a substring  
- Skip blank cells to avoid clutter  
- Only **string-type** values are touched; numbers, booleans and formulas are **converted to text first** (formulas are dropped to prevent corruption)  
- **Empty cells**  
  - `skipEmptyCells = true`  → skipped  
  - `skipEmptyCells = false` → filled with insert text (cell becomes text type)

- **Anchor not found**：When `position = BeforeText|AfterText` and `selectText` does **not** exist, the cell value remains unchanged

## **AddText API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/add/text
```

### The request parameters of **addText** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|text|String|Query|Specify the added text content.|
|position|String|Query|Indicates the specific location for adding text content.None, AtTheBeginning, AtTheEnd, BeforeText, AfterText.  |
|selectText|String|Query|Indicates selecting the specific position to add text based on the content of the text.|
|skipEmptyCells|Boolean|Query|Indicates skip empty cells.|
|worksheet|String|Query|Specify the worksheet of spreadsheet.|
|range|String|Query|Specify the worksheet range of spreadsheet.|
|outPath|String|Query|(Optional) The folder path where the workbook is stored. The default is null.|
|outStorageName|String|Query|Output file Storage Name.|
|region|String|Query|The spreadsheet region setting.|
|password|String|Query|The password for opening spreadsheet file.|

### **Response**

```json
{
File
}
```

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Merge Local Spreadsheet API?

## Why should you use the Merge Local Spreadsheet API?

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/AddText) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Add text for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
