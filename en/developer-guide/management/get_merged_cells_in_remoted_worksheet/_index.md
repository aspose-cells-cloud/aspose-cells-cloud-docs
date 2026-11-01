---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Get Merged Cells In Remote Worksheet – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Get Merged Cells In Remote Worksheet"
type: docs
url: /merged-cells-in-remote-worksheet
aliases: []
keywords: "Aspose Cells, Get Merged Cells, Remote Worksheet, API"
description: "Retrieves all merged cell areas from a remote worksheet in a spreadsheet."
weight: 100
---
The **GetMergedCellsInRemotedWorksheet** API (`GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells`) in Aspose.Cells Cloud retrieves all merged cell areas from a specified worksheet of a remote spreadsheet, returning a structured list of cell ranges defined by their top-left and bottom-right coordinates—enabling precise layout analysis, data validation, and integrity checks before further processing.

## The Get Merged Cells in Remoted Worksheet Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | spreadsheet name |
| worksheet | String | Path | worksheet name |
| folder | String | Query | The cloud storage path of the spreadsheet. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### **Response**

```json
[
  {
    "Name": "CellArea[]",
    "DataType": {
      "Identifier": "Array"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

**Response Status Codes**

Get all merged cell area form a remote spreadsheet worksheet.

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| —              | —    | _None_      |

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
