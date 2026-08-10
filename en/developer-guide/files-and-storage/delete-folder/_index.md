---
title: "Delete Folder – Aspose.Cells Cloud API | Remove Folders via REST"
description: "Learn how to delete a folder (optionally recursively) from Aspose.Cells Cloud storage using the DELETE /v4.0/cells/storage/folder/{path} endpoint. Includes request syntax, parameters, authentication, sample code, and error handling."
keywords: "Aspose.Cells, delete folder, cloud storage, API, REST, Excel, file management"
slug: delete-folder
date: 2026-07-30
---

# Delete Folder – Aspose.Cells Cloud API

Remove a folder (optionally all of its contents) from Aspose.Cells Cloud storage.

---

## Overview

The **Delete Folder** operation permanently removes a folder from a storage account used by Aspose.Cells Cloud.  
You can delete an empty folder or, by setting the `recursive` flag to `true`, delete the folder together with every file and sub‑folder it contains. This endpoint is commonly used in cleanup scripts, automated workflows, or when temporary directories are no longer needed.

---

## HTTP Request

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – the full path of the folder to delete (URL‑encoded).

### Required HTTP Headers

| Header            | Value                              | Description                              |
|-------------------|------------------------------------|------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | JWT token obtained from the auth service. |
| `Accept`          | `application/json`                | Expected response format.                |
| `Content-Type`    | `application/json` *(optional)*   | Not required for DELETE, but may be sent. |

---

## Authentication

Aspose.Cells Cloud uses **JWT token‑based authentication**.  
Obtain an access token via the [authentication endpoint](/authentication/) and include it in the `Authorization` header as shown above.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Parameters

| Name          | Type    | Location | Required | Description                                                               |
|---------------|---------|----------|----------|---------------------------------------------------------------------------|
| `path`        | string  | Path     | Yes      | Path of the folder to delete (URL‑encoded).                               |
| `storageName` | string  | Query    | No       | Name of the storage that contains the folder. If omitted, the default storage is used. |
| `recursive`   | boolean | Query    | No       | `true` → delete the folder **and all of its contents**. Default is `false`. |

**Example query string**

```
?storageName=MyStorage&recursive=true
```

---

## Request Example (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Response

A successful request returns **HTTP 200 OK** with an empty JSON object:

```json
{}
```

No additional payload is provided because the operation’s result is binary – the folder is either removed or an error is returned.

---

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

When an error occurs, the body contains a JSON object with `code` and `message` fields describing the problem.

---

## SDK Code Samples

The following examples demonstrate how to call **Delete Folder** with the officially supported SDKs. Replace `{access_token}` and parameter values with your own.

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configure API client
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Delete folder (recursive)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// Initialise API client
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// Configure
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Delete folder recursively
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Folder deleted.";
} catch (Exception $e) {
    echo 'Exception when calling FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Folder deleted.'
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Folder deleted'))
    .catch(err => console.error('Error:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Folder deleted")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Folder deleted.\n";
};
if ($@) {
    warn "Error deleting folder: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println("Folder deleted")
}
```
</details>

---

## See Also

- **[Create Folder](/create-folder/)** – Create a new folder in cloud storage.  
- **[Copy Folder](/copy-folder/)** – Duplicate a folder and its contents.  
- **[Move Folder](/move-folder/)** – Relocate a folder to a different path.  
- **[OpenAPI Specification]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">DeleteFolder operation</a> (interactive API explorer).

---

## SEO & Accessibility Checklist (internal)

- **Title & H1** use the correct en‑dash (`–`) and contain the primary keyword *Delete Folder*.  
- All headings follow a logical hierarchy (`H1 → H2 → H3`).  
- No UTF‑8 encoding artifacts remain.  
- Meta keywords consolidated into a single, clean list (or omitted if preferred).  
- External links include `rel="noopener noreferrer"` for security.  
- UI icons and language flags (if rendered on the page) should carry `aria-label`/`alt` attributes (e.g., `aria-label="English (US)"`).  
- `<link rel="alternate" hreflang="xx" href="…">` tags are recommended in the page head for each language version.

---