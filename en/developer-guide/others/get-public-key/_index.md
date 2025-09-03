---
title: "Get Public Key - Excel API"
second_title: "Aspose.Cells Cloud"
linktitle: "Get Public Key"
type: docs
url: /get-public-key/
keywords: "asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integration"
description: "Retrieve an asymmetric public key for secure data encryption."
weight: 100
kwords: "asymmetric encryption, public key, REST API, Excel API, security, data encryption, API integration, JSON, API documentation"
---

# **Excel API: Get Public Key**

Retrieve an asymmetric public key for secure data encryption.

## **Interface Details**

### **Endpoint**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Function Description**

The GetPublicKey method retrieves the public key from an asymmetric encryption algorithm. Asymmetric algorithms (such as RSA and ECC) utilize a pair of keys: a public key for encrypting data or verifying signatures and a private key for decrypting data or generating signatures. This method is essential for obtaining the public key when needed for secure operations.

### The request parameters of **getPublicKey** API are

| Parameter Name | Type | Path/Query String/HTTP Body | Description |
| :- | :- | :- | :- |
|  |  |  |  |

### **Response Description**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
        "Name": "class:cellscloudpublickey"
      }
    },
    {
      "Name": "Code",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "Integer",
        "Name": "integer"
      }
    },
    {
      "Name": "Status",
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": true,
      "DataType": {
        "Identifier": "String",
        "Name": "string"
      }
    }
  ]
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) defines a publicly accessible programming interface, enabling you to perform REST interactions directly from your web browser.

## Excel API SDK

Utilizing an SDK is the most efficient way to accelerate development. An SDK manages low-level details, allowing you to concentrate on your project tasks. For a comprehensive list of Aspose.Cells Cloud SDKs, please consult the [GitHub repository](https://github.com/aspose-cells-cloud).

The following code examples illustrate how to interact with Aspose.Cells web services using various SDKs:
