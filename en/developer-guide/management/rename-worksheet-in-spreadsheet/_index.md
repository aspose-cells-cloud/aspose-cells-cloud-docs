---
title: Rename Worksheet in Excel – Aspose.Cells Cloud API
linktitle: Rename Worksheet
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "rename worksheet, Aspose.Cells Cloud, Excel API, spreadsheet SDK, REST API"
description: "Rename Excel worksheets programmatically using Aspose.Cells Cloud API. Includes cURL, C#, Java, Python, and SDK examples. Supports password-protected files, regional settings, and cloud storage integration."
date: 2023-11-15
lastmod: 2024-05-22
weight: 100
ArticleTitle: "Rename Worksheet in Excel with Aspose.Cells Cloud API"
---
The **RenameWorksheetInSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet`), part of Aspose.Cells Cloud v4.0, enables users to rename a specified worksheet within a workbook by submitting the current and new sheet names alongside the spreadsheet file in a single request. This RESTful operation supports dynamic workbook reorganization, improving structure and readability—ideal for report standardization, ETL workflows, and multilingual content delivery without manual intervention.

## The Rename Worksheet in Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| sourceName | String | Query | The current name of the worksheet to be renamed. |
| targetName | String | Query | The new name for the worksheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

> **Note:** Excel worksheet names are limited to 31 characters and cannot include `:`, `\`, `?`, `*`, `[`, or `]`.

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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

A successful request returns the modified workbook as a file stream. The response header includes `Content-Type: application/octet-stream`.

**Endpoint:**  
`PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet`

### cURL Example

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

> **Tip:** Replace `{access_token}` with your valid JWT token. Learn more about [authentication](/authentication/).

## Use Cases

### Report Generation & Brand Standardization

Automatically rename generic worksheet tabs (e.g., `Sheet1`) to client-specific names (e.g., `AcmeCorp_Q1_Summary`) for professional report delivery.

### ETL Workflow Standardization

Rename extracted or transformed worksheets to consistent names (e.g., `Raw_Data`, `Cleaned_Data`) for downstream analysis pipelines.

### Multilingual Content Delivery

Localize worksheet names based on user locale (e.g., `数据` for Chinese, `Données` for French) before distribution.

## Why Use Aspose.Cells Cloud API?

- **Official SDKs**: Full support for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go ([SDK Overview](/sdks/)).
- **No Server Maintenance**: Fully managed cloud service—no infrastructure to host or update.
- **Secure & Compliant**: JWT-based authentication ([learn more](/authentication/)) and GDPR-ready data handling.
- **Cost-Efficient**: Pay-per-use pricing—no upfront licensing fees.

## How to Use the Rename Worksheet in Spreadsheet API with SDKs?

### Rename Worksheet in Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/RenameWorksheetInSpreadsheet" rel="noopener noreferrer">Rename Worksheet in Spreadsheet API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
