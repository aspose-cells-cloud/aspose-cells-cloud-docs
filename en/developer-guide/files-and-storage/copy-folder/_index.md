---
title: "Aspose.Cells Cloud Folder Copy API – Fast Copying of Folders in the Cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management Solution – Detailed Explanation of Aspose.Cells Copy Folder API’s Batch Copy Functionality"
linktitle: "Copy Folder"
type: docs
url: /copy-folder/
keywords: "Copy Folder API, Aspose.Cells, Cloud Storage, REST API, Spreadsheet Management"
description: "Learn how to copy folders in Aspose.Cells Cloud storage with a single REST call. Includes endpoint, parameters, sample requests, error codes, and SDK examples."
weight: 100
---

## **Excel API: Copy Folder**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### Function Description

The **CopyFolder** API duplicates an existing folder within Aspose.Cells Cloud storage. This is useful for creating backups, reorganising data, or preparing a folder hierarchy for further processing without manual file moves.

### The CopyFolder API accepts the following parameters

| Parameter Name    | Required | Type   | Location (Path/Query) | Description                                                            |
| ----------------- | -------- | ------ | --------------------- | ---------------------------------------------------------------------- |
| `srcPath`         | Yes      | String | Path                  | The path of the source folder to copy.                                 |
| `destPath`        | Yes      | String | Query                 | The path where the new folder will be created.                         |
| `srcStorageName`  | No       | String | Query                 | The name of the storage that contains the source folder.               |
| `destStorageName` | No       | String | Query                 | The name of the destination storage where the folder should be copied. |

````

### Sample Response

A successful call returns **HTTP 200** with an empty JSON body:

```json
{}
````

### Error Codes

| HTTP Status | Code                | Meaning                           | Typical Cause                           |
| ----------- | ------------------- | --------------------------------- | --------------------------------------- |
| 400         | BadRequest          | Missing or invalid parameters     | `srcPath` or `destPath` not supplied    |
| 401         | Unauthorized        | Invalid or missing OAuth token    | Token expired or not provided           |
| 404         | NotFound            | Source folder does not exist      | Incorrect `srcPath`                     |
| 409         | Conflict            | Destination folder already exists | `destPath` points to an existing folder |
| 500         | InternalServerError | Unexpected server error           | Service outage or internal bug          |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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

### Frequently Asked Questions

**Q: How do I copy a folder using Aspose.Cells Cloud API?**  
A: Send a `PUT` request to `https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}` with the query parameters `destPath`, optional `srcStorageName` and `destStorageName`, and include an OAuth 2.0 Bearer token in the `Authorization` header. A successful call returns HTTP 200 with an empty JSON body (`{}`).

**Q: What authentication method is required for the CopyFolder API?**  
A: The API requires OAuth 2.0. Obtain an access token via the Aspose Cloud authentication endpoint and pass it as `Authorization: Bearer <access_token>` in the request header.

**Q: What error codes can I expect when copying a folder?**  
A: Common responses are `400 Bad Request` (missing parameters), `401 Unauthorized` (invalid token), `404 Not Found` (source folder not found), and `409 Conflict` (destination already exists). The response body contains a JSON error object with `Code` and `Message`.

**Q: Can I copy a folder between different storages?**  
A: Yes. Use the optional `srcStorageName` and `destStorageName` query parameters to specify the source and destination storages.

**Q: Is there a size limit for the folder being copied?**  
A: The API does not impose a specific size limit, but the request is subject to the overall storage quota and the service’s timeout settings.

---
