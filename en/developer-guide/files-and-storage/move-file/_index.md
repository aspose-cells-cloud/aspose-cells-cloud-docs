---
title: "Aspose.Cells Cloud Move File API – Interface for Fast Moving of Files in the Cloud"
second_title: "Developer Guide"
ArticleTitle: "Cloud-based Excel File Efficient Management Solution – Interface for Fast Moving of Files in the Cloud"
linktitle: "Move File"
type: docs
url: /move-file/
keywords: "Aspose.Cells, Move File API, Cloud Storage, Excel API, File Management"
description: "Move Excel files in Aspose.Cells Cloud storage using the Move File API with path parameters and cURL/SDK examples"
weight: 100
---
The **MoveFile** API (`PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}`) moves a file from a specified source path (`srcPath`) to a destination path (`destPath`) within Aspose.Cells Cloud storage using the HTTP PUT method; it supports optional parameters for specifying source and destination storage names and version IDs, enabling efficient file reorganization across cloud storage locations without downloading or re-uploading.

## The Move File Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### The request parameters of **moveFile** API are

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| srcPath | String | Path | - |
| destPath | String | Query | - |
| srcStorageName | String | Query | - |
| destStorageName | String | Query | - |
| versionId | String | Query | - |

### **Response**

```json
[
  {
    "Name": "Void",
    "DataType": {
      "Identifier": "Void"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

A successful request returns **HTTP 200 OK** with an empty JSON body.

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
