---
title: "Aspose.Cells Cloud Move Folder API – Quickly Move Folders in the Cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management – Quickly Move Folders in the Cloud"
linktitle: "Move Folder"
type: docs
url: /move-folder/
keywords: "Aspose.Cells, Move Folder, Cloud Storage, Excel API"
description: "Learn how to move folders in Aspose.Cells Cloud storage via the RESTful Move Folder API. Includes endpoint, parameters, sample cURL, error codes, and SDK examples for C#, Java, Python, and more."
weight: 100
---

This API moves a folder from one location to another within Aspose.Cells Cloud storage. It helps organize files and manage cloud storage efficiently.

## **Excel API: Move Folder**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**Example cURL request**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

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

### **Response**

On success the API returns an empty response body with HTTP status **200 OK**. Errors are returned as JSON objects containing an `error` field.

**HTTP Status Codes**

| HTTP Code | HTTP Status           | Description                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK                    | Web API called successfully; response contains operation details. |
| 400       | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401       | Unauthorized          | Invalid or missing JWT token.                                     |
| 413       | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500       | Internal Server Error | Unexpected server error.                                          |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Using an SDK is the best way to speed up the development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
