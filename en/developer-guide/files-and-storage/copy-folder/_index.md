---
title: "Copy Folder"
linktitle: "Copy Folder"
type: docs
url: /copy-folder/
description: "Automate Excel folder backups and reorganization in the cloud using Aspose.Cells Cloud’s CopyFolder REST API. Includes full API reference, cURL examples, and SDK code snippets in 8 languages."
keywords: "copy folder, Aspose.Cells Cloud, REST API, cloud storage, spreadsheet management, folder duplication"
date: 2024-03-15
lastmod: 2024-06-15
robots: index, follow
weight: 100
---

The **CopyFolder** API duplicates an existing folder within Aspose.Cells Cloud storage. This operation is useful for creating backups, reorganizing data structures, or preparing folder hierarchies for batch processing—without manual file transfers.

## Prerequisites

To use the CopyFolder API, ensure you have:

- A valid Aspose.Cells Cloud account.
- An API key and App SID (obtained from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/)).
- Familiarity with [JWT-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

> **Note:** Folder copy operations are subject to your storage quota and API rate limits (typically 20 requests/second per account).

## Excel API: Copy Folder

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### Request Parameters

| Parameter Name    | Required | Type   | Location | Description |
|-------------------|----------|--------|----------|-------------|
| `srcPath`         | Yes      | String | Path     | The path of the source folder to copy (e.g., `"source/backup"`). |
| `destPath`        | Yes      | String | Query    | The path where the new folder will be created (e.g., `"dest/backup"`). |
| `srcStorageName`  | No       | String | Query    | Name of the storage containing the source folder (defaults to first configured storage). |
| `destStorageName` | No       | String | Query    | Name of the destination storage (defaults to `srcStorageName` if omitted). |

### Authentication

All requests require a valid JWT access token in the `Authorization` header:

```http
Authorization: Bearer <access_token>
```

For details on obtaining and refreshing tokens, see [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### cURL Example

```bash
curl -v -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy&srcStorageName=FirstStorage&destStorageName=SecondStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json"
```

### Response

A successful request returns **HTTP 200** with an empty JSON body:

```json
{}
```

### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Folder copied successfully. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., `srcPath` or `destPath` missing, or invalid folder path). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token. |
| 403  | Forbidden             | Insufficient permissions for source/destination storage. |
| 404  | Not Found             | Source folder does not exist. |
| 409  | Conflict              | Destination folder already exists (overwrites not supported). |
| 500  | Internal Server Error | Unexpected server-side failure. |

> **Note:** Copying a folder to a location where a folder already exists will return `409 Conflict`. Use `DeleteFolder` first if replacement is intended.

## SDK Examples

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

## Related APIs

- [DeleteFolder](/delete-folder/) – Remove an empty folder.
- [GetFolder](/get-folder/) – Retrieve details of a folder (including contents).
- [PutCreateFolder](/put-create-folder/) – Create a new folder.

## OpenAPI Specification

The API is formally defined in the [OpenAPI Specification for CopyFolder](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder). You can explore and test the endpoint directly in your browser using the interactive Swagger UI.