---
title: "Aspose.Cells Cloud API – Get Files List (Folder Contents)"
description: "Retrieve a list of files and sub‑folders from a specific folder in Aspose.Cells Cloud storage."
keywords:
  - Aspose.Cells
  - API
  - Get Files List
  - Cloud Storage
  - Excel
  - REST
type: docs
weight: 100
---

The **Get Files List** operation returns the collection of files and sub‑folders stored in a specified folder of Aspose.Cells Cloud storage.  
It is the primary entry point for browsing cloud‑based Excel workbooks, archives, and other supported file types.

## Aspose.Cells Cloud API – Get Files List (Folder Contents)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Name            | Location | Type    | Required | Description                                                          |
| --------------- | -------- | ------- | -------- | -------------------------------------------------------------------- |
| **path**        | Path     | string  | Yes      | Path to the folder in cloud storage.                                 |
| **storageName** | Query    | string  | No       | Name of the storage to use. If omitted, the default storage is used. |
| **pageSize**    | Query    | integer | No       | Maximum number of items to return per page (default: 100).           |
| **pageNumber**  | Query    | integer | No       | Page number to retrieve (starting at 1, default: 1).                 |

- **Value** – Array of `StorageFile` objects. Each object contains:
  - `Name` – File or folder name.
  - `IsFolder` – `true` if the entry is a folder.
  - `Size` – Size in bytes (folders report `0`).
  - `ModifiedDate` – Last modification timestamp (ISO 8601).

### **Response**

**HTTP Status Codes**

| HTTP Code | HTTP Status           | Description                                                       |
| --------- | --------------------- | ----------------------------------------------------------------- |
| 200       | OK                    | Web API called successfully; response contains operation details. |
| 400       | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401       | Unauthorized          | Invalid or missing JWT token.                                     |
| 413       | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500       | Internal Server Error | Unexpected server error.                                          |
|  |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK manages low‑level details and lets you focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
