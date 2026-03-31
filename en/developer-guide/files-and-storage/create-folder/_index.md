---
title: "Create Folder – Aspose.Cells Cloud API | Excel Storage Management"
second_title: "Document"
ArticleTitle: "Create Folder – Aspose.Cells Cloud API"
linktitle: "Create Folder"
type: docs
url: /create-folder/
keywords: "Aspose.Cells Cloud, Create Folder, Excel API, REST, Storage"
description: "Learn how to create a folder in Aspose.Cells Cloud storage via a simple REST PUT request. Includes sample cURL, authentication guide, and error handling."
weight: 100
---

## **Excel API: Create Folder**

### API Endpoint

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

> **Version:** v4.0 (June 2026) – HTTPS is required for all requests.

### Authentication

All requests must include a valid OAuth 2.0 bearer token.  
Add the token in the `Authorization` header:

```bash
-H "Authorization: Bearer <access_token>"
```

You can obtain the token through the client‑credentials flow described in the **Aspose.Cells Cloud authentication guide**.

### Function Description

The **createFolder** operation creates a new folder at the specified location in the cloud storage used by the Excel API. This is essential for organizing files and maintaining a structured directory hierarchy.

### The request parameters of **createFolder** API are

| Parameter Name | Type   | Location | Required | Default | Description |
|----------------|--------|----------|----------|---------|-------------|
| `path`         | String | Path     | Yes      | –       | The folder path to be created (e.g., `myFolder/subFolder`). |
| `storageName`  | String | Query    | No       | –       | The name of the storage to use. If omitted, the default storage is applied. |

### Sample Request

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/MyNewFolder" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### Response Description

A successful request returns **204 No Content** (no body) or a JSON confirmation message, for example:

```json
{
  "message": "Folder created successfully."
}
```

### Error Handling

| HTTP Status | Meaning                               | Suggested Remedy                              |
|-------------|---------------------------------------|----------------------------------------------|
| 200 OK / 204 No Content | Folder created successfully. | – |
| 400 Bad Request | Invalid `path` or missing parameters. | Verify the path syntax and required fields. |
| 401 Unauthorized | Missing or invalid OAuth token. | Obtain a valid token and include it in the request. |
| 409 Conflict | The folder already exists. | Choose a different folder name or delete the existing one. |
| 500 Internal Server Error | Server‑side problem. | Retry later or contact support. |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK manages low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}

**See also**

- Delete Folder – `DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}`
- Copy Folder – `PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{srcPath}/copy`  

---