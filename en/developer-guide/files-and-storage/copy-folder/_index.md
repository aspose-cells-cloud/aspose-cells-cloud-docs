---
title: "Aspose.Cells Cloud Folder Copy API – Fast Copying of Folders in the Cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management Solution – Detailed Explanation of Aspose.Cells Copy Folder API’s Batch Copy Functionality"
linktitle: "Copy Folder"
type: docs
url: /copy-folder/
keywords: "Copy Folder, Aspose.Cells Cloud, REST API, Cloud Storage, Spreadsheet Management"
description: "Learn how to copy folders in Aspose.Cells Cloud storage with a single REST call. Includes endpoint, parameters, sample requests, error codes, and SDK examples."
weight: 100
---

The **CopyFolder** API duplicates an existing folder within Aspose.Cells Cloud storage. This is useful for creating backups, reorganising data, or preparing a folder hierarchy for further processing without manual file moves.

## **Excel API: Copy Folder**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### The CopyFolder API accepts the following parameters

| Parameter Name    | Required | Type   | Location (Path/Query) | Description                                                            |
| ----------------- | -------- | ------ | --------------------- | ---------------------------------------------------------------------- |
| `srcPath`         | Yes      | String | Path                  | The path of the source folder to copy.                                 |
| `destPath`        | Yes      | String | Query                 | The path where the new folder will be created.                         |
| `srcStorageName`  | No       | String | Query                 | The name of the storage that contains the source folder.               |
| `destStorageName` | No       | String | Query                 | The name of the destination storage where the folder should be copied. |

### Sample Response

A successful call returns **HTTP 200** with an empty JSON body:

```json
{}
```

**Sample cURL request**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}
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
