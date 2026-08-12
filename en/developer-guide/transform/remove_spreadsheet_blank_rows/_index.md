---
title: "Remove Spreadsheet Blank Rows"
ArticleTitle: "Remove Spreadsheet Blank Rows – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Remove Spreadsheet Blank Rows"
type: docs
url: /cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, remove blank rows, spreadsheet, API"
description: "Deletes all blank rows from a spreadsheet file."
weight: 100
---

## The Remove Spreadsheet Blank Rows of Aspose.Cells Cloud Web Services

This method removes rows from a spreadsheet that are completely empty, containing no data or objects. It scans through all sheets and identifies rows where every cell is empty. The operation is performed directly on the spreadsheet, ensuring that only rows with no content are deleted. This helps in cleaning up the spreadsheet and removing unnecessary blank rows, making the data more organized and easier to manage. Users should ensure that the spreadsheet is backed up before performing this operation, as deleted rows cannot be recovered.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | File   | FormData                    | Upload spreadsheet file. |
| outPath        | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query                       | Output file Storage Name. |
| region         | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Upload spreadsheet file. |

### **Response**

```json
{
  "ResponseFile": "binary file stream"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The processed spreadsheet file with blank rows removed is returned. |
| 400 | Bad Request | Invalid URL or request parameters. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | Request payload exceeds allowed size. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## How to Use the Remove Spreadsheet Blank Rows with SDKs

### Remove Spreadsheet Blank Rows Specification

The [Remove Spreadsheet Blank Rows API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "binary file stream"
}
```
{< /tab >}
{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`