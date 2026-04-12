---
title: "Aspose.Cells Cloud Move Folder API – Quickly Move Folders in the Cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management – Quickly Move Folders in the Cloud"
linktitle: "Move Folder"
type: docs
url: /move-folder/
keywords: "Aspose.Cells, Move Folder API, Cloud Storage, Excel REST API, Files Management"
description: "Learn how to move folders in Aspose.Cells Cloud storage via the RESTful Move Folder API. Includes endpoint, parameters, sample cURL, error codes, and SDK examples for C#, Java, Python, and more."
weight: 100
---

## **Excel API: Move Folder**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Function Description**

This API moves a folder from one location to another within Aspose.Cells Cloud storage. It helps organise files and manage cloud storage efficiently.

### The request parameters of **moveFolder** API are

| Parameter Name  | Type   | Location | Description                                                       |
| --------------- | ------ | -------- | ----------------------------------------------------------------- |
| srcPath         | string | Path     | The full path of the folder to be moved, e.g., `FolderA/`.        |
| destPath        | string | Query    | The target path where the folder will be moved, e.g., `FolderB/`. |
| srcStorageName  | string | Query    | (Optional) Name of the source storage.                            |
| destStorageName | string | Query    | (Optional) Name of the destination storage.                       |

**Parameter details**

- **srcPath** – required. The source folder path.
- **destPath** – required. The destination folder path.
- **srcStorageName** – optional. Identifier of the source storage.
- **destStorageName** – optional. Identifier of the destination storage.

### **Response Description**

On success the API returns an empty response body (`200 OK`). Errors are returned as JSON objects containing an `error` field.

### **Error Handling**

| HTTP Status | Error Code            | Description                            |
| ----------- | --------------------- | -------------------------------------- |
| 400         | `FolderAlreadyExists` | Destination folder already exists.     |
| 400         | `InvalidPath`         | Source or destination path is invalid. |
| 401         | `Unauthorized`        | Missing or invalid access token.       |
| 404         | `FolderNotFound`      | Source folder does not exist.          |
| 500         | `InternalError`       | Unexpected server error.               |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
