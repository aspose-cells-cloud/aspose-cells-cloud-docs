---
title: "Aspose.Cells Cloud File Copy API - An interface for fast copying and batch operations of Excel files in the cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management Solution – Detailed Explanation of Aspose.Cells Copy File API’s Batch Copy Functionality"
linktitle: "Copy File"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel file copy, Cloud storage, REST API"
description: "Learn how to use the Aspose.Cells Cloud CopyFile API to efficiently duplicate Excel files and manage them across storage locations."
weight: 100
---

## **Excel API: Copy File**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

> **Note:** All Aspose Cloud endpoints require HTTPS.

### **Function Description**

The **copyFile** API allows users to duplicate an Excel file from a specified source path to a destination path, supporting various storage options.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

**Prerequisites**

- An active Aspose Cloud account.  
- A generated JWT access token (see the example below).  
- Optional: Storage name(s) if you are using a custom cloud storage.

**Sample request to obtain a JWT token**

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id={YOUR_CLIENT_ID}&client_secret={YOUR_CLIENT_SECRET}"
```

The response contains the `access_token` that must be included in the `Authorization` header of subsequent API calls.

### The request parameters of the **copyFile** API are

| Parameter Name  | Type   | Path/Query String/HTTPBody | Description                                        |
| --------------- | ------ | -------------------------- | -------------------------------------------------- |
| srcPath         | String | Path                       | The source path of the file to be copied.          |
| destPath        | String | Query                      | The destination path where the file will be saved. |
| srcStorageName  | String | Query                      | The name of the source storage.                    |
| destStorageName | String | Query                      | The name of the destination storage.               |
| versionId       | String | Query                      | Optional version ID of the file to copy.           |

**Full request example**

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Typical responses**

- **200 OK** – File copied successfully (empty body).  
- **404 Not Found** – Example error payload:

```json
{
  "error": {
    "code": "FileNotFound",
    "message": "Source file '/MyFolder/Source.xlsx' does not exist."
  }
}
```

### **Response Description**

The operation returns no content on success. Typical HTTP status codes are:

| Status Code | Meaning                              |
| ----------- | ------------------------------------ |
| 200 OK      | File copied successfully.           |
| 400 Bad Request | Invalid request parameters.      |
| 401 Unauthorized | Authentication failed or token missing. |
| 404 Not Found | Source file not found.             |
| 500 Internal Server Error | Unexpected server error. |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/CopyFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to accelerate development. An SDK manages low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
```csharp
// Example40_CopyFile.cs
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var response = api.CopyFile("MyFolder/Source.xlsx", "MyFolder/Dest.xlsx");
Console.WriteLine("Copy operation completed.");
```
{{</tab>}}
{{<tab tabNum="2" >}}
```java
// Example40_CopyFile.java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("client_id", "client_secret");
api.copyFile("MyFolder/Source.xlsx", "MyFolder/Dest.xlsx");
System.out.println("Copy operation completed.");
```
{{</tab>}}
{{<tab tabNum="3" >}}
```php
// Example40_CopyFile.php
require_once 'vendor/autoload.php';
use Aspose\Cells\Cloud\Api\CellsApi;

$api = new CellsApi("client_id", "client_secret");
$api->copyFile("MyFolder/Source.xlsx", "MyFolder/Dest.xlsx");
echo "Copy operation completed.";
```
{{</tab>}}
{{<tab tabNum="4" >}}
```ruby
# Example40_CopyFile.rb
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('client_id', 'client_secret')
api.copy_file('MyFolder/Source.xlsx', 'MyFolder/Dest.xlsx')
puts 'Copy operation completed.'
```
{{</tab>}}
{{<tab tabNum="5" >}}
```javascript
// Example40_CopyFile.ts (Node.js)
const { CellsApi } = require("@aspose/cells-cloud");
const api = new CellsApi("client_id", "client_secret");
api.copyFile("MyFolder/Source.xlsx", "MyFolder/Dest.xlsx")
   .then(() => console.log("Copy operation completed."))
   .catch(err => console.error(err));
```
{{</tab>}}
{{<tab tabNum="6" >}}
```python
# Example40_CopyFile.py
from asposecellscloud import CellsApi

api = CellsApi("client_id", "client_secret")
api.copy_file("MyFolder/Source.xlsx", "MyFolder/Dest.xlsx")
print("Copy operation completed.")
```
{{</tab>}}
{{<tab tabNum="7" >}}
```perl
# Example40_CopyFile.pl
use Aspose::Cells::Cloud::Api::CellsApi;

my $api = Aspose::Cells::Cloud::Api::CellsApi->new('client_id', 'client_secret');
$api->copy_file('MyFolder/Source.xlsx', 'MyFolder/Dest.xlsx');
print "Copy operation completed.\n";
```
{{</tab>}}
{{<tab tabNum="8" >}}
```go
// Example40_CopyFile.go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    api := asposecellscloud.NewCellsApi("client_id", "client_secret")
    _, err := api.CopyFile("MyFolder/Source.xlsx", "MyFolder/Dest.xlsx")
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Copy operation completed.")
    }
}
```
{{</tab>}}
{{< /tabs >}}

### See also

- **Copy Folder API** – <a href="/copy-folder/">Copy Folder</a>  
- **Move File API** – <a href="/move-file/">Move File</a>  
- **Delete File API** – <a href="/delete-file/">Delete File</a>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Aspose.Cells Cloud File Copy API",
  "description": "Documentation for the CopyFile API that enables fast copying of Excel files in Aspose.Cells Cloud storage.",
  "url": "https://docs.aspose.cloud/cells/copy-file/",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Copy File", "item": "https://docs.aspose.cloud/cells/copy-file/" }
    ]
  }
}
</script>