---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Get Merged Cells in Worksheet – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "GetMergedCellsInWorksheet"
type: docs
url: /cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, merged cells, worksheet, API"
description: "Get all merged cell area from a local spreadsheet worksheet."
weight: 1000
---

## The Get Merged Cells In Worksheet of Aspose.Cells Cloud Web Services

Get all merged cell area from a local spreadsheet worksheet.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | Worksheet name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| N/A | N/A | This operation does not accept a JSON body; the spreadsheet file is sent via `multipart/form-data`. |

### **Response**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Successfully retrieved merged cell areas. |
| 400 | Bad Request | One or more request parameters are invalid or missing. |
| 401 | Unauthorized | Authentication failed – invalid or missing JWT token. |
| 413 | Payload Too Large | Uploaded spreadsheet exceeds the allowed size limit. |
| 500 | Internal Server Error | An unexpected error occurred on the server. |

## How to Use the Get Merged Cells In Worksheet with SDKs

### Get Merged Cells In Worksheet Specification

The [Get Merged Cells In Worksheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
 `[TBD]`