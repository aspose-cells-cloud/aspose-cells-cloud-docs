---
title: "Remove Characters In Remote Spreadsheet"
ArticleTitle: "Remove Characters In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Remove Characters In Remote Spreadsheet"
type: docs
url: /{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, Remove Characters, Text Processing"
description: "Remove specific characters, symbols, or substrings from a range in a remote Excel file using Aspose.Cells Cloud API"
weight: 100
---
The **RemoveCharactersInRemoteSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters`) in Aspose.Cells Cloud v4.0 deletes user-defined characters, predefined symbol sets (such as NonPrinting, Text, Numeric, Symbols, or Punctuation), or specific substrings from every cell in a named worksheet range while preserving formulas, formatting, and data validation.

## The Remove Characters in Remote Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet | String | Path | Specify the worksheet of spreadsheet. |
| range | String | Path | Specify the worksheet range of spreadsheet. |
| removeTextMethod | String | Query | Specify the removal of text method type. |
| characterSets | String | Query | Specify the character sets. |
| removeCustomValue | String | Query | Specify the remove custom value. |
| caseSensitive | Boolean | Query | Affects `Substring` mode and `CustomChars` when enabled. |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

**Response Status Codes**

Deletes user‑defined characters, predefined symbol sets, or any substring from every cell in the chosen range while preserving formulas, formatting and data‑validation for a remote spreadsheet.

### Request Body Parameter

| Parameter Name | Type   | Description                                     |
| -------------- | ------ | ----------------------------------------------- |
| _None_         | _None_ | This operation does not require a request body. |

## How to Use the Remove Characters In Remote Spreadsheet with SDKs

### Remove Characters In Remote Spreadsheet Specification

The [Remove Characters In Remote Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "Characters removed successfully.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
