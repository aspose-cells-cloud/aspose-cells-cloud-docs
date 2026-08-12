---
title: "Convert Table to CSV"
ArticleTitle: "Convert Table to CSV – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convert Table to CSV"
type: docs
url: /cells/convert/table/csv
aliases: []
keywords: "Convert Table CSV, Aspose.Cells, Cloud API"
description: "Converts a table of spreadsheet on a local drive to the csv file."
weight: 1
---

## The Convert Table to CSV of Aspose.Cells Cloud Web Services

This method reads a spreadsheet file from the local file system, converts its specified table to a CSV file, and returns the converted result. It operates entirely on the cloud server, so no intermediate upload to cloud storage is required. The source file path and target format must be correctly specified, and appropriate permissions are needed to read the source file. Errors such as missing files, inaccessible paths, or conversion failures will result in appropriate exceptions.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | File   | FormData                    | Upload spreadsheet file. |
| worksheet        | String | Query                       | worksheet name of spreadsheet. |
| tableName        | String | Query                       | table name |
| outPath          | String | Query                       | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName   | String | Query                       | Output file Storage Name. |
| fontsLocation    | String | Query                       | Use Custom fonts. |
| AutoRowsFit      | Boolean| Query                       | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit   | Boolean| Query                       | (Optional) Autofits all columns in worksheets. |
| region           | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password         | String | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| *None* | *None* | *No request body is required; the file is sent as multipart/form-data.* |

### **Response**

```json
{
  "file": "binary stream of the generated CSV file"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The table was successfully converted and the CSV file is returned. |
| 400 | Bad Request | Invalid request parameters or malformed URL. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible or does not exist. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The spreadsheet encountered an anomaly during conversion. |

## How to Use the Convert Table to CSV with SDKs

### Convert Table to CSV Specification

The [Convert Table to CSV API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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
  "file": "binary stream of the generated CSV file"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells Cloud web services using various SDKs:
`[TBD]`