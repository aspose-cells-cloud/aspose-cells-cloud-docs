---
title: "Aspose.Cells Cloud Web API - Remove Duplicate Substrings"
second_title: " Aspose.Cells Cloud – Online, Short-Code,"
linktitle: "Remove Characters by Position"
type: docs
url: /remove-characters-by-position/
keywords: "Remove, Duplicate, Substrings"
description: "Finds and removes repeated substrings inside every cell of the chosen range, using user-defined or preset delimiters, while preserving formulas, formatting and data-validation."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

Finds and removes repeated substrings inside every cell of the chosen range, using user-defined or preset delimiters, while preserving formulas, formatting and data-validation.

## **Introduction**: Remove Unwanted Characters by Position

 **Position modes**  

- `theFirstNCharacters` – remove N characters from the start  
- `theLastNCharacters` – remove N characters from the end  
- `allCharactersBeforeText` – delete everything before the first occurrence of the supplied substring  
- `allCharactersAfterText` – delete everything after the first occurrence  
- `BetweenValues` – strip the substring (and optionally the delimiters themselves) between two user-defined values  

 **Options**  

- `caseSensitive` – affects `BeforeText`, `AfterText` and `BetweenValues` searches  

## **RemoveCharactersByPosition API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### The request parameters of **RemoveCharactersByPosition** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|theFirstNCharacters|Integer|Query|Specify removing the first n characters from selected cells.|
|theLastNCharacters|Integer|Query|Specify removing the last n characters from selected cells.|
|allCharactersBeforeText|String|Query|Specify using targeted removal options to delete text that is located before certain characters.|
|allCharactersAfterText|String|Query|Specify using targeted removal options to delete text that is located after certain characters.|
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

### Refine Your Text: Remove Unwanted Characters with Precision

### Error Codes

- **400 Bad Request**: Invalid Apose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Remove Characters by Position API?

- **Data Standardization**: Clean product codes (remove leading zeros/suffixes), phone numbers (strip country codes)
- **Text Extraction**: Extract key information from log files (remove timestamps/prefixes)
- **File Processing**: Organize filenames (remove uniform prefixes/date suffixes)
- **Data Parsing**: Process structured text (extract content between brackets/specific markers)
- **Database Management**: Clean imported data (remove fixed-format header/trailer redundant characters)

## Why should you use the Remove Characters by Position API?

- **Precise & Efficient**: Direct positional deletion eliminates complex regular expressions
- **Flexible Configuration**: 5 positioning modes + case sensitivity option for diverse scenarios
- **Batch Processing**: Clean entire data columns with one click, boosting efficiency 10x
- **Smart Parsing**: Easily handle complex content extraction between two delimiters

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/RemoveCharactersByPosition) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Remove characters for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
