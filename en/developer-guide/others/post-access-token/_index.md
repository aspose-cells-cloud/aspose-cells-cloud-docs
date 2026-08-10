---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "Document"
ArticleTitle: "Get Access Token with Client ID and Secret"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells, Cloud, Access Token, OAuth2, API, Authentication, REST, Excel, Office Cloud"
description: "Obtain an OAuth2 access token for Aspose.Cells Cloud by calling the POST /cells/connect/token endpoint with your client ID and secret."
weight: 100
---

Retrieve an access token using the Cells Cloud Get Token API with a client ID and secret.

## Post Access Token API

Before calling the endpoint, ensure you have:

* A registered Aspose Cloud account.  
* A **Client ID** and **Client Secret** generated in the Aspose Cloud portal.  

### Web API

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Location                     | Description                                          |
| -------------- | ------ | ---------------------------- | ---------------------------------------------------- |
| grant_type     | string | body (form‑url‑encoded)      | Fixed value `client_credentials` required for OAuth. |
| client_id      | string | body (form‑url‑encoded)      | The client identifier issued to you.                 |
| client_secret  | string | body (form‑url‑encoded)      | The secret associated with the client ID.            |

**Example request (cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### Response

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
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

**Error handling example**

```json
{
  "error": "invalid_client",
  "error_description": "Client authentication failed."
}
```

## How to Use the Get public key API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to get started. The SDK abstracts the underlying HTTP details, enabling you to obtain an access token for Cells with minimal code.

Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs. An SDK takes care of low‑level details so you can focus on your project tasks.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs: