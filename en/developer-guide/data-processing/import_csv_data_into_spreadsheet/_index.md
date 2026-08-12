---
title: "Import CSV Data Into Spreadsheet"
ArticleTitle: "Import CSV Data Into Spreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Import CSV Data Into Spreadsheet"
type: docs
url: /cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, CSV import, spreadsheet, API"
description: "Import CSV data file into the local spreadsheet using Aspose.Cells Cloud API."
weight: 100
---

## The Import CSV Data Into Spreadsheet of Aspose.Cells Cloud Web Services

Import CSV data file into the local spreadsheet. The method parses the CSV, maps the data to the spreadsheet's cell structure, and saves the file locally. Supported spreadsheet formats include .xlsx and .ods.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name        | Type    | Path/Query String/HTTP Body | Description                                                                                                                          |
|-----------------------|---------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile              | File    | FormData                    | Upload data file.                                                                                                                    |
| Spreadsheet           | File    | FormData                    | Upload spreadsheet file.                                                                                                             |
| worksheet             | String  | Query                       | Need to import CSV data into the worksheet. (required)                                                                              |
| startcell             | String  | Query                       | Starting position for data import. (required)                                                                                       |
| insert                | Boolean | Query                       | Controls the insertion behavior. true: inserts data; false: overwrites existing data. Default: true (optional)                     |
| convertNumericData    | Boolean | Query                       | Whether the string in text file is converted to numeric data. Default: true (optional)                                            |
| splitter              | String  | Query                       | Delimiter used to split CSV fields. Default: "," (optional)                                                                         |
| outPath               | String  | Query                       | (Optional) The folder path where the workbook is stored. The default is null (optional).                                            |
| outStorageName        | String  | Query                       | Output file Storage Name. (optional)                                                                                                |
| fontsLocation         | String  | Query                       | Use Custom fonts. (optional)                                                                                                         |
| region                | String  | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. (optional) |
| password              | String  | Query                       | The password for opening spreadsheet file. (optional)                                                                              |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Response**

```json
{
  "file": "<binary stream of the resulting spreadsheet>"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | CSV data imported successfully and the resulting spreadsheet file is returned. |
| 400 | Bad Request | Invalid request parameters or malformed URL. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded files exceed the allowed size limit. |
| 500 | Internal Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

## How to Use the Import CSV Data Into Spreadsheet with SDKs

### Import CSV Data Into Spreadsheet Specification

The [Import CSV Data Into Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Sheet1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@sample.csv" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binary stream of the resulting spreadsheet>"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
 `[TBD]`