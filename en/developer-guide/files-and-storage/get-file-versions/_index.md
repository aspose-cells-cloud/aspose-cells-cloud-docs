---
title: "Aspose.Cells Cloud Get File Versions API – Fast Retrieval of File Version History"
second_title: "Document"
ArticleTitle: "Cloud‑Based Excel Management – Quickly Retrieve File Version History in Aspose.Cells Cloud"
linktitle: "Get File Versions"
type: docs
url: /get-file-versions/
keywords: "Aspose Cells API, file versions, spreadsheet versioning, cloud storage API, REST, Excel file history"
description: "Get a complete list of version history for any Excel file stored in Aspose.Cells Cloud. Supports storage selection, authentication, and detailed error codes."
weight: 100
---

Retrieve a complete list of version records for a specific spreadsheet stored in Aspose.Cells Cloud. This endpoint enables developers to track changes, audit modifications, and implement version‑control workflows directly from the cloud storage.

The **GetFileVersions** API returns all version records for a specified spreadsheet stored in Aspose.Cells Cloud. It helps you keep a complete change history for each file.

## **Excel API: Get File Versions**

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### The request parameters of **GetFileVersions** API are

| Parameter Name | Type   | Location | Description                                                                                 |
| -------------- | ------ | -------- | ------------------------------------------------------------------------------------------- |
| `path`         | String | Path     | **Required.** Full path to the file whose versions are being retrieved.                     |
| `storageName`  | String | Query    | Optional. Name of the storage containing the file. If omitted, the default storage is used. |

### **Response**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["A collection of file version details."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

On success, the API returns **HTTP 200 OK** with a JSON payload containing the `Value` array of file‑version objects, as illustrated above.

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) provides a comprehensive programming interface for executing REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Utilizing an SDK streamlines development by abstracting low‑level complexities, allowing developers to focus on core functionalities. Explore the [GitHub repository](https://github.com/aspose-cells-cloud) for a full list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services across various programming languages:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}
