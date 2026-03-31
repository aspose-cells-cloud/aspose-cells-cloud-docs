---
title: "Delete Folder – Aspose.Cells Cloud API | Remove Folders via REST"
ArticleTitle: "Delete Folder – Aspose.Cells Cloud API"
linktitle: "Delete Folder"
type: docs
url: /delete-folder/
keywords: "Aspose.Cells delete folder, cloud storage, REST API, Excel file management, recursive delete"
description: "Learn how to delete a folder (optionally recursively) from Aspose.Cells Cloud storage using the DELETE /v4.0/cells/storage/folder/{path} endpoint. Includes request syntax, parameters, sample code, and error handling."
weight: 100
---

## **Excel API : Delete Folder**

### Prerequisites
- **Authentication** – Obtain an OAuth 2.0 access token (JWT) and include it in the `Authorization: Bearer <token>` header.  
- **SDK version** – Use Aspose.Cells Cloud SDK v4.0 or later.  
- **Supported storages** – Any storage configured in your Aspose Cloud account (e.g., Aspose Cloud Storage, Amazon S3, Azure Blob).

### API Endpoint
```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### Function Description
The `deleteFolder` API removes a specified folder from Aspose.Cells Cloud storage. It can delete the folder alone or, when the `recursive` flag is set to `true`, remove the folder together with all of its contents.

### Request Parameters
The request parameters of the **deleteFolder** API are:

| Parameter Name | Type   | Location                     | Description                                                   |
|----------------|--------|------------------------------|---------------------------------------------------------------|
| path           | String | Path                         | The path of the folder to be deleted.                         |
| storageName    | String | Query                        | The name of the storage that contains the folder.            |
| recursive      | Boolean| Query                        | Set to `true` to delete the folder and all of its contents. |

### Request Example
```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder
Authorization: Bearer {access_token}
Accept: application/json
```
*To delete recursively, add `?recursive=true` to the URL.*

### Response Example
A successful call returns **HTTP 200 OK** with an empty body:

```json
{}
```

### OpenAPI Specification
The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) defines a publicly accessible programming interface and allows you to perform REST interactions directly from a web browser.

### Error Handling
| HTTP Status | Description                                   |
|-------------|-----------------------------------------------|
| 400         | Bad request – missing or invalid parameters. |
| 401         | Unauthorized – authentication token required or invalid. |
| 404         | Not found – the specified folder does not exist. |
| 409         | Conflict – folder cannot be deleted because it contains items and `recursive` is not set. |
| 500         | Internal server error – unexpected condition on the server. |

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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