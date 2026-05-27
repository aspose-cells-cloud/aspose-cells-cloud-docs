---
title: "Aspose.Cells Cloud Move Folder API – Move Folders in Cloud Storage (v4.0)"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud – Move Folder API for Excel File Management"
linktitle: "Move Folder"
type: docs
url: /move-folder/
keywords: "Aspose.Cells Cloud Move Folder, move folder API, Aspose cloud storage, REST move folder, Excel file management, Aspose SDK"
description: "Move a folder in Aspose.Cells Cloud storage with a single REST call. Learn the endpoint, required parameters, sample cURL, SDK usage (C#, Java, Python) and error handling."
weight: 100
---

## **Excel API: Move Folder**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Function Description**

This API moves a folder from one location to another within Aspose.Cells Cloud storage, helping organize files and manage cloud storage efficiently.

### The **moveFolder** API accepts the following parameters:

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

On success, the API returns an empty response body (`200 OK`). Errors are returned as JSON objects containing an `error` field.

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