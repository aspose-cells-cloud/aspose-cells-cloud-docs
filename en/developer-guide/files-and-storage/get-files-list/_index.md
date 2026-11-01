---
title: "Aspose.Cells Cloud API – Get Files List (Folder Contents)"
second_title: "Developer Guide"
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
The **GetFilesList** API (`GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}`) retrieves the collection of files and subfolders stored in a specified folder of Aspose.Cells Cloud storage, enabling developers to browse cloud-based Excel workbooks, archives, and other supported file types programmatically using the v4.0 REST API.

## The Get Files List Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| path | String | Path | - |
| storageName | String | Query | - |

- **Value** – Array of `StorageFile` objects. Each object contains:
  - `Name` – File or folder name.
  - `IsFolder` – `true` if the entry is a folder.
  - `Size` – Size in bytes (folders report `0`).
  - `ModifiedDate` – Last modification timestamp (ISO 8601).

### **Response**

```json
[
  {
    "Name": "FilesList",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesList"
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
