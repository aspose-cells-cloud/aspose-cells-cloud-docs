---
title: "Object Exists API – Check File/Folder Presence in Aspose.Cells Cloud"
second_title: "Developer Guide"
ArticleTitle: "Object Exists API – Verify File or Folder Presence in Aspose.Cells Cloud"
linktitle: "Object Exists"
type: docs
url: /object-exists/
keywords: "Aspose.Cells, cloud storage, object exists, file existence, folder existence, API"
description: "Use the Object Exists API to quickly verify whether a file or folder exists in Aspose.Cells Cloud storage. Supports optional storage name and version ID, and works with versioned objects."
weight: 100
---
The **ObjectExists** API (`GET https://api.aspose.cloud/v4.0/cells/storage/exist/{path}`) enables developers to verify whether a specific file or folder exists in Aspose.Cells Cloud storage by providing a storage path; it supports optional `storageName` and `versionId` query parameters and returns an `ObjectExist` response indicating existence and whether the path refers to a folder.

## The Object Exists Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/exist/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| path | String | Path | - |
| storageName | String | Query | - |
| versionId | String | Query | - |

### **Response**

```json
[
  {
    "Name": "ObjectExist",
    "DataType": {
      "Identifier": "Class",
      "Reference": "ObjectExist"
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

A successful call returns a JSON payload with two properties:


- **Exists** – `true` if the file or folder exists; otherwise `false`.
- **IsFolder** – `true` when the path points to a folder; `false` for a file.

### Web API
_`{path}`_ is the full path to the file or folder in storage.

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/exist/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs. If a Gist fails to load, a static example is provided below each tab.
