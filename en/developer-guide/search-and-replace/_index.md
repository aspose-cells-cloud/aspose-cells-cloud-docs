---
title: "Search & Replace in Aspose.Cells Cloud API – Excel Spreadsheet Manipulation"
second_title: "Document"
ArticleTitle: "Search and Replace in Spreadsheet – Aspose.Cells Cloud API"
linktitle: "Search and Replace"
type: docs
url: /search-replace/
keywords: "Aspose.Cells, Cloud API, Search and Replace, Excel, REST, Spreadsheet automation"
description: "Learn how to use the Aspose.Cells Cloud Search & Replace API to locate and replace text, formulas, or hyperlinks in Excel workbooks. Includes endpoint details, parameters, response examples, status codes, and code snippets for C#, Java, and Python."
weight: 50
---

The **Search & Replace** feature of Aspose.Cells Cloud API enables developers to programmatically locate and replace text, formulas, or hyperlinks within Excel workbooks stored in the cloud.

*Last updated: July 2026*

**API Specification**

**HTTP Method:** `POST`  
**Endpoint:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/replace`  

**Path parameters**

| Parameter | Type   | Description                              |
|-----------|--------|------------------------------------------|
| `fileName`| string | Name of the workbook (including extension) stored in Aspose Cloud storage. |
| `sheetName`| string| Name of the worksheet where the replace operation will be performed. |

**Query parameters**

| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `searchText` | string | Yes | Text, formula, or hyperlink to search for. |
| `newText`    | string | Yes | Replacement text, formula, or hyperlink. |
| `matchCase` | boolean| No  | Set to `true` for case‑sensitive search (default: `false`). |
| `matchWholeCell` | boolean | No | Set to `true` to replace only when the whole cell matches the search text (default: `false`). |
| `folder` | string | No | Cloud folder where the workbook is located. |
| `storage`| string | No | Name of the Aspose Cloud storage. |

**Request body** (optional, JSON) – can be used when performing a bulk replace across the entire workbook:

```json
{
  "SearchText": "oldValue",
  "NewText": "newValue",
  "MatchCase": false,
  "MatchWholeCell": false
}
```

**Responses**

| Status Code | Description                              |
|-------------|------------------------------------------|
| `200`       | Replace operation succeeded; response contains the number of replacements made. |
| `400`       | Bad request – missing required parameters or invalid values. |
| `401`       | Unauthorized – authentication token is missing or invalid. |
| `404`       | Workbook, worksheet, or specified range not found. |
| `500`       | Server error – operation could not be completed. |

**Success response example (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Replacements": 12,
  "Message": "Search and replace completed successfully."
}
```

**Code Samples**

* C# – [SearchReplace.cs](/samples/csharp/SearchReplace.cs)  
* Java – [SearchReplace.java](/samples/java/SearchReplace.java)  
* Python – [search_replace.py](/samples/python/search_replace.py)

---

Related operations (each link now includes a brief description for easier navigation):

- **[Replace Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/replace-content-in-remote-spreadsheet/)** – Replace all occurrences of a string in a workbook stored on Aspose Cloud storage.  
- **[Replace Range Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/replace-content-in-remote-range/)** – Replace content within a defined cell range of a remote workbook.  
- **[Replace Spreadsheet Content](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)** – Perform a bulk replace operation for the entire spreadsheet.  
- **[Replace Worksheet Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/replace-content-in-remote-worksheet/)** – Replace text in a specific worksheet of a remote workbook.  
- **[Search Broken Links of Range in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-broken-links-in-remote-range/)** – Find and report broken hyperlinks within a defined range.  
- **[Search Broken Links of Worksheet in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-broken-links-in-remote-worksheet/)** – Detect broken links across an entire worksheet.  
- **[Search Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-content-in-remote-spreadsheet/)** – Search for specific text, formulas, or values in a remote workbook.  
- **[Search for Broken Links in Remote Spreadsheets](https://docs.aspose.cloud/cells/search-broken-links-in-remote-spreadsheet/)** – Scan multiple workbooks for broken hyperlinks.  
- **[Search Range Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-content-in-remote-range/)** – Search within a specific cell range.  
- **[Search Spreadsheet Broken Links](https://docs.aspose.cloud/cells/search-spreadsheet-broken-links/)** – Provide a comprehensive list of broken links across a spreadsheet.  
- **[Search Spreadsheet Content](https://docs.aspose.cloud/cells/search-spreadsheet-content/)** – General content search across the entire spreadsheet.  
- **[Search Worksheet Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-content-in-remote-worksheet/)** – Search for content within a particular worksheet.  