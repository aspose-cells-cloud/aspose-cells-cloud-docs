---
url: /move-folder/
title: "Aspose.Cells Cloud Move Folder API – Quickly Move Folders in the Cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management – Quickly Move Folders in the Cloud"
linktitle: "Move Folder"
type: docs
date: 2024-03-15
lastmod: 2024-06-10
keywords: "Aspose.Cells, Move Folder, Cloud Storage, Excel API, REST API move folder, Aspose.Cells Cloud storage API"
description: "Aspose.Cells Cloud Move Folder API documentation: REST endpoint, parameters, cURL, and SDK examples for C#, Java, Python. Secure folder management in cloud storage."
weight: 100
---

This API moves a folder from one location to another within Aspose.Cells Cloud storage. It helps organize files and manage cloud storage efficiently.

## Prerequisites

Before using this API, ensure you have:

- A valid Aspose.Cells Cloud account and API key  
- A generated JWT access token (see [JWT Authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){: rel="noopener noreferrer"})  
- Basic familiarity with RESTful APIs and cURL commands

> ⚠️ **Note:** This API uses `/v4.0`. Aspose.Cells Cloud v5.0 is expected in Q4 2024 — review the [migration guide](/migration/) for upcoming changes.

## Web API: Move Folder

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### Request Parameters

| Parameter Name  | Type   | Location | Required | Description                                                                 |
|-----------------|--------|----------|----------|-----------------------------------------------------------------------------|
| `srcPath`       | string | Path     | Yes      | The full path of the source folder to move, e.g., `Documents/FolderA/`.    |
| `destPath`      | string | Query    | Yes      | The full path of the destination folder, e.g., `Documents/FolderB/`.       |
| `srcStorageName`| string | Query    | No       | (Optional) Name of the source storage. Defaults to the first configured storage. |
| `destStorageName`| string| Query    | No       | (Optional) Name of the destination storage. Defaults to the first configured storage. |

> 💡 **Tip:** Use trailing slashes (`/`) for folder paths to avoid ambiguity. If `srcStorageName` and `destStorageName` differ, the folder will be moved across storages.

### Example Request

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/Documents/FolderA/?destPath=Documents/FolderB/" \
     -H "Authorization: Bearer {access_token}"
```

### Response

On success, the API returns an empty response body with HTTP status **200 OK**.

#### HTTP Status Codes

| Code | Status              | Description                                               |
|------|---------------------|-----------------------------------------------------------|
| 200  | OK                  | Folder moved successfully.                                |
| 400  | Bad Request         | Invalid or missing `srcPath`/`destPath`; malformed path. |
| 401  | Unauthorized        | Invalid, expired, or missing JWT token.                   |
| 404  | Not Found           | Source folder does not exist.                             |
| 409  | Conflict            | Destination folder already exists.                        |
| 500  | Internal Server Error | Unexpected server-side error.                           |

## Code Examples

{{< tabs tabTotal="5" tabID="1" tabName1="cURL" tabName2="C#" tabName3="Java" tabName4="Python" tabName5="Node.js" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/SourceFolder/?destPath=TargetFolder/" \
     -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
     -H "Content-Type: application/json"
```
{{< /tab >}}

{{< tab tabNum="2" >}}

```csharp
// Install Aspose.Cells Cloud SDK for .NET via NuGet
// Install-Package Aspose.Cells-Cloud

var config = new Configuration 
{ 
    ClientId = "YOUR_CLIENT_ID", 
    ClientSecret = "YOUR_CLIENT_SECRET" 
};
var cellsApi = new CellsApi(config);

// Move folder from SourceFolder/ to TargetFolder/
await cellsApi.FolderMoveFolderAsync(
    srcPath: "SourceFolder/",
    destPath: "TargetFolder/"
);
```
{{< /tab >}}

{{< tab tabNum="3" >}}

```java
// Install Aspose.Cells Cloud SDK for Java via Maven
// <dependency>
//   <groupId>com.aspose</groupId>
//   <artifactId>aspose-cloud-cells-java</artifactId>
//   <version>22.9</version>
// </dependency>

import com.aspose.cells.CellsApi;

String clientId = "YOUR_CLIENT_ID";
String clientSecret = "YOUR_CLIENT_SECRET";
String basePath = "https://api.aspose.cloud/v4.0";
CellsApi cellsApi = new CellsApi(clientId, clientSecret, basePath, "v4.0");

// Move folder
cellsApi.folderMoveFolder(
    "SourceFolder/",
    "TargetFolder/",
    null, null
);
```
{{< /tab >}}

{{< tab tabNum="4" >}}

```python
# Install Aspose.Cells Cloud SDK for Python via pip
# pip install asposecellscloud

from asposecellscloud.api import cells_api
from asposecellscloud.configuration import Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api = cells_api.CellsApi(config.client_id, config.client_secret)

# Move folder
api.folder_move_folder(
    src_path="SourceFolder/",
    dest_path="TargetFolder/"
)
```
{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Install Aspose.Cells Cloud SDK for Node.js via npm
// npm install asposecellscloud

const { CellsApi } = require("asposecellscloud");

const cellsApi = new CellsApi(
  "YOUR_CLIENT_ID",
  "YOUR_CLIENT_SECRET"
);

// Move folder
cellsApi.folderMoveFolder(
  "SourceFolder/",
  "TargetFolder/"
).then(() => {
  console.log("Folder moved successfully.");
});
```
{{< /tab >}}

{{< /tabs >}}

## Related APIs

- [List Folder](/list-folder/) — Retrieve contents of a storage folder  
- [Delete Folder](/delete-folder/) — Remove an empty folder from storage  
- [Create Folder](/create-folder/) — Create a new folder in cloud storage  

> 🔗 For comprehensive folder management, combine these APIs to build dynamic storage workflows.

## OpenAPI Specification

The API is fully defined in the [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder), enabling direct browser-based testing and integration with API design tools.

{{% /md %}}