---
title: "Aspose.Cells Cloud File Copy API - An interface for fast copying and batch operations of Excel files in the cloud"
second_title: "Document"
ArticleTitle: "Cloud-based Excel File Management Solution – Detailed Explanation of Aspose.Cells Copy File API’s Batch Copy Functionality"
linktitle: "Copy File"
type: docs
url: /copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel file copy, Cloud storage, REST API"
description: "Learn how to use the Aspose.Cells Cloud CopyFile API to efficiently duplicate Excel files and manage them across storage locations."
weight: 100
---

The **copyFile** API allows users to duplicate an Excel file from a specified source path to a destination path, supporting various storage options.

## **Excel API: Copy File**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### The request parameters of the **copyFile** API are

| Parameter Name  | Type   | Path/Query String/HTTPBody | Description                                        |
| --------------- | ------ | -------------------------- | -------------------------------------------------- |
| srcPath         | String | Path                       | The source path of the file to be copied.          |
| destPath        | String | Query                      | The destination path where the file will be saved. |
| srcStorageName  | String | Query                      | The name of the source storage.                    |
| destStorageName | String | Query                      | The name of the destination storage.               |
| versionId       | String | Query                      | Optional version ID of the file to copy.           |

### **Response**

The operation returns no content on success. Typical HTTP status codes are:

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## How to Use the Copy File API with SDKs?

### Copy File API Specification

The [Copy File API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) provides a publicly accessible programming interface for conducting REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
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

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to convert spreadsheet table data to an image with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:
