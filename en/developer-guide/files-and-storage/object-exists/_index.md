---
title: "Object Exists API – Check File/Folder Presence in Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Object Exists API – Verify File or Folder Presence in Aspose.Cells Cloud"
linktitle: "Object Exists"
type: docs
url: /object-exists/
keywords: "Aspose.Cells, cloud storage, object exists, file existence, folder existence, API"
description: "Use the Object Exists API to quickly verify whether a file or folder exists in Aspose.Cells Cloud storage. Supports optional storage name and version ID, and works with versioned objects."
weight: 100
---

The **Object Exists API** lets developers determine whether a specific file or folder is present in Aspose.Cells Cloud storage. It returns a simple Boolean indicating existence and whether the path points to a folder.

## **Excel API: Object Exists**

### Web API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ is the full path to the file or folder in storage.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Location | Required | Description                                                         |
| -------------- | ------ | -------- | -------- | ------------------------------------------------------------------- |
| `path`         | string | Path     | Yes      | Full path to the file or folder.                                    |
| `storageName`  | string | Query    | No       | Name of the storage; defaults to the primary storage if omitted.    |
| `versionId`    | string | Query    | No       | Specific version identifier of the file (if versioning is enabled). |

**HTTP Status Codes**

| HTTP Code | HTTP Status           | Description                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK                    | Web API called successfully; response contains operation details. |
| 400       | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401       | Unauthorized          | Invalid or missing JWT token.                                     |
| 413       | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500       | Internal Server Error | Unexpected server error.                                          |

### **Response**

A successful call returns a JSON payload with two properties:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true` if the file or folder exists; otherwise `false`.
- **IsFolder** – `true` when the path points to a folder; `false` for a file.

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
