---
title: "Import JSON Data Into Spreadsheet"
ArticleTitle: "Import JSON Data Into Spreadsheet – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Import JSON Data Into Spreadsheet"
type: docs
url: /import/data/json
aliases: []
keywords: "Import JSON, Aspose.Cells, Spreadsheet, API"
description: "Import JSON data file into the local spreadsheet."
weight: 100
---
The **ImportJSONDataIntoSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/import/data/json`) in Aspose.Cells Cloud enables developers to import JSON data directly into a specified worksheet of an existing spreadsheet file by parsing the JSON and mapping it to cell values starting at a given position; it supports formats like .xlsx and .ods and allows control over whether data is inserted or overwrites existing content via the `insert` parameter.

## The Import JSONData Into Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| datafile | File | FormData | Upload data file. |
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | Need to import JSON data into the worksheet. |
| startcell | String | Query | Starting position for data import |
| insert | Boolean | Query | Controls the insertion behavior. true: inserts data; false: overwrites existing data. |
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
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

**Response Status Codes**

Import JSON data file into the local spreadsheet. The method parses the JSON, maps the data to the spreadsheet's cell structure, and saves the file locally. Supported spreadsheet formats include .xlsx and .ods.

## How to Use the Import JSON Data Into Spreadsheet with SDKs

### Import JSON Data Into Spreadsheet Specification

The [Import JSON Data Into Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```

{< /tab >}
{< tab tabNum="2" >}

```json
{
  "file": "binary stream"
}
```

{< /tab >}
{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
