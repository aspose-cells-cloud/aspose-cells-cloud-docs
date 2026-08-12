---
title: "Remove Characters By Position"
ArticleTitle: "Remove Characters By Position – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Remove Characters By Position"
type: docs
url: /cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Remove Characters, API"
description: "Deletes characters from cells by position in a spreadsheet."
weight: 100
---

## The Remove Characters By Position of Aspose.Cells Cloud Web Services

Deletes characters from every cell in the target range by position (first/last N, before/after a substring, or between two delimiters) while preserving formulas, formatting and data‑validation.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name            | Type    | Path/Query String/HTTP Body | Description                                                                                                          |
|---------------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | File    | FormData                    | Upload spreadsheet file.                                                                                            |
| theFirstNCharacters       | Integer | Query                       | Specify removing the first n characters from selected cells. Optional.                                               |
| theLastNCharacters        | Integer | Query                       | Specify removing the last n characters from selected cells. Optional.                                                |
| allCharactersBeforeText   | String  | Query                       | Delete text located before a specified substring. Optional.                                                          |
| allCharactersAfterText    | String  | Query                       | Delete text located after a specified substring. Optional.                                                           |
| caseSensitive             | Boolean | Query                       | Affects `Substring` mode and `CustomChars` when enabled. Optional.                                                   |
| worksheet                 | String  | Query                       | Specify the worksheet of spreadsheet. Optional.                                                                      |
| range                     | String  | Query                       | Specify the worksheet range of spreadsheet (e.g., `A1:B10`). Optional.                                               |
| outPath                   | String  | Query                       | (Optional) The folder path where the workbook is stored. Default is null. Optional.                                 |
| outStorageName            | String  | Query                       | Output file Storage Name. Optional.                                                                                  |
| region                    | String  | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Optional.                                             |
| password                  | String  | Query                       | The password for opening spreadsheet file. Optional.                                                                 |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Upload spreadsheet file. |

### **Response**

```json
{
  "status": "OK",
  "message": "Characters removed successfully.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The operation completed successfully and the processed file is returned. |
| 400 | Bad Request | The request is malformed or contains invalid parameters. |
| 401 | Unauthorized | Authentication failed or JWT token is missing/invalid. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | An unexpected error occurred on the server side. |

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
`[TBD]`