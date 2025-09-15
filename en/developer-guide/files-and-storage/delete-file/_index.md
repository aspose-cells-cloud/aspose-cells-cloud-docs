---
title: "Delete File - Excel API"
second_title: "Document"
linktitle: "Delete File"
type: docs
url: /delete-file/
keywords: "Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usage"
description: "Learn how to delete files in Excel using the Aspose.Cells API. This guide provides detailed information on the deleteFile API endpoint, request parameters, and response structure."
weight: 100
kwords: "Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usage"
---

## **Excel API : Delete File**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Function Description**

The **deleteFile** API allows users to remove specified files from cloud storage, ensuring efficient management of resources and data.

### The request parameters for the **deleteFile** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- |:- |
|path|String|Path|The path to the file that needs to be deleted.|
|storageName|String|Query|The name of the storage where the file is located. Optional if default storage is used.|
|versionId|String|Query|The version ID of the file to delete, if applicable.|

### **Response Description**

```json
{
Void
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK manages low-level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
