---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Get Structure In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "GetStructureInRemoteSpreadsheet"
type: docs
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, spreadsheet, structure"
description: "Retrieve the structural metadata of a remote Excel workbook, including worksheets, tables, pivot tables, charts, shapes, and other core information."
weight: 100
---

## The Get Structure In Remote Spreadsheet of Aspose.Cells Cloud Web Services

Structurally convert the core metadata, worksheets, tables, pivot tables, charts, shapes, and other information of an Excel workbook into a JObject type JSON object, for scenarios such as data export, API responses, and log recording.

### Web API Endpoint

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
|----------------|------|-----------------------------|-------------|
| name | string | Path | Name of the spreadsheet file. |
| folder | string | Query | Folder where the file is located. (Optional) |
| storageName | string | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | string | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | string | Query | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Response**

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Successfully retrieved workbook structure. |
| 400 | Bad Request | Invalid request parameters. |
| 401 | Unauthorized | Authentication failed or token missing. |
| 413 | Payload Too Large | The request payload exceeds the allowed size. |
| 500 | Internal Server Error | Unexpected server error. |

## How to Use the Get Structure In Remote Spreadsheet with SDKs

### Get Structure In Remote Spreadsheet Specification

The [Get Structure In Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Sheet1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Quarterly Sales",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`