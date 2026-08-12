---
title: "Get Worksheets With Local Spreadsheet"
ArticleTitle: "Get Worksheets With Local Spreadsheet – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Get Worksheets With Local Spreadsheet"
type: docs
url: /cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, Worksheets, Local Spreadsheet, API"
description: "Fetches a complete list of worksheets from the currently active local spreadsheet."
weight: 1000
---

## The Get Worksheets With Local Spreadsheet of Aspose.Cells Cloud Web Services

This endpoint accesses the local spreadsheet application (e.g., Excel) via interop or a local API, collects the name and type (e.g., standard, chart, macro) of every worksheet, and returns the collection as a structured JSON array. It is typically used to populate a worksheet selector UI or to audit spreadsheet contents.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | File   | FormData (HTTP Body)        | Upload spreadsheet file. |
| region         | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. *(optional)* |
| password       | String | Query                       | The password for opening spreadsheet file. *(optional)* |

### Request Body Parameter

| Parameter Name | Type | Description |
|----------------|------|-------------|
| Spreadsheet    | File | Upload spreadsheet file. |

### **Response**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... additional worksheets
  ]
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The list of worksheets was retrieved successfully. |
| 400 | Bad Request | Invalid request (e.g., malformed URL or missing required data). |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## How to Use the Get Worksheets With Local Spreadsheet with SDKs

### Get Worksheets With Local Spreadsheet Specification

The [Get Worksheets With Local Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Chart1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... additional worksheets
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells Cloud web services using various SDKs:
`[TBD]`