---
title: "Delete Folder"
second_title: "Developer Guide"
linktitle: "Delete folder"
type: docs
url: /delete-folder/
description: "Delete folders in Aspose.Cells Cloud storage using REST API with optional recursive removal."
keywords: "delete folder, Aspose.Cells Cloud, REST API, remove folder, Excel cloud storage"
weight: 30
ArticleTitle: "Delete Folder in Aspose.Cells Cloud Storage via REST API"
---
The **DeleteFolder** API (`DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}`) removes a specified folder from Aspose.Cells Cloud storage, with optional recursive deletion of its contents via the `recursive` query parameter; it accepts the folder path as a required path parameter and supports specifying a custom storage name with the `storageName` query parameter.

---

## Overview

The **Delete Folder** operation permanently removes a folder from a storage account used by Aspose.Cells Cloud.  
You can delete an empty folder or, by setting the `recursive` flag to `true`, delete the folder together with every file and sub‑folder it contains. This endpoint is commonly used in cleanup scripts, automated workflows, or when temporary directories are no longer needed.

---

## The Delete Folder Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### Security and Authentication

Aspose.Cells Cloud uses **JWT token‑based authentication**.  
Obtain an access token via the [authentication endpoint](/authentication/) and include it in the `Authorization` header as shown above.

```bash
-H "Authorization: Bearer {access_token}"
```

> **Tip**: Replace `{access_token}` with your actual token or use environment variables (e.g., `os.Getenv("ASPOSE_CLOUD_ACCESS_TOKEN")` in Node.js/Python) to avoid hardcoding credentials.

---

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| path | String | Path | - |
| storageName | String | Query | - |
| recursive | Boolean | Query | - |

**Example query string**

```
?storageName=MyStorage&recursive=true
```

---

### Response

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

_`{path}`_ – the full path of the folder to delete (URL‑encoded).

### Required HTTP Headers

| Header          | Value                           | Description                               |
| --------------- | ------------------------------- | ----------------------------------------- |
| `Authorization` | `Bearer {access_token}`         | JWT token obtained from the auth service. |
| `Accept`        | `application/json`              | Expected response format.                 |
| `Content-Type`  | `application/json` _(optional)_ | Not required for DELETE, but may be sent. |

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

| Code | Meaning               | Description                    |
| ---- | --------------------- | ------------------------------ |
| 200  | OK                    | Folder deleted successfully.   |
| 400  | Bad Request           | Missing or invalid parameters. |
| 401  | Unauthorized          | Invalid or missing JWT token.  |
| 404  | Not Found             | Folder or storage not found.   |
| 500  | Internal Server Error | Unexpected server error.       |

When an error occurs, the body contains a JSON object with `code` and `message` fields describing the problem.

---

## How to Use the Delete Folder API with SDKs?

### Delete Folder API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/DeleteFolder" rel="noopener noreferrer">Delete Folder API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{</tab>}}
{{< /tabs >}}
