---
title: "Aspose.Cells Cloud Excel Text Search Web API – Find Text in Remote Worksheet"
second_title: "Document"
ArticleTitle: "Search Text in Remote Excel Spreadsheet Worksheet – Find Specific Data"
linktitle: "Search Remote Worksheet Content"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Aspose, Cells, Excel, API, text search, remote worksheet, cloud storage"
description: "Search for text, numbers, or formulas in a remote Excel worksheet using Aspose.Cells Cloud API. Supports case‑insensitive searches and password‑protected files."
weight: 100
---

## **Search Content in Remote Worksheet**

Programmatically search for specific text within any Excel worksheet using the Aspose.Cells Cloud API. The service can locate text, numbers, or formulas in remote files stored in cloud storage, enabling automated data‑discovery, content‑analysis, and spreadsheet‑auditing workflows.

**Prerequisites**  
- A valid Aspose.Cloud JWT access token (see the Authentication link below).  
- The workbook must be stored in Aspose Cloud storage.  
- Appropriate permissions for the target storage location.

### **Web API**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

| Parameter Name | Type    | Path/Query String/HTTP Body | Description                                                                                       |
| -------------- | ------- | --------------------------- | ------------------------------------------------------------------------------------------------- |
| name           | String  | Path                        | **Required.** The filename of the target workbook (e.g., `annual_report.xlsx`).                   |
| worksheet      | String  | Path                        | **Required.** The worksheet within the workbook where the search is performed.                    |
| searchText     | String  | Query                       | **Required.** The exact text string or number to locate.                                          |
| ignoreCase     | Boolean | Query                       | **Optional.** When `true`, the search is case‑insensitive. Default is `false`.                    |
| folder         | String  | Query                       | **Optional.** Path to the folder containing the workbook. If omitted, the root folder is used.    |
| storageName    | String  | Query                       | **Optional.** Name of a custom‑configured cloud storage. If omitted, the default storage is used. |
| region         | String  | Query                       | **Optional.** Locale setting (e.g., `ja-JP`) that may affect text comparison.                     |
| password       | String  | Query                       | **Optional.** Password for a protected workbook. Omit if the file is not encrypted.               |

### **Response**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Array of matches. Each item contains the cell address (`cellName`), the matched string (`text`), and how many times it appears in that cell (`occurrences`).
- **code** – HTTP status code returned by the service.
- **status** – Textual description of the result.

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## Where should we use the Search content within the worksheet of the Spreadsheet API?

- **Workbook compliance audit:** Quickly locate sensitive terms (e.g., “Confidential”) across the entire file.
- **Cross‑sheet data association:** Find a project number or customer name that appears on multiple sheets.
- **Template verification:** After generating reports, confirm that placeholders such as `{{Date}}` have been replaced.
- **Historical data mining:** Search for specific event codes in legacy spreadsheets to understand past business logic.

## Why should you use the Search content within the worksheet of the Spreadsheet API?

- **Developer‑friendly:** SDKs for many languages accelerate development and are fully documented.
- **Reduced labor costs:** Decreases the need for staff dedicated to manual data consolidation.
- **Pay‑per‑use:** You only pay for the API calls you actually make.
- **Zero maintenance:** No servers to manage, no software updates, and no compatibility concerns.
- **Preserves complex Excel formatting** when exporting results to PDF or other formats.

## How to Use the Search for broken links within the worksheet of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search content within worksheets of spreadsheets for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.