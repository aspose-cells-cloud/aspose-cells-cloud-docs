---
title: "Aspose.Cells Cloud Web API - Post Access Token"
date: 2023-11-15
lastmod: 2024-06-15
articleTitle: "Get Access Token with Client ID and Secret"
linktitle: "Post Access Token"
keywords: "Aspose.Cells Cloud, OAuth2, access token, REST API, JWT, authentication, Excel cloud, client credentials flow"
description: "Obtain an OAuth2 access token for Aspose.Cells Cloud REST API using client credentials. Includes secure cURL examples, SDK integrations, error handling, and best practices for token management in Excel cloud operations."
weight: 100
draft: false
---

# Get Access Token with Client ID and Secret

Before calling this endpoint, ensure you have:

* A registered [Aspose Cloud account](https://dashboard.aspose.cloud/).
* A **Client ID** and **Client Secret** generated in the [Aspose Cloud dashboard](https://dashboard.aspose.cloud/authorization).

> 🔒 **Security Best Practice**: Store `client_id` and `client_secret` in environment variables or a secrets manager — *never* in source code, configuration files, or client-side JavaScript.

---

## API Endpoint

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### Authentication Flow

This API acts as a secure proxy to the Aspose Cloud authorization service. It accepts your client credentials via OAuth 2.0 **client credentials flow**, forwards them to the authorization server, and returns the resulting JWT (JSON Web Token) access token — *not* a raw JWT, but a token *issued* by Aspose Cloud and intended for use with Aspose.Cells Cloud APIs.

> ℹ️ **Note**: The returned `access_token` is a JWT with a 1-hour (`expires_in: 3600`) lifetime. Use it in the `Authorization: Bearer <token>` header for all subsequent API calls.

---

## Request Parameters

| Parameter     | Type   | Location                 | Description                                      |
|---------------|--------|--------------------------|--------------------------------------------------|
| `grant_type`  | string | body (form‑url‑encoded)  | Must be `client_credentials` for OAuth2.         |
| `client_id`   | string | body (form‑url‑encoded)  | Your Aspose Cloud client identifier.             |
| `client_secret`| string| body (form‑url‑encoded)  | Your Aspose Cloud client secret.                 |

---

## Example Request (cURL)

```bash
# ⚠️ Never commit secrets! Use environment variables.
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=${ASPOSE_CLIENT_ID}&client_secret=${ASPOSE_CLIENT_SECRET}"
```

> 🔐 **Recommended**: Set credentials in `.env` or your CI/CD secrets:
> ```bash
> export ASPOSE_CLIENT_ID="your-client-id"
> export ASPOSE_CLIENT_SECRET="your-client-secret"
> ```

---

## Response

### Success (200 OK)

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJhYmMxMjMiLCJleHAiOjE3MTYwOTk2MDB9.xxxxx",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

### Error Responses

| Code | Meaning           | Description                                  | Example                                                                 |
|------|-------------------|----------------------------------------------|-------------------------------------------------------------------------|
| 400  | Bad Request       | Missing or malformed parameters (e.g., missing `grant_type`) | ```json {"error": "invalid_request", "error_description": "Missing grant_type."}``` |
| 401  | Unauthorized      | Invalid or expired `client_id`/`client_secret` | ```json {"error": "invalid_client", "error_description": "Client authentication failed."}``` |
| 500  | Internal Server Error | Temporary service disruption              | ```json {"error": "server_error", "error_description": "An unexpected error occurred."}``` |

> ℹ️ **Token Expiration**: Always check `expires_in`. Renew tokens *before* expiration to avoid 401 errors in downstream calls.

---

## How to Use the Access Token with SDKs

Using an SDK is the fastest and safest way to obtain and manage tokens. SDKs handle token caching, expiration, and secure credential storage.

### Supported SDKs

- [.NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)
- [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java)
- [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python)
- [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-javascript)
- [PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php)
- [Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby)
- [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go)

Check the [GitHub organization](https://github.com/aspose-cells-cloud){: rel="noopener noreferrer"} for the full list and installation guides.

### Example (Node.js SDK)

```javascript
const { CellsApi } = require("aspose-cells-cloud");

const cellsApi = new CellsApi({
  clientId: process.env.ASPose_CLIENT_ID,
  clientSecret: process.env.ASPose_CLIENT_SECRET,
  basePath: "https://api.aspose.cloud",
  authPath: "https://api.aspose.cloud/connect/token"
});

// Token is fetched automatically on first API call
cellsApi.cellsWorkbookPutConvertWorkbook(
  { file: "input.xlsx", format: "pdf" },
  (err, result) => {
    if (err) throw err;
    console.log("Conversion successful.");
  }
);
```

> ✅ SDKs automatically:
> - Fetch and cache tokens
> - Refresh expired tokens (if refresh tokens are supported)
> - Handle retries and error parsing

---

## OpenAPI Specification

The API is fully defined in the [machine-readable OpenAPI spec](https://raw.githubusercontent.com/aspose-cells-cloud/aspose-cells-cloud-openapi-spec/main/specs/cells_api.yaml) (YAML/JSON), enabling code generation and contract testing.

You can also explore the interactive reference at:  
[reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken)

---

## Related Documentation

- [Getting Started: API Authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [OAuth 2.0 Overview](https://docs.aspose.cloud/total/getting-started/oauth2/)
- [Managing API Credentials](https://dashboard.aspose.cloud/authorization)
- [Error Handling Best Practices](https://docs.aspose.cloud/total/working-with-errors/)

---

## Security Considerations

1. **Transport Security**: Always use HTTPS. Never send credentials over HTTP.
2. **Token Storage**: Store tokens in memory or secure storage (e.g., environment variables, vaults like HashiCorp Vault or AWS Secrets Manager).
3. **Token Lifecycle**: Implement token refresh logic. Do not hardcode tokens.
4. **Client-Side Use**: Avoid using client credentials directly in browser-based apps. Use a backend proxy to obtain tokens.

> ⚠️ **Critical**: If you suspect credential exposure (e.g., accidentally committed to Git), immediately rotate your `client_id` and `client_secret` in the [Aspose Cloud dashboard](https://dashboard.aspose.cloud/authorization).