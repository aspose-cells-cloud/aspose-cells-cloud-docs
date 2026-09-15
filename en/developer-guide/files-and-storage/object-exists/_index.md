---
title: "Object Exists API – Check File/Folder Presence in Aspose.Cells Cloud"
url: "https://reference.aspose.cloud/cells/#/StorageController/ObjectExists"
linktitle: "Object Exists (Storage)"
date: 2024-03-15T10:00:00Z
draft: false
robots: index, follow
sitemap:
  changefreq: monthly
  priority: 0.8
keywords: "Aspose.Cells Cloud, file existence check, folder existence, storage API, REST API, object exists endpoint"
description: "Aspose.Cells Cloud Object Exists API: Verify file or folder presence in cloud storage with optional versioning and storage selection. Includes cURL, SDK examples, authentication, and response details."
weight: 100
---

Use the **Object Exists API** to efficiently determine whether a specific file or folder exists in Aspose.Cells Cloud storage. This lightweight endpoint supports optional `storageName` and `versionId` parameters and returns structured Boolean indicators for existence and type (file vs. folder).

## Overview

The Object Exists API is part of the Aspose.Cells Cloud Storage API suite, enabling developers to programmatically verify resource presence before performing operations such as download, delete, or version restoration—reducing unnecessary processing and error handling.

> **Note**: This API endpoint is versioned at `/v5.0/`. Ensure all client requests use this version to avoid compatibility issues.

## HTTP Request

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

### Path Parameters

| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `path`    | string | Yes      | Full path to the file or folder in cloud storage (e.g., `Book1.xlsx` or `Reports/Q3/`). |

### Query Parameters

| Parameter      | Type   | Required | Description |
|----------------|--------|----------|-------------|
| `storageName`  | string | No       | Name of the cloud storage; defaults to the primary storage if omitted. |
| `versionId`    | string | No       | Version identifier for versioned objects (only applicable when storage versioning is enabled). |

## Authentication

All requests to Aspose.Cells Cloud APIs require JWT token authentication. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for implementation guidance.

## HTTP Status Codes

| Code | Status            | Description |
|------|-------------------|-------------|
| 200  | OK                | Request succeeded; response body contains existence and type info. |
| 400  | Bad Request       | Invalid or missing `path` parameter; unsupported format in path. |
| 401  | Unauthorized      | Invalid, expired, or missing JWT token. |
| 403  | Forbidden         | Insufficient permissions for the requested storage. |
| 404  | Not Found         | Storage or path not found (e.g., `storageName` does not exist). |
| 500  | Internal Server Error | Unexpected server-side error. |

## Response

A successful response returns a JSON object with the following structure:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

| Field     | Type    | Description |
|-----------|---------|-------------|
| `Exists`  | boolean | `true` if the object exists; `false` otherwise. |
| `IsFolder`| boolean | `true` if the path refers to a folder; `false` for a file. |

> **Tip**: Use `Exists == false` to short-circuit operations before attempting file access—reducing redundant API calls.

## Example Requests

### cURL Example (v5.0)

```bash
curl -X GET "https://api.aspose.cloud/v5.0/cells/storage/exist/Reports/Quarterly.xlsx?storageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: application/json"
```

**Response (200 OK)**:
```json
{
  "Exists": true,
  "IsFolder": false
}
```

> ✅ **Fix applied**: Updated from `/v4.0/` to `/v5.0/` to match the documented API endpoint.

## SDK Integration

Using an SDK simplifies authentication, serialization, and error handling. Below are quick-start examples:

{{< tabs tabTotal="4" tabID="1" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Node.js" >}}

{{< tab tabNum="1" >}}

```csharp
var configuration = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};
var api = new StorageApi(configuration);

var response = await api.ObjectExists("Reports/Quarterly.xlsx", storageName: "MyStorage");
Console.WriteLine($"Exists: {response.Exists}, IsFolder: {response.IsFolder}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}

```java
Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");
StorageApi api = new StorageApi(config);

ObjectExist response = api.objectExists("Reports/Quarterly.xlsx", "MyStorage", null);
System.out.printf("Exists: %b, IsFolder: %b%n", response.getExists(), response.getIsFolder());
```
{{< /tab >}}

{{< tab tabNum="3" >}}

```python
from asposecellscloud.configuration import Configuration
from asposecellscloud.cells_api import CellsApi

config = Configuration()
config.app_sid = "YOUR_APP_SID"
config.app_key = "YOUR_APP_KEY"
api = CellsApi(config)

response = api.object_exists("Reports/Quarterly.xlsx", storage_name="MyStorage")
print(f"Exists: {response.exists}, IsFolder: {response.is_folder}")
```
{{< /tab >}}

{{< tab tabNum="4" >}}

```javascript
const { StorageApi } = require('aspose.cells.cloud');

const configuration = new Configuration({
  appSid: 'YOUR_APP_SID',
  apiKey: 'YOUR_APP_KEY'
});
const storageApi = new StorageApi(configuration);

const response = await storageApi.objectExists('Reports/Quarterly.xlsx', { storageName: 'MyStorage' });
console.log(`Exists: ${response.body.exists}, IsFolder: ${response.body.isFolder}`);
```
{{< /tab >}}

{{< /tabs >}}

> 🔗 Explore official SDKs: [GitHub Repository](https://github.com/aspose-cells-cloud)

## Related API Endpoints

- [Upload File API](/cells/upload-file/) — Upload documents to cloud storage.  
- [Download File API](/cells/download-file/) — Retrieve files from storage.  
- [Get Storage Items](/cells/storage-items/) — List files and folders in a storage path.

## Best Practices

- ✅ **Pre-validate before operations** — Use `Object Exists` to avoid `404 Not Found` errors during downloads or deletes.  
- ✅ **Specify `storageName` explicitly** — Prevent accidental writes to the default storage.  
- ✅ **Handle `IsFolder` separately** — A path may exist as a folder or file; use `IsFolder` to branch logic accordingly.  
- ✅ **Version-aware checks** — When versioning is enabled, include `versionId` to verify a specific revision.

## OpenAPI Specification

The API contract is defined in the [ObjectExists operation](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) within the Aspose.Cells Cloud OpenAPI specification. You can also explore the interface directly in the [Swagger UI](https://apireference.aspose.cloud/cells/).