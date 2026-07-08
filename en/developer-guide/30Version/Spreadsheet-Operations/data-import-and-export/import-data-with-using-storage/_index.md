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
description: "Import data into an Excel worksheet using Aspose.Cells Cloud API from various storage sources. Learn how to import JSON, CSV, or other formats securely via HTTPS."
keywords: "Aspose.Cells Cloud, Excel, Import Data, REST API, Cloud Storage, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Import Data Using Storage - Aspose.Cells Cloud API Documentation"
---

This REST API imports data into an Excel file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### The request parameters are

| Parameter Name | Type   | Location | Description                                            |
| -------------- | ------ | -------- | ------------------------------------------------------ |
| name           | string | path     | The name of the Excel file.                            |
| folder         | string | query    | The folder path in the storage where the file resides. |
| storageName    | string | query    | The name of the storage service.                       |
| importData     | object | body     | JSON object that contains the data to be imported.     |

**The import‑data options parameters** are described in [the reference link](/cells/import/#import-data-option-parameter).

The <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

> **Prerequisites**  
> • A valid Aspose Cloud account with an API key and JWT token.  
> • The target Excel workbook must already exist in the specified storage location.  
> • The chosen storage service (e.g., AWS S3, Azure Blob) must be configured in your Aspose Cloud account.

> **Authentication**  
> The API uses JWT‑based authentication. Obtain a JWT token by calling the `/connect/token` endpoint with your client credentials, then include the token in the `Authorization: Bearer <jwt token>` header of each request.

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

> **Response Codes**  
> | Code | Meaning                              |
> |------|--------------------------------------|
> | 200  | Request succeeded; data imported.    |
> | 400  | Bad request – invalid parameters.   |
> | 401  | Unauthorized – missing or invalid JWT. |
> | 404  | Not found – specified file or storage does not exist. |
> | 500  | Internal server error.               |

---