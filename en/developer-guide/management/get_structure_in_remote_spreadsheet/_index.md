---
title: "Get Remote Spreadsheet Structure"
ArticleTitle: "Get Structure In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Remote Spreadsheet Structure"
type: docs
url: /{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, spreadsheet, structure"
description: "Retrieve the structural metadata of a remote Excel workbook, including worksheets, tables, pivot tables, charts, shapes, and other core information."
weight: 100
---
The **GetStructureInRemoteSpreadsheet** API (`GET https://api.aspose.cloud/v4.0/cells/{name}/structure`) in Aspose.Cells Cloud retrieves a structured JSON representation of an Excel workbook’s core elements—including metadata, worksheets, tables, pivot tables, charts, and shapes—by converting them into a JObject, enabling efficient data export, API integration, and logging without requiring local file processing.

## The Get Structure in Remote Spreadsheet Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | - |
| folder | String | Query | - |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response

```json
[
  {
    "Name": "String",
    "DataType": {
      "Identifier": "String"
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
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

**Response Status Codes**

### Request Body Parameter

| Parameter Name | Type  | Description |
| -------------- | ----- | ----------- |
| [TBD]          | [TBD] | [TBD]       |

## How to Use the Get Structure in Remote Spreadsheet API with SDKs?

### Get Structure in Remote Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet" rel="noopener noreferrer">Get Structure in Remote Spreadsheet API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
