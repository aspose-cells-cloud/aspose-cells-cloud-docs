---
title: "Aspose.Cells Cloud Remove Characters Web API – Delete Custom Characters & Substrings from Excel (Online Short‑Code)"
second_title: "Developer Guide"
ArticleTitle: "Excel Text Cleaner – Delete Characters & Substrings from Selected Range"
linktitle: "Remove Characters"
type: docs
url: /remove-characters/
keywords: "Aspose.Cells, remove characters, Excel API, text cleaning, spreadsheet"
description: "Remove custom characters, sets, or substrings from Excel cells using Aspose.Cells Cloud API for precise data cleaning."
weight: 100
---
The **RemoveCharacters** API (`PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters`) in Aspose.Cells Cloud enables precise deletion of user-defined characters, predefined symbol sets (such as non-printing characters, letters, digits, punctuation, or symbols), or substrings from a specified Excel cell range while preserving formulas, formatting, and data validation; it supports multiple removal modes including `CustomChars`, `CharacterSet`, and `Substring`, with optional case sensitivity and locale-aware processing.

## Overview

Easily clean and standardize your Excel data by removing specific, unwanted characters. Our add‑in offers multiple, targeted ways to sanitize your cells:

- **Remove Custom Characters**  
  Delete any specific symbols you define. Simply enter each character into the field, and the add‑in will instantly remove all instances from your selected cells. Perfect for eliminating unique delimiters, typos, or special marks.

- **Remove Character Sets (Bulk Cleaning)**
  - **Non‑printing Characters** – Cleanse your data of invisible characters that disrupt analysis and formatting (line breaks, carriage returns, tabs, and other control characters such as ASCII 0‑31, 127, 129, 141, 143, 144, 157).
  - **Text Characters (All Letters)** – Isolate numbers and symbols by stripping every letter (A‑Z, a‑z) from the selected range.
  - **Numeric Characters (All Digits)** – Extract pure text by deleting all digits (0‑9), ideal for cleaning product names or textual descriptions.
  - **Symbols** – Remove a wide array of symbolic clutter, including mathematical (e.g., ±, √), geometric (e.g., ∆, °), technical, currency (e.g., £, ¢), and letter‑like symbols (e.g., ™, ®, ©).
  - **Punctuation Marks** – Achieve clean, punctuation‑free text by deleting all punctuation marks such as periods, commas, quotation marks, and hyphens.

- **Remove a Specific Substring**  
  Go beyond single characters and delete entire words or specific character sequences. Effortlessly remove common prefixes, suffixes, or any redundant text phrases from your datasets.

**Version 4.0 – Updated 2024‑11‑15**

## The Remove Characters Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| removeTextMethod | String | Query | Specify the removal of text method type. |
| characterSets | String | Query | Specify the character sets. |
| removeCustomValue | String | Query | Specify the remove custom value. |
| caseSensitive | Boolean | Query | affects `Substring` mode and `CustomChars` when enabled |
| worksheet | String | Query | Specify the worksheet of spreadsheet. |
| range | String | Query | Specify the worksheet range of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response

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

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid access token, or incorrect client ID and secret.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – The spreadsheet encountered an anomaly while obtaining calculation data.

## Where Should You Use the Remove Characters API?

- **Data Import/Export** – Clean imported CSV/data by removing invisible characters and formatting errors.
- **Database Management** – Standardize product codes, IDs, and names by removing unwanted symbols or punctuation.
- **Financial Analysis** – Extract pure numbers by stripping currency symbols and text characters.
- **Text Processing** – Remove line breaks and tabs for clean text analysis and reporting.
- **Inventory Management** – Clean product names by eliminating redundant prefixes or suffixes.

## Why Use the Remove Characters API?

- **Save Time** – Bulk‑remove multiple character types instantly versus manual cleaning.
- **Ensure Accuracy** – Eliminate hidden characters that cause analysis errors and formatting issues.
- **Standardize Data** – Achieve consistent formatting across datasets and systems.
- **Improve Analysis** – Obtain clean, analysis‑ready data by isolating numbers or text as needed.
- **Fix Import Errors** – Remove problematic characters that break databases and formulas.
- **Developer‑Friendly** – Aspose.Cells Cloud provides SDK libraries in multiple languages, enabling quick development with comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.
- **Cost‑Effective** – Remove characters without first uploading the workbook, saving storage space and reducing costs.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to implement **Remove Characters** for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
