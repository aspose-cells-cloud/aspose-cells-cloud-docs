---
title: "Accept All Revisions In Remote Spreadsheet"
ArticleTitle: "Accept All Revisions In Remote Spreadsheet – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Accept All Revisions In Remote Spreadsheet"
type: docs
url: /cells/accept-all-revisions
aliases: ["/cells/accept-all-revisions"]
keywords: "Aspose.Cells, AcceptAllRevisions, Remote Spreadsheet"
description: "Accept all revisions in a remote spreadsheet and return the updated workbook file."
weight: 1000
---

## The Accept All Revisions In Remote Spreadsheet of Aspose.Cells Cloud Web Services

Accepts all tracked changes (revisions) in the specified workbook stored in remote storage. The operation can optionally write the resulting workbook to a different location or storage and returns the updated file as a binary stream.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
|----------------|------|-----------------------------|-------------|
| name | string | Path | The name of the workbook file stored in remote storage. |
| folder | string | Query | (Optional) Folder in the storage where the workbook is located. |
| storageName | string | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | string | Query | (Optional) The folder path where the updated workbook should be saved. The default is null. |
| outStorageName | string | Query | (Optional) Output file storage name. |
| fontsLocation | string | Query | (Optional) Path to custom fonts location. |
| region | string | Query | (Optional) Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | string | Query | (Optional) The password for opening the spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| *None* | *None* | This operation does not require a request body. |

### **Response**

```json
{
  "File": "Binary stream of the updated workbook (e.g., .xlsx) returned as the response body."
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The workbook with all revisions accepted is returned as a binary file stream. |
| 400 | Bad Request | Missing required parameters or invalid request format. |
| 401 | Unauthorized | Invalid or missing JWT token. |
| 413 | Payload Too Large | The request exceeds the allowed size limits. |
| 500 | Internal Server Error | An unexpected error occurred on the server. |

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
 `[TBD]`