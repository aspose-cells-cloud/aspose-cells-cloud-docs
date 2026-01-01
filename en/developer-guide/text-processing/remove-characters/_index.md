---
title: "Aspose.Cells Cloud Web API - Remove characters"
second_title: " Aspose.Cells Cloud – Online, Short-Code,"
linktitle: "Remove Characters"
type: docs
url: /remove-characters/
keywords: ""
description: "Perform operations or delete any custom characters, character sets, and substrings within a selected range for a specific position. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

Perform operations or delete any custom characters, character sets, and substrings within a selected range for a specific position.

## **Introduction**: Remove Unwanted Characters with Precision

Easily clean and standardize your Excel data by removing specific, unwanted characters. Our add-in offers multiple, targeted ways to sanitize your cells:

- **Remove Custom Characters**
Delete any specific symbols you define. Simply enter each character into the field, and the add-in will instantly remove all instances from your selected cells. Perfect for eliminating unique delimiters, typos, or special marks.

- **Remove Character Sets (Bulk Cleaning)**

  - **Non-printing Characters**: Cleanse your data of invisible characters that disrupt analysis and formatting. This includes line breaks, carriage returns, tabs, and other control characters (ASCII values 0-31, 127, 129, 141, 143, 144, and 157).

  - **Text Characters (All Letters)**: Isolate numbers and symbols by stripping every letter (A-Z, a-z) from the selected range.

  - **Numeric Characters (All Digits)**: Extract pure text by deleting all digits (0-9), ideal for cleaning product names or textual descriptions.

  - **Symbols**: Remove a wide array of symbolic clutter, including mathematical (e.g., ±, √), geometric (e.g., ∆, °), technical, currency (e.g., £, ¢), and letter-like symbols (e.g., ™, ®, ©).

  - **Punctuation Marks**: Achieve clean, punctuation-free text by deleting all punctuation marks like periods, commas, quotation marks, and hyphens.

- **Remove a Specific Substring**
Go beyond single characters and delete entire words or specific character sequences. Effortlessly remove common prefixes, suffixes, or any redundant text phrases from your datasets.

## **RemoveCharacters API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### The request parameters of **removeCharacters** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|removeTextMethod|String|Query|Specify the removal of text method type. The default value is None, others values are RemoveCustomCharacter, RemoveCharacterSets, RemoveSubString.|
|characterSets|String|Query|Specify the character sets.The default value is None, others values are NonPrintingCharacters, TextCharacters, NumericCharacters, Symbols, PunctuationMarks.|
|removeCustomValue|String|Query|Specify the remove custom value.|
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

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Remove Characters API?

- **Data Import/Export**: Clean imported CSV/data by removing invisible characters and formatting errors
- **Database Management**: Standardize product codes, IDs, and names by removing unwanted symbols/punctuation
- **Financial Analysis**: Extract pure numbers by stripping currency symbols and text characters
- **Text Processing**: Remove line breaks, tabs for clean text analysis and reporting
- **Inventory Management**: Clean product names by eliminating redundant prefixes/suffixes

## Why should you use the Remove Characters API?

- **Save Time**: Bulk remove multiple character types instantly vs manual cleaning
- **Ensure Accuracy**: Eliminate hidden characters that cause analysis errors and formatting issues
- **Standardize Data**: Achieve consistent formatting across datasets and systems
- **Improve Analysis**: Get clean, analysis-ready data by isolating numbers or text as needed
- **Fix Import Errors**: Remove problematic characters that break databases and formulas

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/RemoveCharacters) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement Remove characters for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}
