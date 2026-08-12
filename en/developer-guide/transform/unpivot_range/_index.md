---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "UnpivotRange"
type: docs
url: /cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Switch rows and columns in the spreadsheet."
weight: 10
---

## The UnpivotRange of Aspose.Cells Cloud Web Services

Switch rows and columns in the spreadsheet.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type   | Path/Query String/HTTP Body | Description                                                                                                                                                     |
|------------------|--------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File   | FormData                    | Upload spreadsheet file.                                                                                                                                         |
| worksheet        | string | Query                       | The worksheet name.                                                                                                                                              |
| cellArea         | string | Query                       | A specified data range.                                                                                                                                          |
| skipEmptyValue   | boolean| Query                       | If true, skips empty values. Default: true.                                                                                                                      |
| outPath          | string | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                                                                   |
| outStorageName   | string | Query                       | Output file Storage Name.                                                                                                                                       |
| region           | string | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior.                        |
| password         | string | Query                       | The password for opening spreadsheet file.                                                                                                                      |

### Request Body Parameter

| Parameter Name | Type | Description |
|----------------|------|-------------|
| — | — | — |

### **Response**

```json
{
  "File": "binary stream"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The unpivoted spreadsheet file is returned. |
| 400 | Bad Request | Invalid request parameters. |
| 401 | Unauthorized | Authentication failed. |
| 413 | Payload Too Large | Uploaded file exceeds size limit. |
| 500 | Internal Server Error | Server encountered an unexpected condition. |

## How to Use the UnpivotRange with SDKs

### UnpivotRange Specification

The [UnpivotRange API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells Cloud web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
 `[TBD]`