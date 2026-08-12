---
title: "Create Folder – Aspose.Cells Cloud API | Excel Storage Management"
second_title: "Document"
ArticleTitle: "Create Folder – Aspose.Cells Cloud API"
linktitle: "Create Folder"
type: docs
url: /create-folder/
keywords: "Aspose.Cells, Cloud API, Create Folder, Storage Management, Excel"
description: "Create a new folder in Aspose.Cells Cloud storage via a simple PUT request. See request format, parameters, response and error handling."
weight: 100
---

The **createFolder** operation creates a new folder at the specified location in the cloud storage used by the Excel API. This is essential for organizing files and maintaining a structured directory hierarchy.

## **Excel API: Create Folder**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### The request parameters of **createFolder** API are

| Parameter Name | Type   | Location | Required | Default | Description                                                                 |
| -------------- | ------ | -------- | -------- | ------- | --------------------------------------------------------------------------- |
| `path`         | String | Path     | Yes      | –       | The folder path to be created (e.g., `myFolder/subFolder`).                 |
| `storageName`  | String | Query    | No       | –       | The name of the storage to use. If omitted, the default storage is applied. |

### Response Description

```json
{}
```

The operation returns no content on success. Typical HTTP status codes are:

**HTTP Status Codes**

| HTTP Code | HTTP Status           | Description                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK                    | Web API called successfully; response contains operation details. |
| 400       | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401       | Unauthorized          | Invalid or missing JWT token.                                     |
| 413       | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500       | Internal Server Error | Unexpected server error.                                          |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/myFolder/subFolder" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK manages low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

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
