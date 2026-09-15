---
title: "Create Folder – Aspose.Cells Cloud API"
second_title: "Aspose.Cells Cloud Documentation"
linktitle: "Create Folder"
type: docs
url: /create-folder/
keywords: "Aspose.Cells, Cloud API, Create Folder, Storage Management, Excel"
description: "Programmatically create folders in Aspose.Cells Cloud storage via REST API. Includes cURL examples, SDK code for 8 languages, and error handling."
weight: 100
date: 2024-03-15T10:00:00Z
lastmod: 2024-05-22T14:30:00Z
canonical_url: "https://reference.aspose.cloud/cells/create-folder/"
aliases:
  - "/create-folder"
  - "/cells/create-folder"
tags:
  - storage
  - api
  - rest
---

The `createFolder` operation creates a new folder at the specified location in Aspose.Cells Cloud storage. This is essential for organizing files and maintaining a structured directory hierarchy.

## Excel API: Create Folder

### Web API Endpoint

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

> 💡 **Note**: The `folder` path segment is case-insensitive on Aspose.Cloud storage backends.

### Authentication

Aspose.Cells Cloud APIs require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name | Type   | Location | Required | Default | Description                                                                 |
| -------------- | ------ | -------- | -------- | ------- | --------------------------------------------------------------------------- |
| `path`         | string | Path     | Yes      | —       | The folder path to create (e.g., `myFolder/subFolder`).                     |
| `storageName`  | string | Query    | No       | —       | The name of the storage to use. If omitted, the default storage is applied. |

### Response

The operation returns HTTP status `200 OK` with an empty JSON body (`{}`) on success.

**HTTP Status Codes**

| Code | Status            | Description                                                                 |
| ---- | ----------------- | --------------------------------------------------------------------------- |
| 200  | OK                | Folder created successfully.                                                |
| 400  | Bad Request       | Missing or invalid parameters (e.g., invalid path syntax or unsupported characters). |
| 401  | Unauthorized      | Invalid, expired, or missing JWT token.                                    |
| 409  | Conflict          | Folder already exists at the specified path.                               |
| 500  | Internal Server Error | Unexpected server error.                                                |

### Example: cURL Request

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```
{{< /tab >}}
{{< tab tabNum="12" >}}
```json
{}
```
{{< /tab >}}
{{< /tabs >}}

### Example: SDK Usage

Using an SDK is the recommended approach to accelerate development. SDKs handle authentication, request serialization, and error handling automatically. See the [Aspose.Cells Cloud SDKs GitHub repository](https://github.com/aspose-cells-cloud) for full implementation details.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}

### OpenAPI Specification

The [OpenAPI specification](https://raw.githubusercontent.com/aspose-cells-cloud/aspose-cells-cloud/master/spec/cells_api.json) for this operation is publicly available for programmatic reference.

### See Also

- [Manage Storage](/storage/) — Learn about Aspose.Cells Cloud storage concepts and configuration.
- [List Folders](/list-folders/) — Retrieve directory contents from cloud storage.
- [Delete Folder](/delete-folder/) — Remove an empty folder from storage.

> *Last updated: March 2024 | API version: v4.0*