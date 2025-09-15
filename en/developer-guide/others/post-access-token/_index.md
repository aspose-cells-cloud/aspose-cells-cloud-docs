---
title: "Aspose.Cells Cloud Web API - Post Access Token"
second_title: "Document"
ArticleTitle: "Get Access Token with Client ID and Secret"
linktitle: "Post Access Token"
type: docs
url: /post-access-token/
keywords: "Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Management"
description: "Retrieve an Access Token using the Cells Cloud Get Token API, which acts as a proxy service forwarding user requests to the Aspose Cloud authentication server, and returns the resulting access token to the client securely."
weight: 100
kwords: "Excel, Office Cloud, REST API, Authentication, Token Management, Middleware Integration, Secure API, Aspose Cloud"
---

Retrieve an Access Token using the Cells Cloud Get Token API with Client ID and Secret.

## **Post Access Token API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
| :- | :- | :- |:- |
| Client ID | string | query | Client ID |
| Client Secret | string | query | Client Secret |

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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) defines a publicly accessible programming interface, allowing you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement get access token for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.nt. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
