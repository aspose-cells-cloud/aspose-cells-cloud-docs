---
title: "SearchBrokenLinksInRemoteWorksheet"
ArticleTitle: "Search Broken Links in Remote Worksheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "SearchBrokenLinksInRemoteWorksheet"
type: docs
url: /cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, Search Broken Links, Remote Worksheet"
description: "Search broken links in the worksheet of a remote spreadsheet."
weight: 100
---

## The Search Broken Links in Remote Worksheet of Aspose.Cells Cloud Web Services

This method searches for broken links within a worksheet of a spreadsheet file stored in remote cloud storage. It scans all sheets and cells to identify hyperlinks that no longer point to valid destinations, such as dead URLs or missing external references. The operation is performed remotely within the cloud environment, without requiring the file to be downloaded to the local machine.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
|----------------|------|-----------------------------|-------------|
| name | string | Path | The name of the workbook file to be search. |
| worksheet | string | Path | Specify the worksheet for the lookup. |
| folder | string | Query | The folder path where the workbook is stored. (optional) |
| storageName | string | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | string | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | string | Query | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| — | — | No request body is required for this operation. |

### **Response**

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Successfully retrieved list of broken links. |
| 400 | Bad Request | Invalid request parameters or malformed URL. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | Request entity is too large. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## How to Use the Search Broken Links in Remote Worksheet with SDKs

### Search Broken Links in Remote Worksheet Specification

The [Search Broken Links in Remote Worksheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Sheet1",
      "CellName": "A1",
      "Url": "http://invalid.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`