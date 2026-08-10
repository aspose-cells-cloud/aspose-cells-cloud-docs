---
title: "Aspose.Cells Cloud API – Get Files List (Folder Contents)"
description: "Retrieve a list of files and sub‑folders from a specific folder in Aspose.Cells Cloud storage."
keywords:
  - Aspose.Cells
  - API
  - Get Files List
  - Cloud Storage
  - Excel
  - REST
type: docs
weight: 100
---

# Aspose.Cells Cloud API – Get Files List (Folder Contents)

## Overview
The **Get Files List** operation returns the collection of files and sub‑folders stored in a specified folder of Aspose.Cells Cloud storage.  
It is the primary entry point for browsing cloud‑based Excel workbooks, archives, and other supported file types.

> **Prerequisites**
> - A valid **JWT access token** (see [Authenticating API requests](/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
> - An existing storage account (default storage is used if `storageName` is omitted).  

---

## Endpoint

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

- **{path}** – URL‑encoded path of the folder whose contents you want to list.

### Request URL Template

```
https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName={storageName}&pageSize={pageSize}&pageNumber={pageNumber}
```

---

## Authentication

All Aspose.Cells Cloud APIs require **Bearer token** authentication.

```http
Authorization: Bearer <your_access_token>
```

---

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

## Request Parameters

| Name          | Location | Type    | Required | Description |
|---------------|----------|---------|----------|-------------|
| **path**      | Path     | string  | Yes      | Path to the folder in cloud storage. |
| **storageName** | Query   | string  | No       | Name of the storage to use. If omitted, the default storage is used. |
| **pageSize**  | Query    | integer | No       | Maximum number of items to return per page (default: 100). |
| **pageNumber**| Query    | integer | No       | Page number to retrieve (starting at 1, default: 1). |

---

## Sample Request (cURL)

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

> **Note**: Replace `{path}`, `MyStorage`, and `<your_access_token>` with your actual values.  
> The `path` parameter must be URL‑encoded (e.g., `My%20Folder/Reports`).

---

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
---

## Successful Response (JSON)

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

- **Value** – Array of `StorageFile` objects. Each object contains:
  - `Name` – File or folder name.
  - `IsFolder` – `true` if the entry is a folder.
  - `Size` – Size in bytes (folders report `0`).
  - `ModifiedDate` – Last modification timestamp (ISO 8601).

---

## Error Response Example

```json
{
  "Code": 404,
  "Message": "Folder not found."
}
```

---

## SDK Samples

The following code snippets demonstrate how to call **Get Files List** using the official Aspose.Cells Cloud SDKs.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new FolderApi();
var request = new GetFilesListRequest(
    path: "MyFolder",
    storageName: "MyStorage",
    pageSize: 100,
    pageNumber: 1
);

var response = apiInstance.GetFilesList(request);
Console.WriteLine(response);
```

### Java

```java
import com.aspose.cells.cloud.api.FolderApi;
import com.aspose.cells.cloud.model.requests.GetFilesListRequest;

FolderApi api = new FolderApi();
GetFilesListRequest request = new GetFilesListRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .pageSize(100)
        .pageNumber(1);

var result = api.getFilesList(request);
System.out.println(result);
```

### Python

```python
from asposecellscloud import FolderApi
from asposecellscloud.models import GetFilesListRequest

api = FolderApi()
request = GetFilesListRequest(
    path='MyFolder',
    storage_name='MyStorage',
    page_size=100,
    page_number=1
)

response = api.get_files_list(request)
print(response)
```

### Node.js (TypeScript)

```typescript
import { FolderApi, GetFilesListRequest } from "asposecellscloud";

const api = new FolderApi();
const request = new GetFilesListRequest({
    path: "MyFolder",
    storageName: "MyStorage",
    pageSize: 100,
    pageNumber: 1
});

api.getFilesList(request).then(result => console.log(result));
```

### PHP

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Model\Requests\GetFilesListRequest;

$apiInstance = new FolderApi();
$request = new GetFilesListRequest(
    "MyFolder",          // path
    "MyStorage",         // storageName (optional)
    100,                 // pageSize (optional)
    1                    // pageNumber (optional)
);

$response = $apiInstance->getFilesList($request);
print_r($response);
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::FolderApi.new
request = AsposeCellsCloud::GetFilesListRequest.new(
  path: 'MyFolder',
  storage_name: 'MyStorage',
  page_size: 100,
  page_number: 1
)

result = api_instance.get_files_list(request)
puts result
```

### Go

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v4"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v4/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_access_token>")
    client := api.NewAPIClient(cfg)

    request := client.FolderApi.GetFilesList(
        "MyFolder",   // path
        "MyStorage",  // storageName (optional)
        100,          // pageSize (optional)
        1,            // pageNumber (optional)
    )
    result, _, err := request.Execute()
    if err != nil {
        panic(err)
    }
    fmt.Printf("%+v\n", result)
}
```

### Perl

```perl
#!/usr/bin/perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Object::GetFilesListRequest;

my $api_instance = AsposeCellsCloud::FolderApi->new();
my $request = AsposeCellsCloud::Object::GetFilesListRequest->new(
    path         => 'MyFolder',
    storage_name => 'MyStorage',
    page_size    => 100,
    page_number  => 1,
);

my $result = $api_instance->get_files_list(request => $request);
print $result;
```

---

## Related API Endpoints

- **Copy File** – `POST /cells/storage/file/copy`  
- **Delete Folder** – `DELETE /cells/storage/folder/{path}`  
- **Upload File** – `PUT /cells/storage/file/{path}`  

Explore these links to build a complete file‑management workflow.

---

## Additional Resources

- **OpenAPI Specification**: <https://reference.aspose.cloud/cells/#/FolderController/GetFilesList>  
- **SDK Repository**: <https://github.com/aspose-cells-cloud>  
- **Authentication Guide**: <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  

---

*Document last updated: 2026‑07‑30*  