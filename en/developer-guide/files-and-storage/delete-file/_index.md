---
title: "Aspose.Cells Cloud – Delete File API"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud – Delete File API"
linktitle: "Delete File"
type: docs
url: /delete-file/
keywords: "Aspose Cells, Delete File API, Excel Cloud Storage, REST API, File Management"
description: "Delete an Excel file from Aspose.Cells Cloud storage using the RESTful Delete File API. Includes endpoint, parameters, auth, and sample code."
weight: 100
---

The **deleteFile** API removes the specified file from cloud storage, helping you manage resources and data efficiently.

## **Excel API : Delete File**

### Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name | Type   | Location | Description                                                                                 |
| :------------- | :----- | :------- | :------------------------------------------------------------------------------------------ |
| `path`         | string | Path     | The URL‑encoded path to the file that should be deleted.                                    |
| `storageName`  | string | Query    | The name of the storage where the file resides. Omit if the default storage is used.        |
| `versionId`    | string | Query    | Identifier of a specific file version to delete. If omitted, the latest version is removed. |

### Response Description

A successful request returns **HTTP 200** with an empty response body. No JSON payload is returned.

```json
{}
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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
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

Using an SDK is the best way to speed up development. An SDK manages low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs.
