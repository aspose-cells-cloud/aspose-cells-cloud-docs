---
title: "Calculate Formula"
ArticleTitle: "Calculate Formula – Aspose.Cells Cloud API"
second_title: "Developer Guide"
linktitle: "Calculate Formula"
type: docs
url: /calculate/formula
aliases: []
keywords: "Aspose Cells, calculate formula, spreadsheet, API"
description: "Calculate formula in a spreadsheet using Aspose.Cells Cloud API."
weight: 100
---
The **CalculationFormula** API (`PUT https://api.aspose.cloud/v4.0/cells/calculate/formula`) in Aspose.Cells Cloud enables developers to compute the value of a specified formula within a given worksheet of an uploaded spreadsheet file, returning the updated workbook as a downloadable file stream; it supports locale-specific calculations via the optional `region` parameter and can process password-protected files using the `password` query parameter.

## The Calculation Formula Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | - |
| formula | String | Query | - |
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

Calculates a specified formula in a given worksheet of an uploaded spreadsheet file and returns the resulting spreadsheet as a file stream. This operation supports locale‑specific processing via the **region** parameter and can open password‑protected files.

### Request Body Parameter

| Parameter Name | Type  | Description |
| -------------- | ----- | ----------- |
| [TBD]          | [TBD] | [TBD]       |

## How to Use the Calculate Formula with SDKs

### Calculate Formula Specification

The [Calculate Formula API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<binary stream of the resulting spreadsheet>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
