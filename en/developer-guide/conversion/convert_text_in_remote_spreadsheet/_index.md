---
title: "Convert Text In Remote Spreadsheet"
ArticleTitle: "Convert Text In Remote Spreadsheet – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Convert Text In Remote Spreadsheet"
type: docs
url: /cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, Text Conversion, API"
description: "Converts text in a specified range of a worksheet, including number conversion, character replacement, line break handling, and accented character normalization."
weight: 1000
---

## The Convert Text In Remote Spreadsheet of Aspose.Cells Cloud Web Services

Indicates converting the numbers stored as text into the correct number format, replacing unwanted characters and line breaks with the desired characters, and converting accented characters to their equivalent characters without accents.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description |
|------------------|--------|-----------------------------|-------------|
| name             | string | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet        | string | Path | Specify the worksheet of spreadsheet. |
| range            | string | Path | Specify the worksheet range of spreadsheet. |
| convertTextType  | string | Query | Indicates the conversion of text type. (Required) |
| sourceCharacters | string | Query | Indicates the source characters. (Optional) |
| targetCharacters | string | Query | Indicates the target characters. (Optional) |
| folder           | string | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName      | string | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region           | string | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. (Optional) |
| password         | string | Query | The password for opening spreadsheet file. (Optional) |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| - | - | - |

### **Response**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Text conversion completed successfully.",
  "Data": {
    // Details of the conversion result, such as number of cells updated, can be added here.
  }
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The text conversion operation completed successfully. |
| 400 | Bad Request | The request was malformed or missing required parameters. |
| 401 | Unauthorized | Authentication failed or JWT token is missing/invalid. |
| 413 | Payload Too Large | The request payload exceeds the allowed size limit. |
| 500 | Internal Server Error | An unexpected error occurred on the server. |

## How to Use the Convert Text In Remote Spreadsheet with SDKs

### Convert Text In Remote Spreadsheet Specification

The [Convert Text In Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Text conversion completed successfully.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "Numbers converted, characters replaced, line breaks normalized."
  }
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
 `[TBD]`