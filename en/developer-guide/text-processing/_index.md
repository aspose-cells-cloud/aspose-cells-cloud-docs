---
title: "Aspose.Cells Cloud API – Text Processing (Trim, Split, Convert, Extract, Remove)"
second_title: "Document"
ArticleTitle: "Spreadsheet Text Processing: Trim, Split, Convert, Extract, and Remove Text"
linktitle: "Text Processing"
type: docs
url: /text-processing/
description: "Learn how to trim, split, convert, extract, and remove text in Excel files using Aspose.Cells Cloud REST APIs. Includes concise examples and SDK snippets."
keywords: "Aspose.Cells, Cloud API, Text Processing, Trim Text, Split Text, Convert Text, Extract Text, Remove Text, Excel API"
weight: 30
---

## Excel Text Manipulation APIs

Aspose.Cells Cloud offers a collection of REST endpoints that let you manipulate text inside Excel worksheets. These operations cover everyday tasks such as trimming whitespace, splitting strings, converting case, extracting substrings, and removing unwanted characters.  

**Prerequisites:** All requests must be authenticated with a valid access token supplied in the `Authorization` header. Refer to the authentication guide for details on obtaining and using tokens.

Below is a concise reference that summarises the most frequently used text‑processing endpoints.

| Operation | HTTP Method | Endpoint (template) | Key Parameters | Sample Response |
|-----------|------------|---------------------|----------------|-----------------|
| Trim whitespace or characters | POST | `/cells/{file}/worksheets/{sheet}/cells/trim` | `range`, `trimChars` (optional) | `{ "code": 200, "status": "OK", "trimmedCells": 12 }` |
| Split text into multiple cells | POST | `/cells/{file}/worksheets/{sheet}/cells/split` | `range`, `delimiter`, `destinationRange` | `{ "code": 200, "status": "OK", "splitCells": 8 }` |
| Convert text case (upper, lower, title) | POST | `/cells/{file}/worksheets/{sheet}/cells/convert-case` | `range`, `caseType` | `{ "code": 200, "status": "OK", "convertedCells": 15 }` |
| Extract substring | POST | `/cells/{file}/worksheets/{sheet}/cells/extract` | `range`, `startIndex`, `length` | `{ "code": 200, "status": "OK", "extractedValue": "Sample" }` |
| Remove specific characters | POST | `/cells/{file}/worksheets/{sheet}/cells/remove-characters` | `range`, `characters` | `{ "code": 200, "status": "OK", "removedChars": 5 }` |

### Basic Text Operations

- [How to Add Text to an Excel File Using Aspose.Cells API](/cells/add-text/)
- [How to Change Text Case in Excel Files with Aspose.Cells Cloud API](/cells/change-word-case/)
- [How to Convert Text Format in Excel Using Aspose.Cells API](/cells/convert-text/)

### Text Cleaning & Processing

- [How to Remove Specific Characters from Excel Files via API](/cells/remove-characters/)
- [How to Remove Characters by Position in Excel Cells Using API](/cells/remove-characters-by-position/)
- [How to Trim Whitespace and Characters from Excel Cells via API](/cells/trim-character/)

### Advanced Text Handling

- [How to Remove Duplicate Substrings from Excel Data via API](/cells/remove-duplicate-substrings/)
- [How to Split Text into Multiple Cells in Excel Using API](/cells/split-text/)