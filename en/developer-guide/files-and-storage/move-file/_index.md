---
title: "Aspose.Cells Cloud Move File API – Interface for Fast Moving of Files in the Cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Efficient Management Solution – Interface for Fast Moving of Files in the Cloud"
linktitle: "Move File"
type: docs
url: /move-file/
keywords: "Aspose.Cells, Move File API, Cloud Storage, Excel API, File Management"
description: "How to move files between folders in Aspose.Cells Cloud storage using the v4.0 Move File API – endpoint, parameters, examples, and SDK links."
weight: 100
---

The **moveFile** API moves a file from one location to another within Aspose.Cells Cloud storage. It helps you organize files and manage storage efficiently.

## **Excel API: Move File**

### Web API

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### The request parameters of **moveFile** API are

| Parameter Name  | Type   | Path/Query String/HTTP Body | Description                                        |
| --------------- | ------ | --------------------------- | -------------------------------------------------- |
| srcPath         | String | Path                        | The source path of the file to be moved.           |
| destPath        | String | Query                       | The destination path where the file will be moved. |
| srcStorageName  | String | Query                       | The source storage name, if applicable.            |
| destStorageName | String | Query                       | The destination storage name, if applicable.       |
| versionId       | String | Query                       | The version ID of the file, if applicable.         |

### **Response**

A successful request returns **HTTP 200 OK** with an empty JSON body.

```json
{}
```

**HTTP Status Codes**

| HTTP Code | HTTP Status           | Description                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK                    | Web API called successfully; response contains operation details. |
| 400       | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401       | Unauthorized          | Invalid or missing JWT token.                                     |
| 413       | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500       | Internal Server Error | Unexpected server error.                                          |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/MoveFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

Using an SDK is the best way to speed up the development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
