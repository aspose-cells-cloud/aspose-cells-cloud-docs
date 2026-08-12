---
title: "Remove Duplicate Substrings In Remote Spreadsheet"
ArticleTitle: "Remove Duplicate Substrings In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Remove Duplicate Substrings In Remote Spreadsheet"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, Remove Duplicate Substrings, API"
description: "API to find and remove repeated substrings inside cells of a specified range in a workbook."
weight: 1
---

## The Remove Duplicate Substrings In Remote Spreadsheet of Aspose.Cells Cloud Web Services

Finds and removes repeated substrings inside every cell of the chosen range, using user‑defined or preset delimiters, while preserving formulas, formatting and data‑validation.

**How duplicates are detected**  
1. Each cell value is split into substrings by the chosen delimiter(s).  
2. The tool compares substrings **within the same cell** and keeps only the **first occurrence** of each duplicate.  
3. Cleaned substrings are re‑joined with the same delimiter(s) and written back to the cell.  

**Delimiter options**  
- Preset list: comma, semicolon, space, tab, line‑break  
- `Custom` – enter any character(s); multiple characters are treated as one composite delimiter  
- `TreatConsecutiveDelimitersAsOne` – collapse adjacent delimiters into a single separator  

Only string‑type cells are processed; numbers, booleans and formulas are converted to string before splitting (formulas are dropped). Returns the count of cleaned cells and the updated workbook stream.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTP Body | Description |
|----------------|---------|-----------------------------|-------------|
| name | string | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet | string | Path | Specify the worksheet of spreadsheet. |
| range | string | Path | Specify the worksheet range of spreadsheet. |
| delimiters | string | Query | Delimiters used to split cell values (e.g., comma, semicolon, space, tab, line‑break). Required. |
| treatConsecutiveDelimitersAsOne | boolean | Query | Collapse adjacent delimiters into a single separator. Default: true. Optional. |
| caseSensitive | boolean | Query | Perform case‑sensitive comparison when detecting duplicates. Optional. |
| folder | string | Query | (Optional) The folder path where the workbook is stored. Default: null. |
| storageName | string | Query | (Optional) The name of the storage if using custom cloud storage. |
| region | string | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Optional. |
| password | string | Query | The password for opening spreadsheet file. Optional. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| - | - | No request body is required for this operation. |

### **Response**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-encoded workbook stream"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Operation succeeded; returns the count of cleaned cells and the updated workbook stream. |
| 400 | Bad Request | One or more request parameters are missing or invalid. |
| 401 | Unauthorized | Authentication failed or JWT token is missing/invalid. |
| 413 | Payload Too Large | The request exceeds the allowed size limits. |
| 500 | Internal Server Error | An unexpected error occurred on the server. |

## How to Use the Remove Duplicate Substrings In Remote Spreadsheet with SDKs

### Remove Duplicate Substrings In Remote Spreadsheet Specification

The [Remove Duplicate Substrings In Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-encoded workbook stream"
}
```
{< /tab >}
{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`