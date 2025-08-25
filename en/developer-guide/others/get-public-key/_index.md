---
title: "Get public key"
second_title: "Developer Guide"
linktitle: "Get public key"
type: docs
url: /get-public-key/
keywords: ""
description: "Get an asymmetric public key. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : GetPublicKey**

Get an asymmetric public key. 

## **Interface Details**

### **Endpoint** 

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Function Description**

Retrieves the public key portion of an asymmetric encryption algorithm.Asymmetric encryption algorithms (such as RSA, ECC, etc.) use a pair of keys: a public key and a private key.The public key is used for encrypting data or verifying signatures, while the private key is used for decrypting data or generating signatures.The primary purpose of the GetPublicKey method is to extract and return the public key portion for use when needed.

### The request parameters of **getPublicKey** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 


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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

