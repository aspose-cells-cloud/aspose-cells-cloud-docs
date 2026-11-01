---
title: "Remove Characters By Position"
ArticleTitle: "Remove Characters By Position – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Remove Characters By Position"
type: docs
url: /content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Remove Characters, API"
description: "Deletes characters from cells by position in a spreadsheet."
weight: 100
---
The **RemoveCharactersByPosition** API (`PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position`) in Aspose.Cells Cloud enables precise, position-based character removal from spreadsheet cells—such as stripping the first or last N characters, deleting text before or after a substring, or extracting content between delimiters—while preserving formulas, formatting, and data validation rules.

## The Remove Characters by Position Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| theFirstNCharacters | Integer | Query | Specify removing the first n characters from selected cells. |
| theLastNCharacters | Integer | Query | Specify removing the last n characters from selected cells. |
| allCharactersBeforeText | String | Query | Specify using targeted removal options to delete text that is located before certain characters. |
| allCharactersAfterText | String | Query | Specify using targeted removal options to delete text that is located after certain characters. |
| caseSensitive | Boolean | Query | Affects `Substring` mode and `CustomChars` when enabled. |
| worksheet | String | Query | Specify the worksheet of spreadsheet. |
| range | String | Query | Specify the worksheet range of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
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
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

**Response Status Codes**

Deletes characters from every cell in the target range by position (first/last N, before/after a substring, or between two delimiters) while preserving formulas, formatting and data‑validation.

### Request Body Parameter

| Parameter Name | Type | Description              |
| -------------- | ---- | ------------------------ |
| Spreadsheet    | File | Upload spreadsheet file. |

## How to Use the Remove Characters By Position with SDKs

### Remove Characters By Position Specification

The [Remove Characters By Position API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "Characters removed successfully.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
