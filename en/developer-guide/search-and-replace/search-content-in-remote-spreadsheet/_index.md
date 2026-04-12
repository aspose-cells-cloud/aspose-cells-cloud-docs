---
title: "Search Text in Remote Excel Spreadsheets – Aspose.Cells Cloud API"
second_title: "Document"
ArticleTitle: "Search Text in Remote Excel Spreadsheets – Find Specific Data"
linktitle: "Search Remote Spreadsheet Content"
type: docs
url: /search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, Excel search API, cloud spreadsheet, text search, REST"
description: "Search for text, numbers, or formulas in Excel files stored in cloud storage using Aspose.Cells Cloud. Supports case‑insensitive queries, folder selection, and password‑protected workbooks."
weight: 100
---

### **Search Content in Remote Spreadsheet API**

Programmatically search for specific text within any Excel spreadsheet using the Aspose.Cells Cloud API. Find text, numbers, or formulas in files stored in cloud storage. This RESTful API enables automated data discovery, content analysis, and spreadsheet‑auditing workflows.

### **Web API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Request Parameters:**

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                                                                                                                      |
| :------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Path                       | **Required**. The filename of the Excel workbook (including extension) where the text search will be performed, e.g., `sales_data.xlsx`.                         |
| searchText     | String  | Query                      | **Required**. The exact string, number, or partial content to locate across the entire workbook or worksheet(s).                                                 |
| ignoringCase   | Boolean | Query                      | **Optional**. Determines case‑sensitivity. Set to `true` for case‑insensitive matching (e.g., “Report” matches “REPORT”); default is `false`.                    |
| folder         | String  | Query                      | **Optional**. The directory path within your cloud storage that contains the target workbook. If omitted, the root folder is assumed.                            |
| storageName    | String  | Query                      | **Optional**. The name identifier for a custom‑configured cloud storage service. If not specified, the API uses the default storage associated with the account. |
| region         | String  | Query                      | **Optional**. The locale setting (e.g., `es-ES`) applied during the search, which may affect text normalization or collation rules.                              |
| password       | String  | Query                      | **Optional**. The decryption password required to access a password‑protected Excel file. Omit this parameter if the file is not encrypted.                      |

**Glossary**

- **searchText** – The exact string to locate; can be a partial match.
- **ignoringCase** – `true` makes the search case‑insensitive; `false` enforces case‑sensitivity.
- **folder** – Path to the directory that holds the workbook.
- **storageName** – Identifier of a custom storage configuration.
- **region** – Locale code that influences text comparison rules.
- **password** – Decryption password for protected workbooks.

### **Response**

```json
{
  "Cells": [
    {
      "CellName": "A1",
      "WorksheetName": "Sheet1",
      "Text": "Report"
    },
    {
      "CellName": "B5",
      "WorksheetName": "Sheet2",
      "Text": "Report"
    }
  ],
  "Status": "OK"
}
```

The response contains a list of cells (`CellName`) where the searched text was found, together with the worksheet name and the matching text. If no matches are found, the `Cells` array is empty and the request still returns HTTP 200 OK.

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Invalid access token, client ID, or client secret.
- **404 Not Found** – The spreadsheet file is not accessible.
- **500 Server Error** – An unexpected condition prevented the API from completing the request.

## Where should we use the Search content within the Spreadsheet API?

- **Comprehensive workbook compliance audit** – Quickly scan the entire Excel file to identify all sensitive terms (e.g., “Confidential Clause”, “Internal Data”) for enterprise data‑security and compliance checks.
- **Cross‑sheet data association query** – When project information is scattered across multiple worksheets, search for a specific project number or customer name and instantly locate all related data.
- **Batch template content verification** – After automated report generation, scan multiple Excel files in batches to confirm that all preset placeholders (such as `{{Date}}`) have been correctly replaced, ensuring report completeness and accuracy.
- **Historical data archiving and mining** – Analyse legacy files, search for specific event codes or business terms, and quickly understand historical business logic for data archaeology.

## Why should you use the Search content within the Spreadsheet API?

- **Developer‑friendly** – Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling rapid development with comprehensive documentation. Compared with building custom solutions, this significantly reduces development effort.
- **Reduced labor costs** – Automates repetitive search tasks, freeing developers from manual data‑extraction work.
- **Pay‑per‑use** – No upfront investment; you only pay for the API calls you actually use.
- **No maintenance required** – Aspose manages servers, updates, and compatibility, so you can focus on your application logic.
- **Preserves complex Excel formatting** – Results can be exported to universally accessible PDF format while retaining original styling.

## How to Use the Search for broken links within the range of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteSpreadsheet) defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search content within spreadsheets for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
