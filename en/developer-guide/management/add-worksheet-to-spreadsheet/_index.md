---
title: "Add Worksheet to Excel Workbook — Aspose.Cells Cloud API"
description: "Add Excel worksheet, chart, or macro sheet via Aspose.Cells Cloud API with type, name, and position control"
date: 2024-05-10
lastmod: 2024-06-15
draft: false
url: /add-worksheet-to-spreadsheet/
linktitle: "Add Worksheet to Spreadsheet"
type: docs
keywords: "add worksheet to excel, excel api, aspose.cells cloud, insert sheet, spreadsheet automation, chart sheet, macro sheet, REST API"
weight: 100
ArticleTitle: "Add Worksheet to Excel Workbook with Aspose.Cells Cloud REST API"
---
The **AddWorksheetToSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet`) enables users to add a new worksheet, chart sheet, or macro sheet to an Excel workbook via the Aspose.Cells Cloud REST API by specifying the worksheet type, insertion position, and name; it supports dynamic workbook structuring for automated reporting, template generation, and audit workflows, and accepts a spreadsheet file upload along with optional query parameters for fine-grained control.

## The Add Worksheet to Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| sheetType | String | Query | Specifies the name of the new worksheet.If not provided, a default name will be assigned. |
| position | Integer | Query | Specifies the position at which the new worksheet should be inserted.If not provided, the worksheet will be added at the end of the workbook. |
| sheetName | String | Query | Specifies the type of worksheet to be added.If not provided, a default worksheet type will be used. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
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

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining data. |

On success, the API returns **HTTP 200 OK** with the updated workbook in the response body.


#### HTTP Status Codes

### Supported Worksheet Types

| Type         | Description                                |
| ------------ | ------------------------------------------ |
| `worksheet`  | Standard cell-based worksheet (default)    |
| `chartsheet` | Chart-only sheet                           |
| `macrosheet` | Legacy BIFF8 macro sheet                   |
| `vbmodule`   | Visual Basic for Applications (VBA) module |

> **Note**: Avoid ambiguous or deprecated types like `BIFF4Macro`, `Other`, or `Dialog`; they are not supported in v4.0.

---

## How to Use the Add Worksheet to Spreadsheet API with SDKs?

### Add Worksheet to Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AddWorksheetToSpreadsheet" rel="noopener noreferrer">Add Worksheet to Spreadsheet API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?sheetName=Q2Data&sheetType=worksheet&position=1" \
  -H "Authorization: Bearer <access_token>" \
  -H "Accept: application/json" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -o updated_workbook.xlsx
```

### Use Aspose Cells Cloud SDKs

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
