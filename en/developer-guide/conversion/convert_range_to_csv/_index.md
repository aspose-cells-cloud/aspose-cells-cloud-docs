---
title: "Convert Range to CSV"
ArticleTitle: "Convert Range to CSV – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convert Range to CSV"
type: docs
url: /cells/convert/range/csv
aliases: []
keywords: "convert, csv, range, Aspose.Cells"
description: "Converts a range of spreadsheet on a local drive to the csv file."
weight: 1
---

## The Convert Range to CSV of Aspose.Cells Cloud Web Services

This operation reads a spreadsheet file from the local file system, converts a specified range to CSV format, and returns the converted result directly. It works entirely on the cloud server, so no intermediate upload to cloud storage is required. The API supports optional parameters such as custom fonts, auto‑fit rows/columns, locale settings, and password‑protected workbooks.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type    | Path/Query String/HTTP Body | Description                                                                                                                            |
|------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                    | Upload spreadsheet file.                                                                                                               |
| worksheet        | String  | Query                       | Worksheet name of spreadsheet. **Required**.                                                                                           |
| range            | String  | Query                       | Cell area. e.g. `A1:C10`. **Required**.                                                                                                 |
| outPath          | String  | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                          |
| outStorageName   | String  | Query                       | Output file Storage Name.                                                                                                              |
| fontsLocation    | String  | Query                       | Use Custom fonts.                                                                                                                      |
| AutoRowsFit      | Boolean | Query                       | (Optional) Autofits all rows in worksheets.                                                                                            |
| AutoColumnsFit   | Boolean | Query                       | (Optional) Autofits all columns in worksheets.                                                                                         |
| region           | String  | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password         | String  | Query                       | The password for opening spreadsheet file.                                                                                             |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| None | N/A | No request body parameters. |

### **Response**

```json
{
  "ResponseFile": "binary file stream (CSV content)"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The range was successfully converted and the CSV file is returned in the response body. |
| 400 | Bad Request | Invalid URL or missing required parameters. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 413 | Payload Too Large | The request payload exceeds the allowed size limit. |
| 500 | Internal Server Error | The spreadsheet encountered an anomaly while obtaining conversion data. |

## How to Use the Convert Range to CSV with SDKs

### Convert Range to CSV Specification

The [Convert Range to CSV API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "Base64EncodedCsvContent"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low‑level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
`[TBD]`