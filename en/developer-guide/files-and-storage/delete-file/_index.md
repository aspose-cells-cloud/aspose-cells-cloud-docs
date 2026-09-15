---
title: "Delete File"
linktitle: "Delete File"
type: docs
url: /delete-file/
description: "Delete an Excel file from Aspose.Cells Cloud storage using the REST API. Includes endpoint, path/query parameters, authentication, HTTP status codes, and cURL/SDK examples."
keywords: "Aspose.Cells, delete file API, Excel cloud storage, REST API, file management, cloud file deletion"
date: 2024-03-15
lastmod: 2024-05-22
canonical: "https://reference.aspose.cloud/cells/delete-file/"
weight: 100
---

# Delete File

Delete a file from Aspose.Cells Cloud storage using the RESTful API.

## Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### Request Parameters

| Parameter Name | Type   | Location | Description |
| :------------- | :----- | :------- | :---------- |
| `path`         | string | Path     | **Required.** The URL-encoded path to the file in cloud storage (e.g., `input/Report.xlsx`). |
| `storageName`  | string | Query    | **Optional.** The name of the storage where the file resides. Omit to use the default storage. |
| `versionId`    | string | Query    | **Optional.** The version identifier of the file to delete. If omitted, the latest version is deleted. |

### Security and Authentication

All requests require JWT token authentication.

```bash
-H "Authorization: Bearer {access_token}"
```

> **Note**: Replace `{access_token}` with your valid JWT access token. See the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for setup instructions.

### Response Description

A successful request returns **HTTP 200** with an empty response body.

```json
{}
```

#### HTTP Status Codes

| Code | Meaning               | Description |
| :--- | :-------------------- | :---------- |
| 200  | OK                    | File deleted successfully. |
| 400  | Bad Request           | Invalid or missing `path`, unsupported file type, or malformed query parameters. |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token. |
| 404  | Not Found             | File or storage not found. |
| 413  | Payload Too Large     | Request size exceeds limits (rare for DELETE). |
| 500  | Internal Server Error | Unexpected server error. |

### Examples

#### cURL Request

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

> **Tip**: Replace `{access_token}` with your valid JWT token. For test environments, you may generate a token via the [OAuth Playground](https://apiconsole.aspose.cloud/applications).

#### Using Aspose.Cells Cloud SDKs

SDKs abstract low-level HTTP details and improve reliability. Available SDKs include .NET, Java, Python, Node.js, PHP, Ruby, and Go.

- 📘 **SDK Documentation**: [https://docs.aspose.cloud/cells/sdk/](https://docs.aspose.cloud/cells/sdk/)
- 💻 **GitHub Repositories**: [https://github.com/aspose-cells-cloud](https://github.com/aspose-cells-cloud)

##### Example (C#)

```csharp
var config = new Configuration { ClientId = "YOUR_CLIENT_ID", ClientSecret = "YOUR_CLIENT_SECRET" };
var cellsApi = new CellsApi(config);

// Delete file from storage
await cellsApi.DeleteFile("Example.xlsx", "MyStorage");
```

##### Example (Python)

```python
from asposecellscloud.configuration import Configuration
from asposecellscloud.api.cells_api import CellsApi

config = Configuration(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
cells_api = CellsApi(config)

# Delete file
await cells_api.delete_file("Example.xlsx", storage_name="MyStorage")
```

### Related Operations

- [Upload File](/upload-file/)  
- [List Files](/list-files/)  
- [Download File](/download-file/)  
- [Storage API Overview](/storage-api/)

### OpenAPI Specification

The OpenAPI specification for this operation is available as a machine-readable YAML file:  
🔗 [spec.yaml](https://raw.githubusercontent.com/aspose-cells-cloud/aspose-cells-cloud/master/openapi/spec.yaml)