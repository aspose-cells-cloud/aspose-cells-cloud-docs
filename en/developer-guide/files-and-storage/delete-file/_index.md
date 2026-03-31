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

## **Excel API : Delete File**

### API Endpoint  

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```  

### **Function Description**  

The **deleteFile** API removes the specified file from cloud storage, helping you manage resources and data efficiently.

### Prerequisites  

- An active Aspose Cloud account with a valid API key/Client ID.  
- An OAuth 2.0 access token (see the **Authentication** section).  
- The file path must be URL‑encoded.  

### Authentication  

The API requires an OAuth 2.0 Bearer token. Include the token in the request header:

```http
Authorization: Bearer <access_token>
```  

Tokens are obtained through the Aspose Cloud OAuth flow described in the official documentation.

### Request Parameters  

| Parameter Name | Type   | Location | Description |
|:---------------|:------|:---------|:------------|
| `path`         | string | Path     | The URL‑encoded path to the file that should be deleted. |
| `storageName`  | string | Query    | The name of the storage where the file resides. Omit if the default storage is used. |
| `versionId`    | string | Query    | Identifier of a specific file version to delete. If omitted, the latest version is removed. |

### Request Example  

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/MyFolder/MyFile.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>"
```  

### HTTP Response Codes  

| Code | Meaning                              |
|------|--------------------------------------|
| 200  | File deleted successfully (empty body). |
| 401  | Unauthorized – missing or invalid token. |
| 404  | Not Found – the specified file or storage does not exist. |
| 429  | Too Many Requests – rate limit exceeded. |
| 500  | Internal Server Error – unexpected condition. |

### Response Description  

A successful request returns **HTTP 200** with an empty response body. No JSON payload is returned.

```json
{}
```  

### Error Handling  

- **401 Unauthorized** – Refresh the OAuth token and retry.  
- **429 Too Many Requests** – Wait for the period indicated in the `Retry-After` header before retrying.  
- **500 Internal Server Error** – Verify request parameters and retry; if the problem persists, contact support.  

### **Response Example (Error)**  

```json
{
  "error": {
    "code": "FileNotFound",
    "message": "The specified file does not exist."
  }
}
```  

## OpenAPI Specification  

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK  

Using an SDK is the best way to speed up development. An SDK manages low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs.

### C# SDK Example  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>",
    AccessToken = "<access_token>"
};

var apiInstance = new CellsStorageApi(config);
await apiInstance.DeleteFileAsync(path: "MyFolder/MyFile.xlsx", storageName: "MyStorage");
```

### Java SDK Example  

```java
import com.aspose.cloud.cells.api.CellsStorageApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setClientId("<your_client_id>");
config.setClientSecret("<your_client_secret>");
config.setAccessToken("<access_token>");

CellsStorageApi api = new CellsStorageApi(config);
api.deleteFile("MyFolder/MyFile.xlsx", "MyStorage", null);
```

### Python SDK Example  

```python
from asposecellscloud import CellsStorageApi, Configuration

config = Configuration()
config.client_id = "<your_client_id>"
config.client_secret = "<your_client_secret>"
config.access_token = "<access_token>"

api = CellsStorageApi(config)
api.delete_file(path="MyFolder/MyFile.xlsx", storage_name="MyStorage")
```

## Frequently Asked Questions  

**Q: How do I delete an Excel file stored in Aspose.Cells Cloud?**  
A: Send a `DELETE` request to `https://api.aspose.cloud/v4.0/cells/storage/file/{path}` with a valid OAuth 2.0 Bearer token. Replace `{path}` with the URL‑encoded file path. Optional query parameters are `storageName` and `versionId`. A successful call returns HTTP 200 with an empty body.

**Q: What authentication method is required for the Delete File API?**  
A: The API requires an OAuth 2.0 access token passed in the `Authorization: Bearer <token>` header.

**Q: What HTTP status codes can I expect from the Delete File API?**  
A: 200 OK (success), 401 Unauthorized (invalid token), 404 Not Found (file or storage missing), 429 Too Many Requests (rate limit), 500 Internal Server Error (server problem).

**Q: Can I delete a specific version of a file?**  
A: Yes. Include the `versionId` query parameter with the desired version identifier. If omitted, the latest version is removed.

## See Also  

- [Upload File API](/upload-file/)  
- [Get Files List API](/list-files/)  

---  

*Note: The language selector and other UI scripts have been reviewed for accessibility compliance.*