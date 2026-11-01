---
title: "Aspose.Cells Cloud CopyFile API - Secure Excel File Duplication in the Cloud"
second_title: "Documentation"
articleTitle: "Cloud-based Excel File Management – CopyFile API for Batch File Operations"
linktitle: "CopyFile"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel file copy, Cloud storage, REST API, duplicate Excel file"
description: "Copy Excel files in the cloud with Aspose.Cells Cloud CopyFile API—REST and SDK examples for cURL, Python, Go, Node.js"
weight: 100
---
The **CopyFile** API (`PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}`) in Aspose.Cells Cloud enables secure, server-side duplication of Excel files within or across cloud storage accounts, supporting optional source and destination storage names and versioned file copies via query parameters.

## The Copy File Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### Authentication

All requests require a valid JWT token. See the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for implementation details.  
_Note: External links include `rel="noopener noreferrer"` for security._

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| srcPath | String | Path | - |
| destPath | String | Query | - |
| srcStorageName | String | Query | - |
| destStorageName | String | Query | - |
| versionId | String | Query | - |

### HTTP Responses

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

> **Note**: A `200 OK` response contains no body—success is indicated solely by the HTTP status.

The **CopyFile** API enables secure, server-side duplication of Excel files within or across cloud storage accounts. Ideal for batch operations, backup workflows, and file versioning, this RESTful endpoint operates entirely in the cloud—no local file handling required.

### Example: cURL Request

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

### SDK Examples

Using an SDK simplifies authentication, serialization, and error handling. Below are working examples for key languages.

#### Go

```go
import (
    "context"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v44/cells"
)

config := cells.NewConfiguration()
client := cells.NewCellsApiWithClientConfiguration(config)

_, _, err := client.CopyFile(context.Background(), &cells.CopyFileRequest{
    SrcPath:      "source.xlsx",
    DestPath:     "dest.xlsx",
    SrcStorageName: "MyStorage",
    DestStorageName: "MyStorage",
})
if err != nil {
    panic(err)
}
```

#### Python

```python
from asposecellscloud.api import cells_api
from asposecellscloud.models import CopyFileRequest

api = cells_api.CellsApi(client_id, client_secret)
request = CopyFileRequest(
    src_path="source.xlsx",
    dest_path="dest.xlsx",
    src_storage_name="MyStorage",
    dest_storage_name="MyStorage"
)
api.copy_file(request)
```

#### Node.js

```javascript
const { CellsApi } = require("aspose-cells-cloud");
const client = new CellsApi(process.env.CLIENT_ID, process.env.CLIENT_SECRET);

await client.copyFile("source.xlsx", {
  destPath: "dest.xlsx",
  srcStorageName: "MyStorage",
  destStorageName: "MyStorage",
});
```

> 🔗 [GitHub Repository](https://github.com/aspose-cells-cloud) | [API Reference](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile)

### Related Operations

| Operation       | Description                           | Link               |
| --------------- | ------------------------------------- | ------------------ |
| `PutCreate`     | Upload a new file to cloud storage    | `/put-create/`     |
| `DeleteFile`    | Remove a file from storage            | `/delete-file/`    |
| `GetWorkbook`   | Retrieve a workbook from storage      | `/download-file/`  |
| `CloneWorkbook` | Create a new workbook from a template | `/clone-workbook/` |