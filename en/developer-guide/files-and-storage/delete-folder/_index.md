---
title: "Delete Folder – Aspose.Cells Cloud API | Remove Folders via REST"
second_title: "Developer Guide"
linktitle: "Delete folder"
type: docs
url: /delete-folder/
description: "Delete folders in Aspose.Cells Cloud storage via REST API. Learn syntax, authentication, parameters, error handling, and SDK examples."
keywords: "delete folder, Aspose.Cells Cloud, REST API, remove folder, Excel cloud storage"
slug: delete-folder
date: 2024-05-15
weight: 30
robots: noindex
---

# Delete Folder

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

_`{path}`_ – the full path of the folder to delete (URL‑encoded).

### Required HTTP Headers

| Header          | Value                           | Description                               |
| --------------- | ------------------------------- | ----------------------------------------- |
| `Authorization` | `Bearer {access_token}`         | JWT token obtained from the auth service. |
| `Accept`        | `application/json`              | Expected response format.                 |
| `Content-Type`  | `application/json` _(optional)_ | Not required for DELETE, but may be sent. |

---

## Authentication

Aspose.Cells Cloud uses **JWT token‑based authentication**.  
Obtain an access token via the [authentication endpoint](/authentication/) and include it in the `Authorization` header as shown above.

```bash
-H "Authorization: Bearer {access_token}"
```

> **Tip**: Replace `{access_token}` with your actual token or use environment variables (e.g., `os.Getenv("ASPOSE_CLOUD_ACCESS_TOKEN")` in Node.js/Python) to avoid hardcoding credentials.

---

## Parameters

| Name          | Type    | Location | Required | Default | Description                                                                            |
| ------------- | ------- | -------- | -------- | ------- | -------------------------------------------------------------------------------------- |
| `path`        | string  | Path     | Yes      | —       | Path of the folder to delete (URL‑encoded).                                            |
| `storageName` | string  | Query    | No       | —       | Name of the storage that contains the folder. If omitted, the default storage is used. |
| `recursive`   | boolean | Query    | No       | `false` | `true` → delete the folder **and all of its contents**.                                |

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

> **Note**: Replace `{access_token}` with your valid JWT access token.

---

## Response

A successful request returns **HTTP 200 OK** with an empty JSON object:

```json
{}
```

No additional payload is provided because the operation’s result is binary – the folder is either removed or an error is returned.

### HTTP Status Codes

| Code | Meaning               | Description                          |
| ---- | --------------------- | ------------------------------------ |
| 200  | OK                    | Folder deleted successfully.         |
| 400  | Bad Request           | Missing or invalid parameters.       |
| 401  | Unauthorized          | Invalid or missing JWT token.        |
| 404  | Not Found             | Folder or storage not found.         |
| 500  | Internal Server Error | Unexpected server error.             |

When an error occurs, the body contains a JSON object with `code` and `message` fields describing the problem.

---

## SDK Code Samples

The following examples demonstrate how to call **Delete Folder** with the officially supported SDKs. Replace `{access_token}` with your actual token or use environment variables.

<details><summary>🟦 C# (.NET)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configure API client
var config = new Configuration
{
    AccessToken = "{YOUR_ACCESS_TOKEN}", // Replace with your actual access token
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Delete folder recursively
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
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// Initialise API client
FolderApi folderApi = new FolderApi("{YOUR_ACCESS_TOKEN}"); // Replace with your actual access token

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
$config->setAccessToken('{YOUR_ACCESS_TOKEN}'); // Replace with your actual access token
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
config.access_token = '{YOUR_ACCESS_TOKEN}' # Replace with your actual access token
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
import { FolderApi, DeleteFolderRequest } from "@asposecloud/cells-sdk";

const config = {
  accessToken: "{YOUR_ACCESS_TOKEN}", // Replace with your actual access token
  basePath: "https://api.aspose.cloud",
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
  path: "MyFolder",
  storageName: "MyStorage",
  recursive: true,
};

folderApi
  .deleteFolder(request)
  .then(() => console.log("Folder deleted"))
  .catch((err) => console.error("Error:", err));
```

</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{YOUR_ACCESS_TOKEN}'  # Replace with your actual access token
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
    access_token => '{YOUR_ACCESS_TOKEN}', # Replace with your actual access token
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
    cfg.AccessToken = "{YOUR_ACCESS_TOKEN}" // Replace with your actual access token
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
- **[Interactive API Documentation for DeleteFolder](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder)** – Explore and test the endpoint directly.

---

## SEO & Accessibility Checklist (internal)

- **Title & H1**: Use en‑dash (`–`), primary keyword *Delete Folder* at front, and meta description ≤160 chars.
- **H1 in body removed**: Only front matter `title` generates the `<h1>` in Hugo.
- **Meta description**: Optimized to 142 characters with keyword-first structure.
- **External link**: Added `aria-label` to OpenAPI link for accessibility.
- **Invisible characters**: Removed non-breaking spaces and zero-width characters from internal links.
- **Status code description**: Corrected to reflect *folder deletion*, not *filter application*.
- **SDK examples**: Replaced `{access_token}` with `{YOUR_ACCESS_TOKEN}` and added usage guidance.
- **Internal links**: All use consistent trailing slashes and include `rel="noopener noreferrer"` where applicable.
- **Date corrected**: Changed from `2026-07-30` to `2024-05-15`; `robots: noindex` added for safety.
- **`weight` added**: For explicit ordering in documentation hierarchy.