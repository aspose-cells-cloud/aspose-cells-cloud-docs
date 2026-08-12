---
title: "ConvertWorksheetToPdf"
ArticleTitle: "Convert Worksheet to PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, Convert Worksheet to PDF, API"
description: "Converts a worksheet of a spreadsheet file to PDF using Aspose.Cells Cloud."
weight: 10
---

## The ConvertWorksheetToPdf of Aspose.Cells Cloud Web Services

This method reads a spreadsheet file from the local file system, converts its worksheet to a PDF file, and returns the converted result. The source file path and target format must be specified correctly. Ensure that the necessary permissions are in place to read the source file and write the converted file if applicable. The conversion process occurs entirely on the cloud server, eliminating the need for any cloud storage or external downloads.  

Key features include cloud‑native conversion, reduced cloud resource burden, and a simplified workflow.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type    | Path/Query String/HTTP Body | Description                                                                                                                            |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                    | Upload spreadsheet file.                                                                                                               |
| worksheet        | String  | Query                       | worksheet name of spreadsheet.                                                                                                         |
| outPath          | String  | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                          |
| outStorageName   | String  | Query                       | Output file Storage Name.                                                                                                              |
| fontsLocation    | String  | Query                       | Use Custom fonts.                                                                                                                      |
| AutoRowsFit      | Boolean | Query                       | (Optional) Autofits all rows in worksheets.                                                                                           |
| AutoColumnsFit   | Boolean | Query                       | (Optional) Autofits all columns in worksheets.                                                                                        |
| region           | String  | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password         | String  | Query                       | The password for opening spreadsheet file.                                                                                             |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| [TBD]          |      |             |

### **Response**

```json
{
  "file": "<binary stream of the generated PDF>"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Worksheet successfully converted to PDF and returned as a file stream. |
| 400 | Bad Request | Invalid request parameters or malformed URL. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The spreadsheet encountered an anomaly during conversion. |

## How to Use the ConvertWorksheetToPdf with SDKs

### ConvertWorksheetToPdf Specification

The [ConvertWorksheetToPdf API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=SecretPwd" \
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
  "file": "<binary stream of the generated PDF>"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`