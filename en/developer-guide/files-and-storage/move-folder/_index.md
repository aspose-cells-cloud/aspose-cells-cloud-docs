---
title: "Aspose.Cells Cloud Move Folder API – Quickly Move Folders in the Cloud"
second_title: "Developer Guide"
ArticleTitle: "Cloud-based Excel File Management – Quickly Move Folders in the Cloud"
linktitle: "Move Folder"
type: docs
url: /move-folder/
keywords: "Aspose.Cells, Move Folder, Cloud Storage, Excel API"
description: "Learn how to move folders in Aspose.Cells Cloud storage via the RESTful Move Folder API. Includes endpoint, parameters, sample cURL, error codes, and SDK examples for C#, Java, Python, and more."
weight: 100
---
The **MoveFolder** API (`PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}`) in Aspose.Cells Cloud moves a folder from a specified source path to a destination path within cloud storage, using required path parameter `srcPath` and query parameter `destPath` to define the operation, and optionally supporting `srcStorageName` and `destStorageName` for multi-storage scenarios, enabling efficient reorganization of files and storage resources programmatically.

## The Move Folder Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### The request parameters of **moveFolder** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| srcPath | String | Path | - |
| destPath | String | Query | - |
| srcStorageName | String | Query | - |
| destStorageName | String | Query | - |

**Parameter details**

- **srcPath** – required. The source folder path.
- **destPath** – required. The destination folder path.
- **srcStorageName** – optional. Identifier of the source storage.
- **destStorageName** – optional. Identifier of the destination storage.

### **Response**

```json
[
  {
    "Name": "Void",
    "DataType": {
      "Identifier": "Void"
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

On success the API returns an empty response body with HTTP status **200 OK**. Errors are returned as JSON objects containing an `error` field.

### Web API
**Example cURL request**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

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
