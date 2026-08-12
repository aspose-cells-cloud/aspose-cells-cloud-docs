---
title: "Unpivot Table"
ArticleTitle: "Unpivot Table – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Unpivot Table"
type: docs
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, Unpivot, Transform"
description: "Switch rows and columns in the spreadsheet."
weight: 1
---

## The Unpivot Table of Aspose.Cells Cloud Web Services

Switch rows and columns in the spreadsheet.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name   | Type    | Path/Query String/HTTP Body | Description                                                                                                            |
|------------------|---------|-----------------------------|------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | File    | FormData                    | Upload spreadsheet file.                                                                                               |
| worksheet        | String  | Query                       | The worksheet name.                                                                                                    |
| index            | Integer | Query                       | A specified data range.                                                                                                |
| skipEmptyValue   | Boolean | Query                       | Skip empty values (default: true).                                                                                    |
| outPath          | String  | Query                       | (Optional) The folder path where the workbook is stored. The default is null.                                         |
| outStorageName   | String  | Query                       | Output file Storage Name.                                                                                              |
| region           | String  | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password         | String  | Query                       | The password for opening spreadsheet file.                                                                             |

### Request Body Parameter

| Parameter Name | Type | Description |
| -------------- | ---- | ----------- |
| N/A            | N/A  | No request body parameters. |

### **Response**

```json
{
  "File": "binary stream of the unpivoted spreadsheet"
}
```

**Response Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | The unpivoted spreadsheet file is returned. |
| 400 | Bad Request | Invalid request parameters. |
| 401 | Unauthorized | Authentication failed or JWT token missing/invalid. |
| 413 | Payload Too Large | Uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | Unexpected server error. |

## How to Use the Unpivot Table with SDKs

### Unpivot Table Specification

The [Unpivot Table API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Use HTTPS for a secure connection
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "binary stream of the unpivoted spreadsheet"
}
```

{< /tab >}

{< /tabs >}

### Use Aspose Cells Cloud SDKs

Using an SDK is the fastest way to accelerate development. An SDK abstracts low-level details, allowing you to focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose Cells Cloud web services using various SDKs:
 `[TBD]`