---
title: Delete all OLE objects in an Excel worksheet
description: Delete all OLE objects from an Excel worksheet using Aspose.Cells Cloud REST API v3.0. Includes cURL examples, SDK samples (C#, Java, Python, Node.js, Go), path/query parameters, error handling, and best practices.
linktitle: Clear
type: docs
url: /oleobjects/clear/
aliases: [/delete-all-oleobjects-from-excel-worksheet/]
keywords: Aspose.Cells Cloud, delete OLE objects, Excel API, REST API, worksheet OLE clear, cloud SDK
api_version: v3.0
last_updated: 2024-11-01
lastmod: 2024-11-01
weight: 60
---

# Delete all OLE objects in an Excel worksheet

**OleObjects – Clear** removes **all** OLE (Object Linking and Embedding) objects from a specified worksheet while leaving cell data untouched. This operation is useful for cleaning legacy spreadsheets or preparing a workbook for redistribution.

> **Note:** The operation is _idempotent_ — calling it when no OLE objects exist returns a successful `200 OK`.

---

## Prerequisites

- A valid **Aspose Cloud JWT access token** (OAuth 2.0).
- The target workbook must be stored in Aspose Cloud storage (or specify the `folder`/`storageName` where it resides).
- API version **v3.0** or higher.

---

## HTTP Request

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Path parameters

| Name        | Type   | Required | Description                    |
| ----------- | ------ | -------- | ------------------------------ |
| `name`      | string | ✔️       | The name of the workbook file. |
| `sheetName` | string | ✔️       | The name of the worksheet.     |

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
