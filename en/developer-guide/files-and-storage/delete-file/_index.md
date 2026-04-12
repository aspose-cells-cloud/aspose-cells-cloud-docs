---
title: "Aspose.Cells Cloud – Delete File API"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud – Delete File API"
linktitle: "Delete File"
type: docs
url: /delete-file/
keywords: "Aspose Cells, Delete File API, Excel Cloud Storage, REST API, File Management"
description: "Delete an Excel file from Aspose.Cells Cloud storage using the RESTful Delete File API. Includes endpoint, parameters, auth, and sample code."
weight: 100
---

## **Excel API : Delete File**

### Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Function Description**

The **deleteFile** API removes the specified file from cloud storage, helping you manage resources and data efficiently.

### Request Parameters

| Parameter Name | Type   | Location | Description                                                                                 |
| :------------- | :----- | :------- | :------------------------------------------------------------------------------------------ |
| `path`         | string | Path     | The URL‑encoded path to the file that should be deleted.                                    |
| `storageName`  | string | Query    | The name of the storage where the file resides. Omit if the default storage is used.        |
| `versionId`    | string | Query    | Identifier of a specific file version to delete. If omitted, the latest version is removed. |

### HTTP Response Codes

| Code | Meaning                                                   |
| ---- | --------------------------------------------------------- |
| 200  | File deleted successfully (empty body).                   |
| 401  | Unauthorized – missing or invalid token.                  |
| 404  | Not Found – the specified file or storage does not exist. |
| 429  | Too Many Requests – rate limit exceeded.                  |
| 500  | Internal Server Error – unexpected condition.             |

### Response Description

A successful request returns **HTTP 200** with an empty response body. No JSON payload is returned.

```json
{}
```

### Error Handling

- **401 Unauthorized** – Refresh the OAuth token and retry.
- **429 Too Many Requests** – Wait for the period indicated in the `Retry-After` header before retrying.
- **500 Internal Server Error** – Verify request parameters and retry; if the problem persists, contact support.

### **Response Example (Error)**

```json
{
  "error": {
    "code": "FileNotFound",
    "message": "The specified file does not exist."
  }
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK manages low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs.
