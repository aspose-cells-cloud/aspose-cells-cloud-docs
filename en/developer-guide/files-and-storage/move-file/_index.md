---
title: "Move File"
second_title: "Document"
linktitle: "Move File"
type: docs
url: /move-file/
keywords: "Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulation"
description: "Learn how to use the MoveFile API to manage files in Aspose.Cells cloud storage."
weight: 100
kwords: "Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, Move file, File Management, Cloud Storage"
---

## **Excel API: Move File**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Function Description**

The **moveFile** API allows you to move a file from one location to another within the Aspose.Cells cloud storage. This is particularly useful for organizing files and managing storage effectively.

### The request parameters of **moveFile** API are

| Parameter Name      | Type   | Path/Query String/HTTP Body | Description                                |
|---------------------|--------|------------------------------|--------------------------------------------|
| srcPath             | String | Path                         | The source path of the file to be moved.  |
| destPath            | String | Query                        | The destination path where the file will be moved. |
| srcStorageName      | String | Query                        | The source storage name if applicable.     |
| destStorageName     | String | Query                        | The destination storage name if applicable.|
| versionId           | String | Query                        | The version ID of the file if applicable. |

### **Response Description**

```json
{
Void
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/MoveFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
