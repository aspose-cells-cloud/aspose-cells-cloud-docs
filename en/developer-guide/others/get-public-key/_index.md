---
title: "Aspose.Cells Cloud API – Get Public Key (v4.0) | REST Documentation"
second_title: "Document"
ArticleTitle: "Get Public Key"
linktitle: "Get Public Key"
type: docs
url: /get-public-key/
keywords: "aspose cells cloud, public key API, asymmetric encryption, REST API, Excel API"
description: "Retrieve the asymmetric public key used for encrypting data with Aspose.Cells Cloud. Learn request format, parameters, sample responses, and SDK usage examples."
weight: 100
---

This API retrieves the public key from an asymmetric encryption algorithm.

## **Get Public Key API**

### **Web API**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

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

## How to Use the Get public key API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) defines a publicly accessible programming interface, enabling you to perform REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement get public key for cells with minimal code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
