---
title: "Post access token"
second_title: "Aspose.Cells Cloud Document"
linktitle: "Post access token"
type: docs
url: /post-access-token/
keywords: ""
description: "Get Access Token Result: The Cells Cloud Get Token API acts as a proxy service,forwarding user requests to the Aspose Cloud authentication server and returning the resulting access token to the client. "
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Match all blank cells in an Excel worksheet
---

# **Excel API : PostAccessToken **

Get Access Token Result: The Cells Cloud Get Token API acts as a proxy service,forwarding user requests to the Aspose Cloud authentication server and returning the resulting access token to the client. 

## **Interface Details**

### **Endpoint** 

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Function Description**

- This API acts as an intermediary proxy, transparently forwarding client authentication requests to the Aspose Cloud authorization service.- Upon successful authentication, the access token issued by Aspose Cloud is returned intact to the caller.- Use cases: Middleware systems requiring integration with Aspose Cloud services that delegate OAuth or similar authentication processes.- Considerations:▸ Ensure valid Aspose Cloud API credentials are registered before invocation.▸ Should be invoked over HTTPS secure channels to prevent token leakage.▸ Securely store returned access tokens and implement proper expiration management.▸ Handle potential error responses (e.g., 401 Unauthorized, 503 Service Unavailable).

### The request parameters of **postAccessToken** API are: 

| Parameter Name | Type | Path/Query String/HTTPBody | Description | 
| :- | :- | :- |:- | 


### **Response Description**
```json
{
String
}
```

## OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

## Excel API SDK 

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

