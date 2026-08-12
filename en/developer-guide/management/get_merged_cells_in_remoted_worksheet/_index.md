---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Get Merged Cells In Remote Worksheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Get Merged Cells In Remote Worksheet"
type: docs
url: /cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, Get Merged Cells, Remote Worksheet, API"
description: "Retrieves all merged cell areas from a remote worksheet in a spreadsheet."
weight: 10
---

## The GetMergedCellsInRemotedWorksheet of Aspose.Cells Cloud Web Services

Get all merged cell area form a remote spreadsheet worksheet.

### Web API Endpoint

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| name | string | Path | Spreadsheet name |
| worksheet | string | Path | Worksheet name |
| folder | string | Query | The cloud storage path of the spreadsheet. |
| storageName | string | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | string | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | string | Query | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| — | — | *None* |

### **Response**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The request succeeded and the list of merged cell areas is returned. |
| 400 | Bad Request | Invalid URL or malformed request parameters. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 413 | Payload Too Large | The request payload exceeds the allowed size. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## How to Use the GetMergedCellsInRemotedWorksheet with SDKs

### GetMergedCellsInRemotedWorksheet Specification

The [GetMergedCellsInRemotedWorksheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`