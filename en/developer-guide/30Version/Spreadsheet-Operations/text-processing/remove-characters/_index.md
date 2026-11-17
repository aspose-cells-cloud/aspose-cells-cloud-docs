---
url: /excel-remove-characters/
title: Remove Characters from Excel – Aspose.Cells Cloud API (POST /cells/removecharacters)
description: "Remove specific characters or substrings from Excel cells via Aspose.Cells Cloud API POST /cells/removecharacters"
date: 2024-06-15
lastmod: 2024-06-15
tags:
  - excel
  - text-processing
  - api
keywords: "remove characters, Aspose.Cells, Excel API, text processing, cloud"
aliases:
  - /text-processing/remove-characters/
weight: 100
type: docs
linktitle: "Remove Characters from Excel"
ArticleTitle: "Aspose.Cells Cloud API: Remove Characters from Excel Files"
---

The **PostRemoveCharacters** API (`POST https://api.aspose.cloud/v3.0/cells/removecharacters`) in Aspose.Cells Cloud enables precise text cleaning within Excel worksheets by removing specified characters, character sets (such as non-printing characters, letters, digits, symbols, or punctuation), or substrings from selected cells — eliminating unwanted symbols, formatting artifacts, or inconsistent text patterns — and supports data preprocessing, validation, and workflow automation through a single, flexible request body parameter. Note that this operation modifies cell values _in-place_ and returns the updated workbook as a base64-encoded string in the response.

## The Post Remove Characters Web API

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name          | Type                          | Path/Query String/HTTPBody | Description |
| ----------------------- | ----------------------------- | -------------------------- | ----------- |
| removeCharactersOptions | class:removecharactersoptions | HTTPBody                   | -           |

### Response

```json
[
  {
    "Name": "FileInfo",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FileInfo"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

On success, the API returns a `FileInfo` object containing metadata and the updated file content.

| Field         | Description                                              |
| ------------- | -------------------------------------------------------- |
| `Code`        | HTTP status code (200 for success).                      |
| `Status`      | Operation result (`"OK"`).                               |
| `Filename`    | Name of the modified file.                               |
| `Filesize`    | Size of the updated file in bytes.                       |
| `FileContent` | Base64-encoded binary content of the updated Excel file. |

### `RemoveCharactersOptions` Schema

| Property           | Type    | Required | Description                                                                              |
| ------------------ | ------- | -------- | ---------------------------------------------------------------------------------------- |
| `Range`            | string  | Yes      | A1-style range (e.g., `"A1:C10"`) or named range to process.                             |
| `CustomCharacters` | string  | No       | String of characters to remove (e.g., `"@#$"`). Each character is treated individually.  |
| `CharacterSet`     | string  | No       | Predefined set: `"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, or `"Punctuation"`. |
| `Substring`        | string  | No       | Exact substring to remove (e.g., `"USD"`, `"°C"`).                                       |
| `IgnoreCase`       | boolean | No       | If `true`, substring and text-character removal is case-insensitive. Default: `false`.   |

> **Tip**: Only one of `CustomCharacters`, `CharacterSet`, or `Substring` should be specified per request to avoid ambiguous behavior.

### Supported Character Sets

| Set           | Characters Removed                                                 | Use Case                                                            |
| ------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------- |
| `NonPrinting` | ASCII 0–31, 127, 129, 141, 143, 144, 157                           | Remove hidden line breaks, control chars, and formatting artifacts. |
| `Text`        | All letters (A–Z, a–z)                                             | Strip alphabetic characters (e.g., to extract pure numbers).        |
| `Numeric`     | All digits (0–9)                                                   | Remove numbers, leaving text or symbols.                            |
| `Symbols`     | Math (`+`, `×`, `π`), currency (`€`, `¥`), punctuation-like (™, №) | Standardize technical or financial data.                            |
| `Punctuation` | `.,;:!?'"()[]{}-`                                                  | Clean natural-language text for NLP or indexing.                    |

## How to Use the Post Remove Characters API with SDKs?

### Post Remove Characters API Specification

The <a href="https://reference.aspose.cloud/cells/#/TextProcessing/PostRemoveCharacters" rel="noopener noreferrer">Post Remove Characters API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**Example cURL Request**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -H "Content-Type: application/json" \
  -d '{
    "Range": "A1:B20",
    "CustomCharacters": "@#$",
    "Substring": "USD",
    "IgnoreCase": true
  }'
```

**Success Response (200 OK)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Filename": "cleaned_report.xlsx",
  "Filesize": 45892,
  "FileContent": "UEsDBBQABgAIAAAAIQDf...[base64-encoded .xlsx content]"
}
```

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
