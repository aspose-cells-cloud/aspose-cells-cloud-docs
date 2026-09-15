---
url: https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions
title: "Aspose.Cells Cloud Get File Versions API – Fast Retrieval of File Version History"
subtitle: "Track Excel file changes in the cloud with Aspose.Cells Cloud’s GetFileVersions API — secure, REST-based, and SDK-supported."
linktitle: "GetFileVersions"
date: 2024-05-01T00:00:00Z
type: docs
draft: false
description: "Aspose.Cells Cloud GetFileVersions API retrieves full version history for Excel files stored in cloud storage. RESTful, JWT-secured, with SDKs for C#, Java, Python, Node.js, PHP, Ruby, Perl, and Go."
keywords: "Aspose Cells API, file versions, spreadsheet versioning, cloud storage API, REST, Excel file history"
weight: 100
---

## Overview

The **GetFileVersions** API enables developers to retrieve a complete list of version records for any Excel file stored in Aspose.Cells Cloud. This functionality supports audit trails, change tracking, and version-controlled workflows directly from cloud storage.

> ✅ **Before proceeding**, ensure you have:
> - An active [Aspose.Cells Cloud account](https://dashboard.aspose.cloud/)
> - Valid API credentials ([obtain JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/))
> - A file uploaded to cloud storage (see [UploadFile API](/upload-file/))

---

## Excel API: Get File Versions

### Web API Endpoint

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### Request Parameters

| Parameter Name | Type   | Location | Required | Description |
|----------------|--------|----------|----------|-------------|
| `path`         | String | Path     | Yes      | Full path to the file in cloud storage (e.g., `input/Report.xlsx`). |
| `storageName`  | String | Query    | No       | Name of the storage containing the file. If omitted, the default storage is used. |

### Authentication

All requests require a [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) in the `Authorization` header:

```
Authorization: Bearer {access_token}
```

> ⚠️ **Important**: Replace `{access_token}` with your valid JWT. Example:  
> `Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c`

---

## Response

On success, the API returns **HTTP 200 OK** with a JSON payload containing the `Value` array of file-version objects.

### Response Structure

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

| Field | Type | Description |
|-------|------|-------------|
| `Value` | Array\<[FileVersion](#fileversion-object)\> | Collection of version records |
| `VersionId` | String | Unique identifier for the version |
| `IsLatest` | Boolean | `true` if this is the most recent version |
| `ModifiedDate` | String (ISO 8601) | Timestamp of the last modification |
| `Size` | Integer | File size in bytes |

### HTTP Status Codes

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Request succeeded; file version list returned. |
| 400 | Bad Request | Missing or invalid parameters (e.g., unsupported file type, malformed path). |
| 401 | Unauthorized | Invalid or missing JWT token. |
| 404 | Not Found | File not found at the specified path. |
| 500 | Internal Server Error | Unexpected server error. |

---

## Example: cURL Request

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/path/to/your/file.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

> 📝 **Note**: Replace `path/to/your/file.xlsx` and `{access_token}` with actual values.

---

## Example: SDK Usage

Utilizing an SDK streamlines development by handling low-level details like authentication and JSON parsing. Below are concise examples in key languages.

{{< tabs tabTotal="8" tabID="sdk_examples" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
```csharp
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/blob/master/Examples/Cells/GetFileVersions.cs

var cellsApi = new CellsApi(clientId, clientSecret, basePath);
var versions = cellsApi.CellsStorageGetFileVersions("path/to/your/file.xlsx");
foreach (var version in versions.Value)
{
    Console.WriteLine($"Version {version.VersionId} | Modified: {version.ModifiedDate}");
}
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```java
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Examples/src/main/java/Example40_GetFileVersions.java

CellsApi cellsApi = new CellsApi(clientId, clientSecret);
FileVersionsResponse response = cellsApi.cellsStorageGetFileVersions("path/to/your/file.xlsx", null, "MyStorage");
for (FileVersion version : response.getValue()) {
    System.out.printf("Version %s | Latest: %b | Size: %d bytes%n", 
        version.getVersionId(), version.getIsLatest(), version.getSize());
}
```
{{< /tab >}}
{{< tab tabNum="3" >}}
```php
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/blob/master/Examples/Cells/GetFileVersions.php

$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->cellsStorageGetFileVersions("path/to/your/file.xlsx", null, "MyStorage");
foreach ($response->getValue() as $version) {
    echo "Version {$version->VersionId} | Latest: " . ($version->IsLatest ? 'Yes' : 'No') . "\n";
}
```
{{< /tab >}}
{{< tab tabNum="4" >}}
```ruby
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/blob/master/examples/get_file_versions.rb

cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
response = cells_api.cells_storage_get_file_versions("path/to/your/file.xlsx", storage_name: "MyStorage")
response.value.each do |v|
  puts "Version #{v.version_id} | Latest: #{v.is_latest}"
end
```
{{< /tab >}}
{{< tab tabNum="5" >}}
```typescript
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/blob/master/examples/Cells/GetFileVersions.ts

const cellsApi = new CellsApi(clientId, clientSecret);
const response = await cellsApi.cellsStorageGetFileVersions("path/to/your/file.xlsx", undefined, "MyStorage");
response.body.value?.forEach(v => {
  console.log(`Version ${v.versionId} | Latest: ${v.isLatest}`);
});
```
{{< /tab >}}
{{< tab tabNum="6" >}}
```python
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/blob/master/examples/cells/get_file_versions.py

cells_api = CellsApi(client_id, client_secret)
response = cells_api.cells_storage_get_file_versions("path/to/your/file.xlsx", storage_name="MyStorage")
for version in response.value:
    print(f"Version {version.version_id} | Latest: {version.is_latest}")
```
{{< /tab >}}
{{< tab tabNum="7" >}}
```perl
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/blob/master/examples/GetFileVersions.pl

my $cells_api = Aspose::Cells::Cloud::CellsApi->new(
    $client_id, $client_secret, $base_url
);
my $response = $cells_api->cells_storage_get_file_versions(
    "path/to/your/file.xlsx", 
    storage_name => "MyStorage"
);
for my $v (@{$response->value}) {
    print "Version $v->{VersionId} | Latest: " . ($v->{IsLatest} ? 'Yes' : 'No') . "\n";
}
```
{{< /tab >}}
{{< tab tabNum="8" >}}
```go
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/blob/master/examples/GetFileVersions.go

cfg := cells.NewConfiguration(clientId, clientSecret)
api := cells.NewAPIClient(cfg)
resp, _, err := api.StorageController.GetFileVersions(context.Background(), "path/to/your/file.xlsx").
    StorageName("MyStorage").Execute()
if err != nil { log.Fatal(err) }
for _, v := range resp.Value {
    fmt.Printf("Version %s | Latest: %v\n", v.VersionId, v.IsLatest)
}
```
{{< /tab >}}
{{< /tabs >}}

> 🔗 For installation, dependencies, and full examples, visit the [GitHub repository](https://github.com/aspose-cells-cloud).

---

## Related Resources

- [Upload a file to cloud storage](/upload-file/)
- [Download a specific file version](/download-file/)
- [List all files in storage](/list-files/)
- [Manage storage](/storage-management/)

---

## Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| `404 Not Found` | File path incorrect or file does not exist | Verify path and storage name. Use [ListFiles](/list-files/) to confirm existence. |
| `401 Unauthorized` | Invalid or expired JWT token | Refresh your token and ensure it includes required scopes. |
| `400 Bad Request` | Malformed path or unsupported file format | Use a valid Excel file (`.xlsx`, `.xls`, etc.) and percent-encode special characters in the path. |
| `500 Internal Server Error` | Temporary server issue | Retry the request. If persistent, contact [support](https://forum.aspose.cloud/). |

---

## API Specification

- **OpenAPI Spec**: [GetFileVersions Operation](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)
- **SDK Source**: [GitHub Org](https://github.com/aspose-cells-cloud)

---

*Last updated: 2024-05-01*