---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "Document"
ArticleTitle: "Get Access Token with Client ID and Secret"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Aspose.Cells Cloud, Access Token, OAuth2, API Authentication, REST API, Excel, Office Cloud"
description: "Obtain an OAuth2 access token for Aspose.Cells Cloud by calling the POST /cells/connect/token endpoint with your client ID and secret."
weight: 100
---

Retrieve an access token using the Cells Cloud Get Token API with a client ID and secret.

## **Post Access Token API**

### **Web API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Request Parameters:**

| Parameter Name | Type   | Location | Description                               |
| -------------- | ------ | -------- | ----------------------------------------- |
| Client ID      | string | query    | The client identifier issued to you.      |
| Client Secret  | string | query    | The secret associated with the client ID. |

### **Response**

```json
[
  {
    "Name": "String",
    "DataType": {
      "Identifier": "String",
      "Name": "string"
    }
  }
]
```

## How to Use the Get public key API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) defines a publicly accessible programming interface, allowing you to perform REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to get started. The SDK abstracts the underlying HTTP details, enabling you to obtain an access token for Cells with minimal code.

Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs. An SDK takes care of low‑level details so you can focus on your project tasks.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:
