---
url: /convert-table-to-json/
title: Convert Excel Table to JSON using Aspose.Cells Cloud API v4.0
linktitle: "Convert Table To Json"
date: 2024-03-15
lastmod: 2024-06-15
summary: Step-by-step guide to convert Excel table data to JSON in one PUT request using Aspose.Cells Cloud API v4.0. Includes cURL, .NET, Java, Python, and Node.js SDK examples.
tags:
  - excel
  - json
  - conversion
  - api
  - cloud
categories:
  - conversion
aliases:
  - /conversion/convert-table-to-json/
weight: 100
type: docs
ArticleTitle: "Convert Excel Table to JSON via Aspose.Cells Cloud API v4.0"
description: "Convert Excel table to JSON via Aspose.Cells Cloud API—no upload required, supports cURL and SDKs."
keywords: "Aspose.Cells Cloud, convert Excel table to JSON, table to JSON API, cloud Excel conversion, Aspose.Cells Cloud API v4.0, convert worksheet table to JSON, JSON export from Excel, cloud table extraction"
---
The **ConvertTableToJson** API (`PUT https://api.aspose.cloud/v4.0/cells/convert/table/json`) in Aspose.Cells Cloud v4.0 converts a specified table from a local spreadsheet file—uploaded directly in the request—into JSON format without requiring prior storage in the cloud, enabling efficient, single-call conversion of local data while avoiding upload and storage overhead.

## The Convert Table to JSON Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### Security and Authentication

All requests require a valid [JWT access token](https://docs.aspose.cloud/total/getting-started/). Obtain your `Client ID` and `Client Secret` from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/), then generate a token using the [OAuth 2.0 flow](https://docs.aspose.cloud/total/getting-started/quickstart/).

> **Note**: Replace `{YOUR_ACCESS_TOKEN}` with your actual JWT token in all examples below.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | worksheet name of spreadsheet. |
| tableName | String | Query | table name |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response

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

Returns a JSON object containing the converted file content:

### **HTTP Status Codes**

| Code  | Meaning               | Description                                                                                     |
| ----- | --------------------- | ----------------------------------------------------------------------------------------------- |
| `200` | OK                    | Conversion successful. Response body contains Base64-encoded JSON.                              |
| `400` | Bad Request           | Missing or invalid parameters (e.g., unsupported file format, missing `worksheet`/`tableName`). |
| `401` | Unauthorized          | Invalid or missing JWT token.                                                                   |
| `404` | Not Found             | Source file inaccessible or table/worksheet not found.                                          |
| `413` | Payload Too Large     | File exceeds 2 GB limit.                                                                        |
| `500` | Internal Server Error | Unexpected server error during conversion.                                                      |

## **How to Use the API**

### **cURL Example**

```bash
# Convert table to JSON and save to local file
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {YOUR_ACCESS_TOKEN}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json

# Convert and save to cloud storage (output folder + storage)
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1&outPath=output&outStorageName=MyStorage" \
  -H "Authorization: Bearer {YOUR_ACCESS_TOKEN}" \
  -F "Spreadsheet=@myWorkbook.xlsx"
```

## How to Use the Convert Table to JSON API with SDKs?

### Convert Table to JSON API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson" rel="noopener noreferrer">Convert Table to JSON API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

The following code snippets demonstrate conversion using Aspose.Cells Cloud SDKs. All examples use the same parameters: `worksheet="Sheet1"`, `tableName="Table1"`.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
