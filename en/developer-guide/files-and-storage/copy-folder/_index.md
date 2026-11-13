---
title: "Copy Folder"
linktitle: "Copy Folder"
type: docs
url: /copy-folder/
description: "Copy an Excel folder in Aspose.Cells Cloud storage via the CopyFolder REST API with cURL and 8 SDKs"
keywords: "copy folder, Aspose.Cells Cloud, REST API, cloud storage, spreadsheet management, folder duplication"
weight: 100
ArticleTitle: "Copy Folder API in Aspose.Cells Cloud: Backup & Reorganize Excel Folders"
---
The **CopyFolder** API (`PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}`) duplicates an existing folder in Aspose.Cells Cloud storage from a source path (`srcPath`) to a destination path (`destPath`), supporting optional storage name parameters for cross-storage operations; this enables efficient backup creation, folder reorganization, and preparation of hierarchical structures for batch processing without manual file transfers.

## The Copy Folder Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### Security and Authentication

All requests require a valid JWT access token in the `Authorization` header:

```http
Authorization: Bearer <access_token>
```

For details on obtaining and refreshing tokens, see [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| srcPath | String | Path | - |
| destPath | String | Query | - |
| srcStorageName | String | Query | - |
| destStorageName | String | Query | - |

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

A successful request returns **HTTP 200** with an empty JSON body:

### cURL Example

```bash
curl -v -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy&srcStorageName=FirstStorage&destStorageName=SecondStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json"
```

### HTTP Status Codes

| Code | Meaning               | Description                                                                                    |
| ---- | --------------------- | ---------------------------------------------------------------------------------------------- |
| 200  | OK                    | Folder copied successfully.                                                                    |
| 400  | Bad Request           | Missing or invalid parameters (e.g., `srcPath` or `destPath` missing, or invalid folder path). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token.                                                        |
| 403  | Forbidden             | Insufficient permissions for source/destination storage.                                       |
| 404  | Not Found             | Source folder does not exist.                                                                  |
| 409  | Conflict              | Destination folder already exists (overwrites not supported).                                  |
| 500  | Internal Server Error | Unexpected server-side failure.                                                                |

> **Note:** Copying a folder to a location where a folder already exists will return `409 Conflict`. Use `DeleteFolder` first if replacement is intended.

## Related APIs

- [DeleteFolder](/delete-folder/) – Remove an empty folder.
- [GetFolder](/get-folder/) – Retrieve details of a folder (including contents).
- [PutCreateFolder](/put-create-folder/) – Create a new folder.

## OpenAPI Specification

The API is formally defined in the [OpenAPI Specification for CopyFolder](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder). You can explore and test the endpoint directly in your browser using the interactive Swagger UI.

## How to Use the Copy Folder API with SDKs?

### Copy Folder API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/CopyFolder" rel="noopener noreferrer">Copy Folder API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

Using an SDK is the recommended approach for integrating folder copy operations. SDKs handle authentication, serialization, and error handling, letting you focus on business logic.

The following examples demonstrate copying `"MyFolder"` to `"MyFolderCopy"` in the same storage:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}

```csharp
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/blob/master/Cells.Cloud.Examples/Examples/Folders/CopyFolder.cs
var cellsApi = new CellsApi(clientId, clientSecret, basePath, baseAddress);
cellsApi.CopyFolder("MyFolder", "MyFolderCopy");
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```java
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Examples/src/main/java/Example40_CopyFolder.java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
cellsApi.copyFolder("MyFolder", "MyFolderCopy", null, null);
```

{{< /tab >}}
{{< tab tabNum="3" >}}

```php
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/Examples/Folder/CopyFolder.php
$cellsApi = new CellsApi($clientId, $clientSecret);
$cellsApi->copyFolder("MyFolder", "MyFolderCopy");
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```ruby
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/blob/master/examples/folder/copy_folder.rb
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
cells_api.copy_folder("MyFolder", "MyFolderCopy")
```

{{< /tab >}}
{{< tab tabNum="5" >}}

```typescript
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/blob/master/examples/folder/copyFolder.ts
const cellsApi = new CellsApi(clientId, clientSecret);
await cellsApi.copyFolder("MyFolder", "MyFolderCopy");
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```python
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/blob/master/examples/folder/copy_folder.py
cells_api = CellsApi(client_id, client_secret)
cells_api.copy_folder("MyFolder", "MyFolderCopy")
```

{{< /tab >}}
{{< tab tabNum="7" >}}

```perl
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/blob/master/examples/folder/copy_folder.pl
my $cells_api = Aspose::Cells::Cloud::CellsApi->new($client_id, $client_secret);
$cells_api->copy_folder("MyFolder", "MyFolderCopy");
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```go
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/blob/master/examples/folder/copy_folder.go
cellsAPI := cells.NewCellsApi(clientId, clientSecret)
_, err := cellsAPI.CopyFolder(context.Background(), "MyFolder", &cells.CopyFolderOptions{DestPath: "MyFolderCopy"})
```

{{< /tab >}}
{{< /tabs >}}

For more code samples, see the [Aspose.Cells Cloud SDK GitHub repository](https://github.com/aspose-cells-cloud).

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}
