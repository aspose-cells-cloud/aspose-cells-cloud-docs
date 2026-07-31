---
title: "Import Data Using Storage"
second_title: "Document"
linktitle: "Import data with storage"
type: docs
url: /import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Import Data Using Storage: Import data into an Excel worksheet using Aspose.Cells Cloud API from various storage sources. Supports JSON, CSV, and other formats via HTTPS."
keywords: "Aspose.Cells Cloud, Excel, Import Data, REST API, Cloud Storage, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Import Data Using Storage - Aspose.Cells Cloud API Documentation"
---

This REST API imports data into an Excel file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### The request parameters are

| Parameter Name | Type   | Location | Description                                            |
| -------------- | ------ | -------- | ------------------------------------------------------ |
| name           | string | path     | The name of the Excel file.                            |
| folder         | string | query    | The folder path in the storage where the file resides. |
| storageName    | string | query    | The name of the storage service.                       |
| importData     | object | body     | JSON object that contains the data to be imported.     |

**The import‑data options parameters** are described in [the reference link](/cells/import/#import-data-option-parameter).

**Prerequisites:** You must provide a valid JWT token in the `Authorization` header and ensure that the target workbook already exists in the specified storage location.

### Response

```json
{
  "Status":"OK",
  "Code":200
}
```
**Http Status Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200  | OK      | Import succeeded; the workbook is updated with the supplied data. |
| 400  | Bad Request | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized | Invalid or missing JWT token. |
| 413  | Payload Too Large | Uploaded file exceeds size limit. |
| 500  | Internal Server Error | Unexpected server error. |

## How to Use the PostImportData API with SDKs

### PostImportData API Specification

The <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to accelerate development. An SDK abstracts low‑level details, allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code example demonstrates how to call the Aspose.Cells web service using the PHP SDK: