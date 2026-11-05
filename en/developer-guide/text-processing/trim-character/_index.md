---
url: /trim-character/
title: "Aspose.Cells Cloud Trim Character API - Clean Excel Cell Data"
linktitle: Trim Character
description: "Remove extra spaces, line breaks, and non-breaking spaces from Excel cells using Aspose.Cells Cloud TrimCharacter API."
keywords: "excel, text-trimming, aspose.cells, cloud-api, data-cleaning"
type: docs
weight: 100
ArticleTitle: "Aspose.Cells Cloud TrimCharacter API: Clean Excel Cell Text & Spaces"
---
The **TrimCharacter** API (`PUT https://api.aspose.cloud/v4.0/cells/content/trim`) in Aspose.Cells Cloud enables programmatic cleaning of spreadsheet content by removing unnecessary spaces, line breaks, and special characters such as non-breaking spaces. Using this RESTful endpoint, developers can trim leading and trailing whitespace, collapse multiple spaces between words into a single space, and eliminate extra or all line breaks to ensure data consistency, readability, and professional formatting in Excel files uploaded via form-data.

## Overview

The TrimCharacter API provides precise control over text formatting cleanup, supporting:

- **Leading/trailing whitespace removal**  
  Eliminate extra spaces at the start and end of cell values for consistent appearance.

- **Multiple space normalization**  
  Reduce consecutive spaces between words to a single space.

- **Non-breaking space handling**  
  Remove Unicode U+00A0 characters that resist standard `TRIM()` functions.

- **Line break management**  
  Selectively remove extra or all line breaks within cells.

- **Targeted scope control**  
  Apply trimming to a specific worksheet, range (e.g., `"A1:C10"`), or entire workbook.

This API is ideal for cleaning user inputs, customer data, report sources, and pre-migration datasets.

## The Trim Character Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### Authentication

All requests require a valid JWT access token with the **Cells** scope. Authenticate using your `client_id` and `client_secret` as described in the [REST API Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

Include the token in the `Authorization` header:

```http
Authorization: Bearer {access_token}
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| trimContent | String | Query | Specify the trim content. |
| trimLeading | Boolean | Query | Specify to trim content from the beginning. |
| trimTrailing | Boolean | Query | Specify to trim content from the end. |
| trimSpaceBetweenWordTo1 | Boolean | Query | Remove excess spaces between words within a cell. |
| trimNonBreakingSpaces | Boolean | Query | Remove non-breaking spaces. |
| removeExtraLineBreaks | Boolean | Query | Remove extra line breaks. |
| removeAllLineBreaks | Boolean | Query | Remove all line breaks. |
| worksheet | String | Query | Specify the worksheet of spreadsheet. |
| range | String | Query | Specify the worksheet range of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

> **Best Practice**: Set `trimLeading` and `trimTrailing` explicitly to avoid unintended behavior when `trimContent` is customized.

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

> **Note**: This documentation applies to Aspose.Cells Cloud API v4.0. For migration guidance to v5.0, see [Aspose.Cells Cloud API Versioning](/cells/working-with-api-versions/).

## Example Request

```bash
curl -X PUT \
  'https://api.aspose.cloud/v4.0/cells/content/trim?trimContent=%20&trimLeading=true&trimTrailing=true&trimSpaceBetweenWordTo1=true&removeAllLineBreaks=true' \
  -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...' \
  -H 'Content-Type: multipart/form-data' \
  -F 'Spreadsheet=@"input.xlsx"'
```

## Response

**Success (HTTP 200)**: Returns a file stream containing the trimmed workbook.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

## Error Codes

| Code  | Description                                                              |
| ----- | ------------------------------------------------------------------------ |
| `400` | Invalid request (e.g., malformed parameters or unsupported file format). |
| `401` | Invalid or expired access token.                                         |
| `403` | Insufficient permissions for the requested operation.                    |
| `404` | Spreadsheet file not found or inaccessible.                              |
| `500` | Internal server error during processing.                                 |

## Use Cases

- **User Input Normalization**: Clean free-text entries in forms or surveys before storage.
- **Customer Data Maintenance**: Standardize names, addresses, and contact fields.
- **Report Automation**: Preprocess data sources to eliminate formatting artifacts.
- **Data Migration**: Normalize legacy spreadsheets before loading into new systems.

## Benefits

- **No Infrastructure Overhead**: Fully managed cloud service—no servers to maintain.
- **Pay-as-you-go Pricing**: Only billed for API calls and storage used.
- **Multi-Format Support**: Process XLSX, XLS, ODS, CSV, and more.
- **Developer-Friendly**: Official SDKs for [C#](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet), [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java), [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python), [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node), [PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php), [Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby), [Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl), and [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

## Related Resources

- [Authentication Guide](/total/working-with-authentication/)
- [Cell Formatting API](/cells/text/format-text-in-excel/)
- [Find & Replace Text](/cells/text/find-and-replace-text-in-excel/)
- [SDK Documentation Hub](https://github.com/aspose-cells-cloud)

## Changelog

| Date       | Version | Changes                                                       |
| ---------- | ------- | ------------------------------------------------------------- |
| 2024-04-18 | v4.0    | Initial published documentation with full parameter coverage. |

---

> **Tip**: For large-scale data cleaning, combine TrimCharacter with [Batch Processing](/cells/batch-process-spreadsheets/) and [Webhook Notifications](/cells/working-with-webhooks/) for end-to-end automation.

## How to Use the Trim Character API with SDKs?

### Trim Character API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter" rel="noopener noreferrer">Trim Character API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
