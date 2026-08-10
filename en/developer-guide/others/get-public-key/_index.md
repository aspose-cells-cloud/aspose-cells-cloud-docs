---
title: "Aspose.Cells Cloud API – Get Public Key (v4.0) | REST Documentation"
second_title: "Document"
ArticleTitle: "Get Public Key"
linktitle: "Get Public Key"
type: docs
url: /get-public-key/
keywords: "Aspose.Cells, Public Key, RSA, API, Cloud"
description: "Retrieve the RSA public key used for encrypting data with Aspose.Cells Cloud. Includes endpoint, parameters, sample request/response, status codes, and SDK usage examples."
weight: 100
---

This API retrieves the public key from an asymmetric encryption algorithm.

**Brief Summary:** Use the Aspose.Cells Get Public Key API to obtain the RSA public key (2048‑bit) required for encrypting data when working with Excel files in the cloud. The endpoint returns the key in JSON format and is secured with OAuth 2.0.

## **Get Public Key API**

**Prerequisites:**  
Obtain a valid OAuth 2.0 access token that includes the `Cells.Read` scope before calling this endpoint.

### **Web API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**Sample Request (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type   | Location | Description                                                                     |
| -------------- | ------ | -------- | ------------------------------------------------------------------------------- |
| Authorization  | string | Header   | Bearer token for OAuth2 authentication (required).                              |
| Accept         | string | Header   | Desired response format, e.g., `application/json` (optional, defaults to JSON). |

### **Response**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the Get public key API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) defines a publicly accessible programming interface, enabling you to perform REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement get public key for cells with minimal code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

Below are concrete examples for the most common languages:

**C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configure API client
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};
var apiInstance = new CellsApi(config);

// Call GetPublicKey
var response = apiInstance.GetPublicKey();
Console.WriteLine($"Public Key: {response.CellsCloudPublicKey.PublicKey}");
```

**Java**

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.model.CellsCloudPublicKeyResponse;

public class GetPublicKeyExample {
    public static void main(String[] args) {
        ApiClient client = new ApiClient();
        client.setAccessToken("{access_token}");
        CellsApi api = new CellsApi(client);

        CellsCloudPublicKeyResponse resp = api.getPublicKey();
        System.out.println("Public Key: " + resp.getCellsCloudPublicKey().getPublicKey());
    }
}
```

**Python**

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

configuration = Configuration()
configuration.access_token = '{access_token}'
configuration.host = 'https://api.aspose.cloud'

api_client = ApiClient(configuration)
cells_api = CellsApi(api_client)

response = cells_api.get_public_key()
print("Public Key:", response.cells_cloud_public_key.public_key)
```

**Node.js**

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
});
const cellsApi = new CellsApi(config);

cellsApi.getPublicKey()
    .then(response => {
        console.log('Public Key:', response.cellsCloudPublicKey.publicKey);
    })
    .catch(error => {
        console.error(error);
    });
```

For additional language support, refer to the SDK documentation linked in the GitHub repository. You may also explore related APIs such as **[Post Access Token](/post-access-token/)** to programmatically obtain the required OAuth 2.0 token.