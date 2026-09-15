---
title: "Get Public Key (v4.0)"
date: 2024-03-15
lastmod: 2024-05-20
linktitle: "Get Public Key"
type: docs
url: /get-public-key/
keywords: ["Aspose.Cells Cloud", "RSA public key", "2048-bit encryption", "REST API", "asymmetric key", "OAuth2"]
description: "Retrieve the 2048-bit RSA public key from Aspose.Cells Cloud API for secure Excel file encryption. Includes cURL, SDK examples, and OAuth2 authentication."
weight: 100
---

This API retrieves the RSA public key (2048-bit) used for encrypting sensitive data before transmission to Aspose.Cells Cloud. The endpoint supports OAuth2 authentication and returns the key in JSON format.

## Prerequisites

Before calling this endpoint, ensure you have:
- A valid OAuth2 access token with the `Cells.Read` scope  
- An understanding of [JWT-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)

## Endpoint

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

## Request

### HTTP Headers

| Header           | Required | Type   | Description                                                                 |
|------------------|----------|--------|-----------------------------------------------------------------------------|
| `Authorization`  | Yes      | string | Bearer token for OAuth2 authentication                                      |
| `Accept`         | No       | string | Desired response format (e.g., `application/json`; defaults to JSON)       |

### cURL Example

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
     -H "Accept: application/json"
```

## Response

### Success Response (200 OK)

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

### HTTP Status Codes

| Code | Meaning               | Description                                                                 |
|------|-----------------------|-----------------------------------------------------------------------------|
| 200  | OK                    | Public key retrieved successfully; response contains RSA public key in JSON |
| 400  | Bad Request           | Invalid or missing parameters (e.g., malformed token, unsupported format)   |
| 401  | Unauthorized          | Invalid, expired, or missing OAuth2 access token                            |
| 413  | Payload Too Large     | Not applicable (GET request has no payload)                                 |
| 500  | Internal Server Error | Unexpected server-side error occurred                                       |

## Usage Examples

### Using Aspose.Cells Cloud SDKs

SDKs reduce boilerplate code, automate token refresh, and simplify integration. Below are examples for common languages:

- **C#**:  
  ```csharp
  var configuration = new Configuration { AppSid = "xxxx", AppKey = "yyyy" };
  var keyApi = new KeyController(configuration);
  var publicKey = keyApi.GetPublicKey();
  Console.WriteLine($"Algorithm: {publicKey.CellsCloudPublicKey.Algorithm}, KeySize: {publicKey.CellsCloudPublicKey.KeySize}");
  ```

- **Python**:  
  ```python
  from asposecellscloud.configuration import Configuration
  from asposecellscloud.api_client import KeyController

  config = Configuration(client_id="xxxx", client_secret="yyyy")
  api = KeyController(config)
  response = api.get_public_key()
  print(f"Algorithm: {response.cells_cloud_public_key.algorithm}, Size: {response.cells_cloud_public_key.key_size}")
  ```

- **Node.js**:  
  ```javascript
  const { Configuration, KeyController } = require('aspose-cells-cloud');

  const config = new Configuration('xxxx', 'yyyy');
  const keyApi = new KeyController(config);
  const response = await keyApi.getPublicKey();
  console.log(`Algorithm: ${response.body.CellsCloudPublicKey.Algorithm}, Size: ${response.body.CellsCloudPublicKey.KeySize}`);
  ```

For a complete list of SDKs and source code, visit the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).

### OpenAPI Specification

You can explore and test this endpoint interactively via the [OpenAPI specification](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey).

## Security Architecture

![Aspose.Cells Cloud Public Key Retrieval Flow](https://docs.aspose.cloud/cells/images/publickey-flow.png)

*Diagram: Client requests OAuth2 token → retrieves public key via `/cells/publickey` → uses key to encrypt Excel data before upload.*

**Alt text:** Diagram showing Aspose.Cells Cloud public key retrieval and data encryption flow

## Related Resources

- [REST API Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [Aspose.Cells Cloud SDK Documentation](https://docs.aspose.cloud/cells/sdk/)
- [Aspose.Cells Cloud SDK Source Code (GitHub)](https://github.com/aspose-cells-cloud)