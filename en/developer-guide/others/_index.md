---
title: "Aspose.Cells Cloud API – Other Features (Health Check, Public Key, Access Token)"
linktitle: "Other Features"
ArticleTitle: "Other Features: Health Check, Public Key, Access Token"
second_title: "Document"
type: docs
url: /other-features/
keywords: "Aspose.Cells Cloud, health check, public key, access token, OAuth2, Excel, REST API"
description: "Learn how to use Aspose.Cells Cloud other features such as the health‑check endpoint, public key retrieval, and OAuth 2.0 access token generation to secure Excel API integrations."
weight: 180
---

**Prerequisites** – To use the features listed below you must have a valid Aspose Cloud subscription and an active **Client ID** / **Client Secret** pair for authentication.

These other features provide essential support operations for the Aspose.Cells Cloud API, including confirming service availability, retrieving cryptographic keys, and obtaining access tokens. They are typically invoked before using workbook‑related endpoints.

- **[Aspose.Cells Cloud Health Check](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Verify that the Aspose.Cells Cloud service is reachable and operating correctly. A successful call returns **HTTP 200** with JSON `{ "status": "OK" }`. Use this endpoint early in your workflow to avoid unnecessary failures.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Read more</a>

- **[Get Aspose.Cells Cloud Run Status](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Retrieve the current run‑time status of the service. The response indicates whether the API is fully operational, in maintenance mode, or experiencing issues.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Read more</a>

- **[Get Public Key](https://docs.aspose.cloud/cells/get-public-key/)**  
  Obtain the RSA public key (PEM format) used to verify JWT tokens issued by Aspose.Cells Cloud. This key is required when you validate tokens on your server.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Read more</a>

- **[Get Access Token with Client ID and Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  Generate an OAuth 2.0 access token using the **client_credentials** grant type. Include your **Client ID** and **Client Secret** in the request body; the response contains `access_token`, `token_type`, and `expires_in`. This token must be supplied in the `Authorization` header for all subsequent API calls.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Read more</a>