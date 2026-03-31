---  
title: "Aspose.Cells Cloud Move Folder API – Quickly Move Folders in the Cloud"  
second_title: "Document"  
ArticleTitle: "Cloud-based Excel File Management – Quickly Move Folders in the Cloud"  
linktitle: "Move Folder"  
type: docs  
url: /move-folder/  
keywords: "Aspose.Cells, Move Folder API, Cloud Storage, Excel REST API, Files Management"  
description: "Learn how to move folders in Aspose.Cells Cloud storage via the RESTful Move Folder API. Includes endpoint, parameters, sample cURL, error codes, and SDK examples for C#, Java, Python, and more."  
weight: 100  
---  

## **Excel API: Move Folder**

### API Endpoint  

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Prerequisites**  

- Aspose.Cells Cloud SDK version 20.10 or later.  
- API version **v4.0**.  
- A valid OAuth 2.0 access token that includes the **Cells** scope.  
- Source and destination storages must belong to the same Aspose Cloud account.  

### **Authentication**  

All requests must contain an `Authorization` header:

```
Authorization: Bearer {access_token}
```

The token is obtained through the Aspose Cloud OAuth flow.

### **Function Description**  

This API moves a folder from one location to another within Aspose.Cells Cloud storage. It helps organise files and manage cloud storage efficiently.

### Sample Request  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Accept: application/json"
```

### Sample Response  

**Status:** `200 OK`  

**Body:** *(empty)*  

```json
{}
```

### The request parameters of **moveFolder** API are  

| Parameter Name   | Type   | Location | Description |
|------------------|--------|----------|-------------|
| srcPath          | string | Path     | The full path of the folder to be moved, e.g., `FolderA/`. |
| destPath         | string | Query    | The target path where the folder will be moved, e.g., `FolderB/`. |
| srcStorageName   | string | Query    | (Optional) Name of the source storage. |
| destStorageName  | string | Query    | (Optional) Name of the destination storage. |

**Parameter details**

- **srcPath** – required. The source folder path.  
- **destPath** – required. The destination folder path.  
- **srcStorageName** – optional. Identifier of the source storage.  
- **destStorageName** – optional. Identifier of the destination storage.  

### **Response Description**  

On success the API returns an empty response body (`200 OK`). Errors are returned as JSON objects containing an `error` field.

### **Error Handling**  

| HTTP Status | Error Code               | Description                                 |
|-------------|--------------------------|---------------------------------------------|
| 400         | `FolderAlreadyExists`    | Destination folder already exists.          |
| 400         | `InvalidPath`            | Source or destination path is invalid.      |
| 401         | `Unauthorized`           | Missing or invalid access token.            |
| 404         | `FolderNotFound`         | Source folder does not exist.               |
| 500         | `InternalError`          | Unexpected server error.                    |

### **Next Steps**  

1. Call **Get Files List** to verify that the folder has been moved.  
2. To rename a folder, invoke **Move Folder** with a different `destPath`.  
3. Explore related operations such as **Copy Folder** and **Delete Folder**.  

## OpenAPI Specification  

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK  

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

### C# Example  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi();
apiInstance.MoveFolder("FolderA", "FolderB", null, null, "YOUR_ACCESS_TOKEN");
```

### Java Example  

```java
import com.aspose.cells.cloud.api.CellsApi;

CellsApi api = new CellsApi();
api.moveFolder("FolderA", "FolderB", null, null, "YOUR_ACCESS_TOKEN");
```

### PHP Example  

```php
<?php
require_once 'vendor/autoload.php';

$apiInstance = new Aspose\Cells\Cloud\Api\CellsApi();
$apiInstance->moveFolder("FolderA", "FolderB", null, null, "YOUR_ACCESS_TOKEN");
?>
```

### Ruby Example  

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new
api.move_folder('FolderA', 'FolderB', nil, nil, 'YOUR_ACCESS_TOKEN')
```

### Node.js (TypeScript) Example  

```typescript
import { CellsApi } from "asposecellscloud";

const api = new CellsApi();
api.moveFolder("FolderA", "FolderB", undefined, undefined, "YOUR_ACCESS_TOKEN");
```

### Python Example  

```python
from asposecellscloud import CellsApi

api = CellsApi()
api.move_folder("FolderA", "FolderB", None, None, "YOUR_ACCESS_TOKEN")
```

### Perl Example  

```perl
use AsposeCellsCloud::CellsApi;

my $api = AsposeCellsCloud::CellsApi->new();
$api->move_folder('FolderA', 'FolderB', undef, undef, 'YOUR_ACCESS_TOKEN');
```

### Go Example  

```go
package main

import (
    "github.com/aspose-cells-cloud/asposecellscloud-go/v4"
)

func main() {
    api := cells.NewCellsApi()
    api.MoveFolder("FolderA", "FolderB", "", "", "YOUR_ACCESS_TOKEN")
}
```

### FAQ  

**Q:** *How do I move a folder to a different storage account?*  
**A:** Provide the `srcStorageName` and `destStorageName` query parameters in the request. Both storages must belong to the same Aspose Cloud account.  

**Q:** *What response do I receive when the move succeeds?*  
**A:** A `200 OK` status with an empty JSON body (`{}`).  

**Q:** *What happens if the destination folder already exists?*  
**A:** The API returns `400 Bad Request` with the error code `FolderAlreadyExists`.  