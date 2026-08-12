---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "TransposeData"
type: docs
url: /cells/transpose
aliases: ["/cells/transpose"]
keywords: "TransposeData, Aspose.Cells, Cloud API, spreadsheet, transpose"
description: "Switch rows and columns in the spreadsheet."
weight: 1000
---

## The TransposeData of Aspose.Cells Cloud Web Services

Switch rows and columns in the spreadsheet.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description                                                                                                                            |
|------------------|--------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                    | Upload spreadsheet file.                                                                                                               |
| worksheet        | String | Query                       | The worksheet name.                                                                                                                    |
| cellArea         | String | Query                       | A specified data range.                                                                                                                |
| outPath          | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                          |
| outStorageName   | String | Query                       | Output file Storage Name.                                                                                                              |
| region           | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password         | String | Query                       | The password for opening spreadsheet file.                                                                                             |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| [TBD]          | [TBD]| [TBD]       |

### **Response**

```json
{
  "file": "binary stream of the transposed spreadsheet"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The transposed spreadsheet file is returned. |
| 400 | Bad Request | Invalid input parameters or malformed request. |
| 401 | Unauthorized | Authentication failed or JWT token missing/invalid. |
| 413 | Payload Too Large | Uploaded file exceeds allowed size limit. |
| 500 | Internal Server Error | Unexpected server error. |

## How to Use the TransposeData with SDKs

### TransposeData Specification

The [TransposeData API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
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
  "file": "binary stream of the transposed spreadsheet"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`