---
title: "Aspise.Cells Cloud Web API – Other Features: Health Check, Get Public Key"
linktitle: "Other Features"
ArticleTitle: "Other Features: Health Check, Get Public Key"
second_title: "Document"
type: docs
url: /other-features/
keywords: "Aspose.Cells, Cloud API, health check, public key, access token, Excel, REST"
description: "Explore Aspose.Cells Cloud other features: health‑check endpoint, public key retrieval, and token generation to secure your Excel API integrations."
weight: 180
---

**Prerequisites** – To use the features listed below you must have a valid Aspose Cloud subscription and an active **Client ID** / **Client Secret** pair for authentication.

These “Other Features” provide essential support operations for the Aspose.Cells Cloud API, such as confirming service availability, retrieving cryptographic keys, and obtaining access tokens. They are typically called before working with workbook‑related endpoints.

- **[Aspose.Cells Cloud Health Check](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Verify that the Aspose.Cells Cloud service is reachable and operating correctly. A successful call returns **HTTP 200** with JSON `{ "status": "OK" }`. Use this endpoint early in your workflow to avoid unnecessary failures.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Read more</a>

- **[Get Aspose.Cells Cloud Run Status](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Retrieve the current run‑time status of the service. The response indicates whether the API is fully operational, in maintenance mode, or experiencing issues.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Read more</a>

- **[Get Public Key](https://docs.aspose.cloud/cells/get-public-key/)**  
  Obtain the RSA public key (PEM format) used to verify JWT tokens issued by Aspose.Cells Cloud. This key is required when you validate tokens on your server side.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Read more</a>

- **[Get Access Token with Client ID and Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  Generate an OAuth 2.0 access token using the **client_credentials** grant type. Include your **Client ID** and **Client Secret** in the request body; the response contains `access_token`, `token_type`, and `expires_in`. This token must be supplied in the `Authorization` header for all subsequent API calls.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Read more</a>

**FAQ**

**Q:** *How can I verify that Aspose.Cells Cloud is up before calling other APIs?*  
**A:** Call the **Health Check** endpoint `GET /cells/healthcheck`. A response of `200 OK` with `{ "status": "OK" }` confirms the service is reachable.

**Q:** *What is the purpose of the public key?*  
**A:** The public key returned by **Get Public Key** is used to validate JWT tokens that Aspose.Cells Cloud issues for authenticated requests.

**Q:** *How do I obtain an access token?*  
**A:** Use the **Post Access Token** endpoint `POST /connect/token` with `grant_type=client_credentials`, providing your **Client ID** and **Client Secret**. The API returns a JSON object containing the `access_token`.