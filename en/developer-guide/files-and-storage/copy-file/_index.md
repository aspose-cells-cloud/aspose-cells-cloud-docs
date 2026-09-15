---
title: "Aspose.Cells Cloud CopyFile API - Secure Excel File Duplication in the Cloud"
second_title: "Documentation"
articleTitle: "Cloud-based Excel File Management – CopyFile API for Batch File Operations"
linktitle: "CopyFile"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel file copy, Cloud storage, REST API, duplicate Excel file"
description: "Use Aspose.Cells Cloud’s CopyFile API to securely duplicate Excel files between storage accounts. Includes cURL examples, SDK support (Go, Python, Node.js), authentication guide, and batch operation insights."
weight: 100
date: 2024-02-15T10:00:00Z
lastmod: 2024-02-15T10:00:00Z
draft: false
canonicalURL: "https://reference.aspose.cloud/cells/copy-file/"
---

## Excel Cloud API: CopyFile

The **CopyFile** API enables secure, server-side duplication of Excel files within or across cloud storage accounts. Ideal for batch operations, backup workflows, and file versioning, this RESTful endpoint operates entirely in the cloud—no local file handling required.

### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### Authentication

All requests require a valid JWT token. See the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for implementation details.  
*Note: External links include `rel="noopener noreferrer"` for security.*

### Request Parameters

| Parameter Name    | Type   | Location | Required | Description                                     |
|-------------------|--------|----------|----------|-------------------------------------------------|
| `srcPath`         | string | Path     | Yes      | Source file path in cloud storage.              |
| `destPath`        | string | Query    | Yes      | Destination file path.                          |
| `srcStorageName`  | string | Query    | No       | Source storage name (defaults to internal storage). |
| `destStorageName` | string | Query    | No       | Destination storage name.                       |
| `versionId`       | string | Query    | No       | Optional version ID (for versioned storage).    |

### HTTP Responses

| Status Code | Description                     |
|-------------|---------------------------------|
| `200 OK`    | File copied successfully.       |
| `400 Bad Request` | Invalid or missing parameters (e.g., invalid path, unsupported extension). |
| `401 Unauthorized` | Invalid or expired JWT token.   |
| `413 Payload Too Large` | Source file exceeds size limit (e.g., > 2 GB). |
| `500 Internal Server Error` | Unexpected server-side failure. |

> **Note**: A `200 OK` response contains no body—success is indicated solely by the HTTP status.

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
  destStorageName: "MyStorage"
});
```

> 🔗 [GitHub Repository](https://github.com/aspose-cells-cloud) | [API Reference](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile)

### Related Operations

| Operation | Description | Link |
|-----------|-------------|------|
| `PutCreate` | Upload a new file to cloud storage | `/put-create/` |
| `DeleteFile` | Remove a file from storage | `/delete-file/` |
| `GetWorkbook` | Retrieve a workbook from storage | `/download-file/` |
| `CloneWorkbook` | Create a new workbook from a template | `/clone-workbook/` |

### Best Practices

- ✅ **Use storage names explicitly** to avoid ambiguity in multi-tenant environments.
- ✅ **Validate `destPath` extension** (e.g., `.xlsx`, `.xls`) to prevent format mismatches.
- ✅ **Leverage versioning** via `versionId` for audit trails and rollback support.
- ✅ **Batch copies sequentially** to prevent rate limiting—avoid concurrent large-file copies.

### Structured Data (JSON-LD)

```json
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud CopyFile API Guide",
  "datePublished": "2024-02-15",
  "dateModified": "2024-02-15",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "articleSection": "API Reference",
  "keywords": "CopyFile API, Excel cloud copy, REST API, Aspose.Cells",
  "url": "https://reference.aspose.cloud/cells/copy-file/"
}
```