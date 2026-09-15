---
title: "Evaluate Aspose.Cells Cloud"
description: "Try Aspose.Cells Cloud REST API for free: convert, merge, split Excel files in the cloud. Includes 150 API calls/month. No credit card required."
date: 2024-02-14T10:00:00Z
lastmod: 2024-03-28T14:30:00Z
draft: false
tags: ["cloud", "excel", "rest-api", "trial"]
categories: ["product-overview"]
weight: 60
aliases: ["/cells/evaluate/", "/cloud/try-cells/"]
url: /evaluate-aspose-cells/
---

You can evaluate the **Aspose.Cells Cloud** REST APIs by creating a free-trial account on the Aspose Cloud Dashboard. After registration, you will receive a **Client Id** and **Client Secret** that allow up to 150 API calls per month.

**Prerequisites**  
Before you begin, ensure you have an active internet connection and a supported development environment. The API can be called directly via HTTP, or you can use one of the Aspose.Cells SDKs (e.g., [.NET](/cells/net/), [Java](/cells/java/), [Python](/cells/python/), PHP) for easier integration.

**Quick start steps**

1. **Create a free-trial account** – visit the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud), sign up, and confirm your email address.  
   ![Aspose.Cells Cloud dashboard with authentication section highlighted](/images/dashboard-auth.png)  
2. **Obtain credentials** – locate the *Client Id* and *Client Secret* in the dashboard’s **Authentication** section.  
3. **Generate an access token** – send a `POST` request to `https://api.aspose.cloud/connect/token` with your credentials (see the API reference for the exact payload).  
4. **Make your first API call** – include the token in the `Authorization: Bearer <token>` header and call a simple endpoint, e.g., `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`.  

The free-trial gives you a practical sense of the service’s capabilities, allowing early development and testing without any cost.

**API reference summary**

| Operation | Method | URL | Required parameters | Sample response |
|-----------|--------|-----|---------------------|-----------------|
| Get access token | `POST` | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (form‑urlencoded) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| List worksheets | `GET` | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | Path: `{file}` – name of the uploaded workbook; Header: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

For detailed pricing, usage limits, and additional plan options, see the [Trial Plan](https://purchase.aspose.cloud/trial) page. For more information on Aspose.Cells Cloud pricing, visit our [Pricing](/cells/pricing/) page.

> *Note: `v3.0` is current. `v2.0` endpoints are deprecated as of 2023-12.*