---
title: "Get Public Key (v4.0)"
date: 2024-03-15
lastmod: 2024-05-20
linktitle: "Get Public Key"
type: docs
url: /get-public-key/
keywords:
  [
    "Aspose.Cells Cloud",
    "RSA public key",
    "2048-bit encryption",
    "REST API",
    "asymmetric key",
    "OAuth2",
  ]
description: "Get 2048-bit RSA public key from Aspose.Cells Cloud API via OAuth2 GET /v4.0/cells/publickey for secure encryption"
weight: 100
ArticleTitle: "Get RSA 2048-bit Public Key from Aspose.Cells Cloud API"
---
The **GetPublicKey** API (`GET https://api.aspose.cloud/v4.0/cells/publickey`) retrieves the 2048-bit RSA public key used by Aspose.Cells Cloud for encrypting sensitive data prior to transmission; this asymmetric public key enables clients to securely encrypt payloads before sending them to the service, supporting end-to-end data protection as part of the API’s OAuth2-secured workflow.

## The Get Public Key Web API

```http
GET https://api.aspose.cloud/v4.0/cells/publickey
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### **Request Parameters:**

This operation does not require request parameters.

### **Response**

```json
[
  {
    "Name": "CellsCloudPublicKeyResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudPublicKeyResponse"
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

## Request

### HTTP Headers

| Header          | Required | Type   | Description                                                          |
| --------------- | -------- | ------ | -------------------------------------------------------------------- |
| `Authorization` | Yes      | string | Bearer token for OAuth2 authentication                               |
| `Accept`        | No       | string | Desired response format (e.g., `application/json`; defaults to JSON) |

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
| ---- | --------------------- | --------------------------------------------------------------------------- |
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
  const { Configuration, KeyController } = require("aspose-cells-cloud");

  const config = new Configuration("xxxx", "yyyy");
  const keyApi = new KeyController(config);
  const response = await keyApi.getPublicKey();
  console.log(
    `Algorithm: ${response.body.CellsCloudPublicKey.Algorithm}, Size: ${response.body.CellsCloudPublicKey.KeySize}`,
  );
  ```

For a complete list of SDKs and source code, visit the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).
