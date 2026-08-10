---
title: "Object Exists API – Check File/Folder Presence in Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Object Exists API – Verify File or Folder Presence in Aspose.Cells Cloud"
linktitle: "Object Exists"
type: docs
url: /object-exists/
keywords: "Aspose.Cells, cloud storage, object exists, file existence, folder existence, API"
description: "Use the Object Exists API to quickly verify whether a file or folder exists in Aspose.Cells Cloud storage. Supports optional storage name and version ID, and works with versioned objects."
weight: 100
---

## **Excel API: Object Exists**

The **Object Exists API** lets developers determine whether a specific file or folder is present in Aspose.Cells Cloud storage. It returns a simple Boolean indicating existence and whether the path points to a folder.

### Web API

```http
GET https://api.aspose.cloud/v5.0/cells/storage/exist/{path}
```

_`{path}`_ is the full path to the file or folder in storage.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Location | Required | Description                                                         |
| -------------- | ------ | -------- | -------- | ------------------------------------------------------------------- |
| `path`         | string | Path     | Yes      | Full path to the file or folder.                                    |
| `storageName`  | string | Query    | No       | Name of the storage; defaults to the primary storage if omitted.    |
| `versionId`    | string | Query    | No       | Specific version identifier of the file (if versioning is enabled). |

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
### Response Description

A successful call returns a JSON payload with two properties:

```json
{
  "Exists": true,
  "IsFolder": false
}
```

- **Exists** – `true` if the file or folder exists; otherwise `false`.
- **IsFolder** – `true` when the path points to a folder; `false` for a file.

### Notes & Limitations

- Rate limits are applied per account; consult the **[Rate Limits](/rate-limits/)** page for exact values.  
- If `storageName` is omitted, the default storage configured for the account is used.  
- The API currently supports version 5.0; older version paths (`/v4.0/`) are deprecated.  

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs. If a Gist fails to load, a static example is provided below each tab.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ObjectExists.cs" >}}
```csharp
// Fallback C# example
var api = new CellsApi("client_id", "client_secret");
var response = api.Storage.ObjectExists("folder/file.xlsx");
Console.WriteLine($"Exists: {response.Exists}, IsFolder: {response.IsFolder}");
```
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ObjectExists.java" >}}
```java
// Fallback Java example
CellsApi api = new CellsApi("client_id", "client_secret");
ObjectExistResponse response = api.storage().objectExists("folder/file.xlsx");
System.out.println("Exists: " + response.getExists() + ", IsFolder: " + response.getIsFolder());
```
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ObjectExists.php" >}}
```php
// Fallback PHP example
$api = new CellsApi($clientId, $clientSecret);
$response = $api->storage->objectExists('folder/file.xlsx');
echo "Exists: {$response->getExists()}, IsFolder: {$response->getIsFolder()}";
```
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ObjectExists.rb" >}}
```ruby
# Fallback Ruby example
api = AsposeCellsCloud::StorageApi.new($client_id, $client_secret)
response = api.object_exists('folder/file.xlsx')
puts "Exists: #{response.exists}, IsFolder: #{response.is_folder}"
```
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ObjectExists.ts" >}}
```javascript
// Fallback Node.js example
const CellsApi = require('asposecellscloud');
const api = new CellsApi('client_id', 'client_secret');
api.storage.objectExists('folder/file.xlsx')
  .then(res => console.log(`Exists: ${res.exists}, IsFolder: ${res.isFolder}`));
```
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ObjectExists.py" >}}
```python
# Fallback Python example
api = CellsApi(client_id, client_secret)
response = api.storage.object_exists('folder/file.xlsx')
print(f'Exists: {response.exists}, IsFolder: {response.is_folder}')
```
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ObjectExists.pl" >}}
```perl
# Fallback Perl example
my $api = AsposeCellsCloud::StorageApi->new($client_id, $client_secret);
my $response = $api->object_exists('folder/file.xlsx');
print "Exists: $response->{Exists}, IsFolder: $response->{IsFolder}\n";
```
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ObjectExists.go" >}}
```go
// Fallback Go example
api := asposecellscloud.NewCellsApi(clientId, clientSecret)
response, _ := api.Storage.ObjectExists("folder/file.xlsx")
fmt.Printf("Exists: %v, IsFolder: %v\n", response.Exists, response.IsFolder)
```
{{</tab>}}
{{< /tabs >}}

---

[← Back to Files and Storage](../)