---
url: /move-file/
title: Move File in Aspose.Cells Cloud
second_title: "API Reference"
linktitle: "Move File"
type: docs
description: "Use Aspose.Cells Cloud's v4.0 Move File API to programmatically relocate Excel files between cloud storage folders. Includes API endpoint, parameters, cURL, and SDK examples."
keywords: "Aspose.Cells Cloud API, Excel file move REST, cloud storage management, file operations API, document automation"
date: 2024-03-15
weight: 100
draft: false
---

## Move File in Aspose.Cells Cloud

The **Move File** API enables you to relocate files between folders within Aspose.Cells Cloud storage. This operation supports organizing large file inventories, implementing archival strategies, and maintaining structured storage hierarchies—all without modifying the file’s content or metadata. Version history is preserved during the move.

> **Prerequisites**  
> Before using this API, ensure you have:  
> 1. An active [Aspose.Cells Cloud account](https://dashboard.aspose.cloud/)  
> 2. Valid client credentials (`Client ID` and `Client Secret`)  
> 3. A file already uploaded to your cloud storage (e.g., via [Upload File](/upload-file/))

---

### Excel API: Move File

#### Web API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

#### Authentication

All Aspose.Cells Cloud API requests require JWT token-based authentication. Include your access token in the `Authorization` header:

```http
Authorization: Bearer {access_token}
```

For detailed instructions, see our [Aspose.Cells Cloud JWT authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

#### Request Parameters

| Parameter Name    | Type   | Location | Required | Description                                                                 |
|-------------------|--------|----------|----------|-----------------------------------------------------------------------------|
| `srcPath`         | string | Path     | Yes      | Full path of the source file in cloud storage (e.g., `Source/Report.xlsx`) |
| `destPath`        | string | Query    | Yes      | Full path where the file will be moved (e.g., `Archive/2024/Report.xlsx`) |
| `srcStorageName`  | string | Query    | No       | Name of the source storage (uses default storage if omitted)               |
| `destStorageName` | string | Query    | No       | Name of the destination storage (uses default storage if omitted)          |
| `versionId`       | string | Query    | No       | Specific version ID to move (for versioned files)                          |

#### Request Example (cURL)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/Source/Report.xlsx?destPath=Archive/2024/Report.xlsx" \
     -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.x..." \
     -H "Content-Type: application/json"
```

#### Response

A successful request returns `HTTP 200 OK` with an empty JSON body:

```json
{}
```

#### HTTP Status Codes

| Code | Status            | Description                                                                 |
|------|-------------------|-----------------------------------------------------------------------------|
| 200  | OK                | File moved successfully.                                                    |
| 400  | Bad Request       | Missing or invalid parameters (e.g., `srcPath` or `destPath` invalid).      |
| 401  | Unauthorized      | Invalid, expired, or missing JWT token.                                     |
| 404  | Not Found         | Source file does not exist or storage path is inaccessible.                 |
| 409  | Conflict          | Destination path already exists and cannot be overwritten.                  |
| 500  | Internal Server Error | Unexpected server-side error occurred during processing.               |

#### Notes

- Moving a file **does not** change its content, formatting, or embedded metadata (e.g., custom properties).
- Version history is preserved when moving versioned files.
- If `destPath` includes non-existent folders, they will be created automatically.

---

### Code Examples

Using an SDK is the best way to accelerate development. SDKs handle authentication, serialization, and error handling automatically.

The following code examples demonstrate how to call the Move File API:

{{< tabs tabTotal="4" tabID="1" tabName1="Go" tabName2="Python" tabName3="Node.js" tabName4="C#" >}}

{{< tab tabNum="1" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v40/cells"
)

func main() {
    cfg := cells.NewConfiguration("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET")
    client := cells.NewAPIClient(cfg)
    
    srcPath := "Source/Report.xlsx"
    destPath := "Archive/2024/Report.xlsx"
    
    _, err := client.FileController.MoveFile(srcPath, &cells.MoveFileOptions{
        DestPath: &destPath,
    })
    
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("File moved successfully!")
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```python
from asposecellscloud.api import CellsApi
from asposecellscloud.models import MoveFileRequest

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"
api = CellsApi(client_id, client_secret)

src_path = "Source/Report.xlsx"
dest_path = "Archive/2024/Report.xlsx"

request = MoveFileRequest(
    src_path=src_path,
    dest_path=dest_path
)

api.cells_storage_move_file(request)
print("File moved successfully!")
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```javascript
const { CellsApi } = require("asposecellscloud");

const clientId = "YOUR_CLIENT_ID";
const clientSecret = "YOUR_CLIENT_SECRET";
const api = new CellsApi(clientId, clientSecret);

const srcPath = "Source/Report.xlsx";
const destPath = "Archive/2024/Report.xlsx";

api.cellsStorageMoveFile(srcPath, destPath)
  .then(() => {
    console.log("File moved successfully!");
  })
  .catch(err => {
    console.error("Error:", err);
  });
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```csharp
using Aspose.Cells.Cloud.Sdk;

var configuration = new Configuration 
{ 
    ClientId = "YOUR_CLIENT_ID", 
    ClientSecret = "YOUR_CLIENT_SECRET" 
};
var cellsApi = new CellsApi(configuration);

string srcPath = "Source/Report.xlsx";
string destPath = "Archive/2024/Report.xlsx";

await cellsApi.CellsStorageMoveFileAsync(srcPath, destPath);
Console.WriteLine("File moved successfully!");
```

{{< /tab >}}

{{< /tabs >}}

> 💡 **Tip**: For full SDK examples and language-specific documentation, explore the [open-source Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud).

---

### See Also

- [Upload File](/upload-file/)  
- [Delete File](/delete-file/)  
- [Get File](/get-file/)  
- [Download File](/download-file/)  

---

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/MoveFile) defines this publicly accessible programming interface and enables direct REST interactions from any HTTP client.