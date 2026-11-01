---
title: Delete all OLE objects in an Excel worksheet
description: "Delete all OLE objects from Excel worksheet via Aspose.Cells Cloud API v3.0 DELETE endpoint with cURL and SDK examples"
linktitle: Clear
type: docs
url: /oleobjects/clear/
aliases: [/delete-all-oleobjects-from-excel-worksheet/]
keywords: Aspose.Cells Cloud, delete OLE objects, Excel API, REST API, worksheet OLE clear, cloud SDK
api_version: v3.0
last_updated: 2024-11-01
lastmod: 2024-11-01
weight: 60
ArticleTitle: "Clear All OLE Objects from Excel Worksheet via Aspose.Cells Cloud REST API"
---
The **DeleteWorksheetOleObjects** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects`) removes all OLE (Object Linking and Embedding) objects from a specified worksheet in an Excel file while preserving the underlying cell data, a capability provided by Aspose.Cells Cloud to clean legacy spreadsheets or prepare workbooks for redistribution without manual intervention.

> **Note:** The operation is _idempotent_ — calling it when no OLE objects exist returns a successful `200 OK`.

---

## The Delete Worksheet OLE Objects Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worsheet name. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

### Query parameters

| Name          | Type   | Required | Description                                 |
| ------------- | ------ | -------- | ------------------------------------------- |
| `folder`      | string | optional | Folder containing the workbook.             |
| `storageName` | string | optional | Storage name where the workbook is located. |

**Headers**

| Header          | Value                |
| --------------- | -------------------- |
| `Authorization` | `Bearer <jwt token>` |
| `Accept`        | `application/json`   |
| `Content-Type`  | `application/json`   |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

_Replace `<jwt token>` with a valid access token and adjust `folder`/`storageName` as needed._

---

## Successful Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                                   |
| ---- | --------------------- | ----------------------------------------------------------------------------- |
| 200  | OK                    | All OLE objects deleted successfully.                                         |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type, locked workbook). |
| 401  | Unauthorized          | Invalid or missing JWT token.                                                 |
| 413  | Payload Too Large     | Workbook exceeds size limit (max 2 GB per file).                              |
| 500  | Internal Server Error | Unexpected server error.                                                      |

---

## SDK Samples

The following code snippets demonstrate how to invoke **DeleteWorksheetOleObjects** with the official Aspose.Cells Cloud SDKs. Replace placeholder values (`<YOUR_TOKEN>`, `<FILE_NAME>`, etc.) with your own data.
