---
title: "Aspose.Cells Cloud Web API - Remove Duplicate Substrings"
second_title: " Aspose.Cells Cloud – Online, Short-Code,"
linktitle: "Remove Duplicate Substrings"
type: docs
url: /remove-duplicate-substrings/
keywords: ""
description: "Perform operations or delete any custom characters, character sets, and substrings within a selected range for a specific position. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

Perform operations or delete any custom characters, character sets, and substrings within a selected range for a specific position.

## **Introduction**: Remove Unwanted Characters with Precision

The Repeat Substring Cleaner API removes duplicate substrings within individual cells of an Excel range while preserving cell formatting, data validation, and other workbook structure. It processes each cell independently, keeping only the first occurrence of each duplicate substring.

### **Data Source Options**

| Field      | Type   | Required | Description                                             |
| ---------- | ------ | -------- | ------------------------------------------------------- |
| `workbook` | file   | Yes      | Excel workbook file (.xlsx, .xlsm)                      |
| `range`    | string | Yes      | Target range to process (e.g., "A1:D100", "Sheet1!A:D") |

### **Delimiter Options**

| Field                   | Type    | Default              | Description                                                   |
| ----------------------- | ------- | -------------------- | ------------------------------------------------------------- |
| `delimiters`            | string  | `"preset"`           | Options: `preset`, `custom` , `comma`, `semicolon`, `space`, `tab`, `line-break` or Custom delimiter string (treats multiple chars as composite)                                  |
| `treatConsecutiveAsOne` | boolean | `false`              | Collapse adjacent delimiters into single separator            |
| `ignoreCase`            | boolean | `false`              | Ignore case when comparing strings                            |

## **RemoveDuplicateSubstrings API**

```http
PUT http://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### The request parameters of **removeCharacters** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
|Spreadsheet|File|FormData|Upload spreadsheet file.|
|delimiters|String|Query|delimiters|
|treatConsecutiveDelimitersAsOne|Boolean|Query|collapse adjacent delimiters into a single separator.|
|caseSensitive|String|Boolean||
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

## Where should we use the Remove Duplicate Substrings API?

- **Data Cleaning & Standardization Scenarios**: Clean up tags like `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"
- **Technical & Operational Data**:  Clean log entries with repeated error codes, Remove duplicate bin/rack identifiers, and so on.
- **Content & Media Management**: Deduplicate skill tags,  Remove redundant certification entries.

## Why should you use the Remove Duplicate Substrings API?

- **Automate Manual, Error-Prone Work**: Eliminate tedious editing, Reduce human error, Scale instantly.
- **Preserve Data Integrity**: Cell colors, fonts, borders, and conditional formatting remain unchanged, Drop-down lists and validation rules are preserved.
- **Flexible & Intelligent Processing**: Delimiter-agnostic, Case-sensitive control, Header protection.
- **Seamless Integration**: API-first design, Language agnostic, Returns clean file.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/RemoveDuplicateSubstrings) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

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
