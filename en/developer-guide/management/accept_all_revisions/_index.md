---
title: "Accept All Revisions"
ArticleTitle: "Accept All Revisions – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Accept All Revisions"
type: docs
url: /cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, spreadsheet, revisions"
description: "Accept all revisions in a spreadsheet file using Aspose.Cells Cloud API."
weight: 100
---

## The AcceptAllRevisions of Aspose.Cells Cloud Web Services

Accept all revisions in the uploaded spreadsheet file and return the processed workbook.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | File   | FormData (HTTP Body)        | Upload spreadsheet file. |
| outPath        | string | Query                       | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | string | Query                       | Output file Storage Name. |
| fontsLocation  | string | Query                       | Use Custom fonts. |
| region         | string | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | string | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Upload spreadsheet file. |

### **Response**

```json
{
  "File": "Binary stream of the processed spreadsheet"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The revisions were successfully accepted and the processed file is returned. |
| 400 | Bad Request | The request is invalid (e.g., missing required file or invalid parameters). |
| 401 | Unauthorized | Authentication failed or JWT token is missing/invalid. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | An unexpected error occurred on the server. |

## How to Use the AcceptAllRevisions with SDKs

### AcceptAllRevisions Specification

The [AcceptAllRevisions API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=en-US&password=12345" \
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
  "File": "Binary stream of the processed spreadsheet"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="[TBD]" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
 `[TBD]`