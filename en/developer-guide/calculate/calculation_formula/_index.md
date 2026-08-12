---
title: "Calculate Formula"
ArticleTitle: "Calculate Formula – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Calculate Formula"
type: docs
url: /cells/calculate/formula
aliases: []
keywords: "Aspose Cells, calculate formula, spreadsheet, API"
description: "Calculate formula in a spreadsheet using Aspose.Cells Cloud API."
weight: 100
---

## The Calculate Formula of Aspose.Cells Cloud Web Services

Calculates a specified formula in a given worksheet of an uploaded spreadsheet file and returns the resulting spreadsheet as a file stream. This operation supports locale‑specific processing via the **region** parameter and can open password‑protected files.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Path/Query String/HTTP Body | Description |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | File   | FormData                    | Upload spreadsheet file. |
| worksheet      | String | Query                       | Name of the worksheet that contains the formula. |
| formula        | String | Query                       | The formula to be calculated (e.g., `=SUM(A1:B2)`). |
| region         | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password       | String | Query                       | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Response**

```json
{
  "File": "<binary stream of the resulting spreadsheet>"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Calculation succeeded; the resulting spreadsheet file is returned. |
| 400 | Bad Request | One or more request parameters are missing or invalid. |
| 401 | Unauthorized | Authentication failed or JWT token is missing/invalid. |
| 413 | Payload Too Large | Uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | An unexpected error occurred on the server. |

## How to Use the Calculate Formula with SDKs

### Calculate Formula Specification

The [Calculate Formula API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "<binary stream of the resulting spreadsheet>"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
 `[TBD]`