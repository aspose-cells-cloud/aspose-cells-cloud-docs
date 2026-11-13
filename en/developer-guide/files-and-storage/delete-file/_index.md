---
title: "Delete File"
linktitle: "Delete File"
type: docs
url: /delete-file/
description: "Delete an Excel file from Aspose.Cells Cloud storage using the REST API. Includes endpoint, path/query parameters, authentication, HTTP status codes, and cURL/SDK examples."
keywords: "Aspose.Cells, delete file API, Excel cloud storage, REST API, file management, cloud file deletion"
weight: 100
ArticleTitle: "Delete Excel File from Aspose.Cells Cloud Storage via REST API"
---
The **DeleteFile** API (`DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}`) removes a specified file from Aspose.Cells Cloud storage using the RESTful v4.0 API; it requires a `path` parameter indicating the file’s location and optionally supports `storageName` and `versionId` query parameters for multi-storage or versioned file management, enabling precise deletion of files stored in cloud environments.

## The Delete File Web API

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### Security and Authentication

All requests require JWT token authentication.

```bash
-H "Authorization: Bearer {access_token}"
```

> **Note**: Replace `{access_token}` with your valid JWT access token. See the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for setup instructions.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| path | String | Path | - |
| storageName | String | Query | - |
| versionId | String | Query | - |

### Response

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

A successful request returns **HTTP 200** with an empty response body.


#### HTTP Status Codes

### Examples

#### cURL Request

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

> **Tip**: Replace `{access_token}` with your valid JWT token. For test environments, you may generate a token via the [OAuth Playground](https://apiconsole.aspose.cloud/applications).

#### Using Aspose.Cells Cloud SDKs

SDKs abstract low-level HTTP details and improve reliability. Available SDKs include .NET, Java, Python, Node.js, PHP, Ruby, and Go.

- 📘 **SDK Documentation**: [https://docs.aspose.cloud/cells/sdk/](https://docs.aspose.cloud/cells/sdk/)
- 💻 **GitHub Repositories**: [https://github.com/aspose-cells-cloud](https://github.com/aspose-cells-cloud)

##### Example (C#)

```csharp
var config = new Configuration { ClientId = "YOUR_CLIENT_ID", ClientSecret = "YOUR_CLIENT_SECRET" };
var cellsApi = new CellsApi(config);

// Delete file from storage
await cellsApi.DeleteFile("Example.xlsx", "MyStorage");
```

##### Example (Python)

```python
from asposecellscloud.configuration import Configuration
from asposecellscloud.api.cells_api import CellsApi

config = Configuration(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
cells_api = CellsApi(config)

# Delete file
await cells_api.delete_file("Example.xlsx", storage_name="MyStorage")
```

### Related Operations

- [Upload File](/upload-file/)
- [List Files](/list-files/)
- [Download File](/download-file/)
- [Storage API Overview](/storage-api/)

## How to Use the Delete File API with SDKs?

### Delete File API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/DeleteFile" rel="noopener noreferrer">Delete File API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteFile.go" >}}
{{</tab>}}
{{< /tabs >}}
