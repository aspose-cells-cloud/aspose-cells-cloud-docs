---
title: "Search & Replace in Aspose.Cells Cloud API – Excel Spreadsheet Manipulation"
second_title: "Document"
ArticleTitle: "Search and Replace in Spreadsheet – Aspose.Cells Cloud API"
linktitle: "Search and Replace"
type: docs
url: /search-replace/
keywords: "Aspose.Cells, Cloud API, Search and Replace, Excel, REST, API, spreadsheet automation, find and replace, Excel cloud"
description: "Learn how to use the Aspose.Cells Cloud **Search & Replace** API to find and replace text, formulas, or links in Excel workbooks. Includes endpoint details, request parameters, response examples, status codes, and code snippets for C#, Java, and Python."
weight: 50
---

The **Search & Replace** feature of Aspose.Cells Cloud API enables developers to programmatically locate and replace text, formulas, or hyperlinks within Excel workbooks stored in the cloud. Below you will find the full API specification, example requests, and sample code for the most common SDKs.

**Search & Replace API Specification**

**Endpoint**  
```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

**Path Parameters**  
- `fileName` – Name of the workbook file (including extension) stored in Aspose Cloud storage.

**Query Parameters**  
- `folder` – (optional) Folder path in cloud storage.  
- `storageName` – (optional) Storage name if not the default.  

**Request Body (JSON)**  
```json
{
  "text": "oldValue",
  "newText": "newValue",
  "isCaseSensitive": false,
  "matchWholeCell": false,
  "range": "A1:B10"
}
```

**Response (JSON)**  
```json
{
  "status": "OK",
  "replacedCount": 5,
  "link": "https://api.aspose.cloud/v3.0/cells/updatedWorkbook.xlsx"
}
```

**Status Codes**  
- `200` – Replacement completed successfully.  
- `400` – Invalid request parameters.  
- `401` – Authentication failed.  
- `500` – Server error.

**Code Samples**

*C#*
```csharp
var api = new CellsApi("clientId", "clientSecret");
var request = new SearchReplaceRequest
{
    Text = "oldValue",
    NewText = "newValue",
    IsCaseSensitive = false,
    MatchWholeCell = false,
    Range = "A1:B10"
};
var response = api.PostSearchReplace("Workbook.xlsx", request);
Console.WriteLine($"Replaced cells: {response.ReplacedCount}");
```

*Java*
```java
CellsApi api = new CellsApi("clientId", "clientSecret");
SearchReplaceRequest request = new SearchReplaceRequest()
        .text("oldValue")
        .newText("newValue")
        .isCaseSensitive(false)
        .matchWholeCell(false)
        .range("A1:B10");
SearchReplaceResponse response = api.postSearchReplace("Workbook.xlsx", request);
System.out.println("Replaced cells: " + response.getReplacedCount());
```

*Python*
```python
api = CellsApi(client_id, client_secret)
request = SearchReplaceRequest(
    text="oldValue",
    new_text="newValue",
    is_case_sensitive=False,
    match_whole_cell=False,
    range="A1:B10"
)
response = api.post_search_replace("Workbook.xlsx", request)
print(f"Replaced cells: {response.replaced_count}")
```

**Related Links**

- **[Replace Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/replace-content-in-remote-spreadsheet/)** – Replaces all occurrences of a specified string in a workbook stored on Aspose Cloud storage.  
- **[Replace Range Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/replace-content-in-remote-range/)** – Replaces content within a defined cell range of a remote workbook.  
- **[Replace Spreadsheet Content](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)** – Provides a bulk replace operation for the entire spreadsheet.  
- **[Replace Worksheet Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/replace-content-in-remote-worksheet/)** – Replaces text in a specific worksheet of a remote workbook.  
- **[Search Broken Links of Range in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-broken-links-in-remote-range/)** – Finds and reports broken hyperlinks within a defined range.  
- **[Search Broken Links of Worksheet in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-broken-links-in-remote-worksheet/)** – Detects broken links across an entire worksheet.  
- **[Search Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-content-in-remote-spreadsheet/)** – Searches for specific text, formulas, or values in a remote workbook.  
- **[Search for Broken Links in Remote Spreadsheets](https://docs.aspose.cloud/cells/search-broken-links-in-remote-spreadsheet/)** – Scans multiple workbooks for broken hyperlinks.  
- **[Search Range Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-content-in-remote-range/)** – Searches within a specific cell range.  
- **[Search Spreadsheet Broken Links](https://docs.aspose.cloud/cells/search-spreadsheet-broken-links/)** – Provides a comprehensive list of broken links across a spreadsheet.  
- **[Search Spreadsheet Content](https://docs.aspose.cloud/cells/search-spreadsheet-content/)** – General content search across the entire spreadsheet.  
- **[Search Worksheet Content in Remote Spreadsheet](https://docs.aspose.cloud/cells/search-content-in-remote-worksheet/)** – Searches for content within a particular worksheet.  