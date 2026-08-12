---
title: "Convert Chart to PDF"
ArticleTitle: "Convert Chart to PDF – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "ConvertChartToPdf"
type: docs
url: /cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, chart conversion"
description: "Converts a chart of spreadsheet on a local drive to pdf."
weight: 100
---

## The Convert Chart to PDF of Aspose.Cells Cloud Web Services

This method reads a chart from a spreadsheet file supplied via a local file upload, converts it into PDF format, and returns the converted result. It operates entirely on the cloud server, so no intermediate storage is required. The source file path and target format must be correct, and appropriate permissions are needed to read the source file. Errors such as missing files, access issues, or conversion failures will result in appropriate HTTP error responses.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | File   | FormData                    | Upload spreadsheet file. |
| worksheet        | String | Query                       | Worksheet name of spreadsheet. |
| chartIndex       | Integer| Query                       | Chart index of worksheet. |
| outPath          | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName   | String | Query                       | Output file Storage Name. |
| fontsLocation    | String | Query                       | Use Custom fonts. |
| region           | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password         | String | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Upload spreadsheet file. |

### **Response**

```json
{
  "ResponseFile": "binary PDF file stream"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Chart successfully converted to PDF; binary PDF file returned. |
| 400 | Bad Request | Invalid request parameters or malformed URL. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | Uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | An error occurred while processing the conversion. |

## How to Use the Convert Chart to PDF with SDKs

### Convert Chart to PDF Specification

The [Convert Chart to PDF API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "binary PDF file stream"
}
```
{< /tab >}
{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`