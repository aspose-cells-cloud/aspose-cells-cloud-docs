---
title: "Convert Worksheet To Html Table"
ArticleTitle: "Convert Worksheet To Html Table – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "ConvertWorksheetToHtmlTable"
type: docs
url: /cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, HTML Table, API"
description: "Converts a worksheet of a spreadsheet on a local drive to an HTML table file using Aspose.Cells Cloud."
weight: 100
---

## The Convert Worksheet To Html Table of Aspose.Cells Cloud Web Services

This operation reads a spreadsheet file from the local file system, converts its specified worksheet to an HTML table, and returns the converted result as a file stream. The conversion is performed entirely on the cloud server, so no intermediate upload to cloud storage is required. It supports optional locale settings and password‑protected workbooks.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | File   | FormData                    | Upload spreadsheet file. |
| worksheet      | String | Query                       | Worksheet name of spreadsheet. (required) |
| region         | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| *None* | *None* | *No JSON body is required; the file is sent as multipart/form-data.* |

### **Response**

```json
{
  "File": "binary stream of the generated HTML table"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Worksheet successfully converted to HTML table and returned as a file stream. |
| 400 | Bad Request | Invalid request URL or missing required parameters. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 500 | Internal Server Error | The spreadsheet encountered an anomaly while obtaining conversion data. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |

## How to Use the Convert Worksheet To Html Table with SDKs

### Convert Worksheet To Html Table Specification

The [Convert Worksheet To Html Table API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "binary stream of the generated HTML table"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells Cloud web services using various SDKs:
`[TBD]`