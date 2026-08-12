---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /cells/{name}/search/content/all-textitems
aliases: []
keywords: "search, text items, Aspose.Cells"
description: "Search all text items in a remote spreadsheet using Aspose.Cells Cloud."
weight: 100
---

## The SearchAllTextItemsInRemoteSpreadsheet of Aspose.Cells Cloud Web Services

This method searches for all text items within a remote spreadsheet file. It supports searching through all sheets and cells of the workbook, identifying occurrences of the search term. The operation is performed in the cloud, requiring no local storage. Ensure that you have the necessary permissions to read the source file. If the source file cannot be accessed or if an error occurs during the search process (such as an unsupported file format), an appropriate exception will be thrown. The method may return the locations of the matches (e.g., sheet name, cell coordinates) depending on implementation details.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| name           | string | Path                        | The name of the workbook file. |
| folder         | string | Query                       | The folder path where the workbook is stored. |
| storageName    | string | Query                       | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region         | string | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | string | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| [TBD]          |      | [TBD] |

### **Response**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The request succeeded and the response contains all text items found in the spreadsheet. |
| 400 | Bad Request | Invalid URL or request parameters. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The request payload exceeds the allowed size. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## How to Use the SearchAllTextItemsInRemoteSpreadsheet with SDKs

### SearchAllTextItemsInRemoteSpreadsheet Specification

The [SearchAllTextItemsInRemoteSpreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Sheet1",
      "CellAddress": "A1",
      "Text": "Sample text"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`