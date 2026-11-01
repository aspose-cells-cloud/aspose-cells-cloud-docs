---
title: "Accept All Revisions In Remote Spreadsheet"
ArticleTitle: "Accept All Revisions In Remote Spreadsheet – Aspose.Cells Cloud"
second_title: "Developer Guide"
linktitle: "Accept All Revisions In Remote Spreadsheet"
type: docs
url: /accept-all-revisions
aliases: ["/cells/accept-all-revisions"]
keywords: "Aspose.Cells, AcceptAllRevisions, Remote Spreadsheet"
description: "Accept all revisions in a remote spreadsheet and return the updated workbook file."
weight: 100
---
The **AcceptAllRevisionsInRemoteSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions`) in Aspose.Cells Cloud v4.0 accepts all tracked changes (revisions) in a specified workbook stored in remote storage, optionally saving the updated workbook to a different path or storage and returning the result as a binary stream.

## The Accept All Revisions in Remote Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | - |
| folder | String | Query | - |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
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

Accepts all tracked changes (revisions) in the specified workbook stored in remote storage. The operation can optionally write the resulting workbook to a different location or storage and returns the updated file as a binary stream.

### Request Body Parameter

| Parameter Name | Type   | Description                                     |
| -------------- | ------ | ----------------------------------------------- |
| _None_         | _None_ | This operation does not require a request body. |

## How to Use the Accept All Revisions In Remote Spreadsheet with SDKs

### Accept All Revisions In Remote Spreadsheet Specification

The [Accept All Revisions In Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "Binary stream of the updated workbook (e.g., .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
