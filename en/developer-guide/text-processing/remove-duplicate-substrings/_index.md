---
title: "Aspose.Cells Cloud Remove Duplicate Substrings Web API - Deduplicate Repeated Text in Excel"
second_title: "Document"
ArticleTitle: "Excel Duplicate Substring Remover - Clean Repeated Text in Cells"
linktitle: "Remove Duplicate Substrings"
type: docs
url: /remove-duplicate-substrings/
keywords: "Aspose.Cells remove duplicate substrings, Excel deduplication API, clean repeated text in cells, Excel text cleaning, substring removal, duplicate text removal, Excel data cleaning, Aspose.Cells Cloud API"
description: "Use Aspose.Cells Cloud API to automatically detect and remove duplicate substrings in Excel cells while preserving formatting, formulas, and data validation."
weight: 100
---

Remove duplicate substrings from Excel cells with intelligent detection. Keep original formatting intact while eliminating redundant text using Aspose.Cells deduplication API.

## **Introduction**: Remove Unwanted Characters with Precision

The Repeat Substring Cleaner API removes duplicate substrings within individual cells of an Excel range while preserving cell formatting, data validation, and other workbook structures. It processes each cell independently, keeping only the first occurrence of each duplicate substring.

### **Data Source Options**

| Field      | Type   | Required | Description                                             |
| ---------- | ------ | -------- | ------------------------------------------------------- |
| `workbook` | file   | Yes      | Excel workbook file (.xlsx, .xlsm)                      |
| `range`    | string | Yes      | Target range to process (e.g., "A1:D100", "Sheet1!A:D") |

### **Delimiter Options**

| Field                   | Type    | Default              | Description                                                   |
| ----------------------- | ------- | -------------------- | ------------------------------------------------------------- |
| `delimiters`            | string  | `"preset"`           | Options: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` or a custom delimiter string (treats multiple characters as a composite) |
| `treatConsecutiveAsOne` | boolean | `false`              | Collapse adjacent delimiters into a single separator |
| `ignoreCase`            | boolean | `false`              | Ignore case when comparing strings |

## **RemoveDuplicateSubstrings API**

### API Endpoint

```http
PUT http://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### The request parameters of **RemoveDuplicateSubstrings** API are

| Parameter Name | Type   | Path/Query String/HTTPBody | Description |
| :- | :- | :- | :- |
| Spreadsheet | File | FormData | The spreadsheet file to be processed. Supported formats include XLSX, XLS, ODS, CSV, etc. |
| delimiters | String | Query | Specifies one or more delimiter characters used to split cell content into substrings for duplicate detection and removal. Multiple delimiters can be specified (e.g., `",;|"`). |
| treatConsecutiveDelimitersAsOne | Boolean | Query | When set to `true`, consecutive delimiter characters are treated as a single separator. When `false`, each delimiter is processed individually. |
| caseSensitive | Boolean | Query | When `true`, duplicate detection considers letter case (e.g., "Text" ≠ "text"). When `false`, case is ignored during duplicate comparison. |
| worksheet | String | Query | *(Optional)* The name of the worksheet where duplicate substring removal will be applied. If omitted, the operation applies to the first worksheet. |
| range | String | Query | *(Optional)* The cell range where duplicate substring removal will be applied (e.g., `"A1:C10"`). If omitted, the operation applies to all used cells in the specified worksheet. |
| outPath | String | Query | *(Optional)* The cloud storage folder path where the processed workbook will be saved. If omitted, the file is saved in the source folder. |
| outStorageName | String | Query | The name of the cloud storage where the output file will be stored. |
| region | String | Query | *(Optional)* Sets the locale for text processing, which may affect delimiter interpretation and case‑sensitivity rules for certain languages (e.g., `"en-US"`, `"tr-TR"`). |
| password | String | Query | *(Optional)* If the uploaded spreadsheet is password‑protected, provide the password to open and process the file. |

### **Response**

```json
{
  File
}
```

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized**: Invalid access token, or invalid client ID and secret.  
- **404 Not Found**: The spreadsheet file is not accessible.  
- **500 Server Error**: The spreadsheet encountered an anomaly while obtaining calculation data.

## Where should we use the Remove Duplicate Substrings API?

- **Data Cleaning & Standardization Scenarios**: Clean up tags like `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.  
- **Technical & Operational Data**: Clean log entries with repeated error codes, remove duplicate bin/rack identifiers, and so on.  
- **Content & Media Management**: Deduplicate skill tags, remove redundant certification entries.

## Why should you use the Remove Duplicate Substrings API?

- **Automate Manual, Error‑Prone Work**: Eliminate tedious editing, reduce human error, and scale instantly.  
- **Preserve Data Integrity**: Cell colors, fonts, borders, and conditional formatting remain unchanged; drop‑down lists and validation rules are preserved.  
- **Flexible & Intelligent Processing**: Delimiter‑agnostic, case‑sensitive control, header protection.  
- **Seamless Integration**: API‑first design, language‑agnostic, returns a clean file.  
- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.  
- **Cost‑Effective**: You can remove duplicate substrings without first uploading the workbook, which saves storage space and reduces costs.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/TextProcessingController/RemoveDuplicateSubstrings) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement duplicate‑substring removal for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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