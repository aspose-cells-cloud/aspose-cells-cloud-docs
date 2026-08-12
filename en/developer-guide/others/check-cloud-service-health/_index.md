---
title: "Aspose.Cells Cloud – Check Service Health (API)"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Health Check"
linktitle: "Check Cloud Service Health"
type: docs
url: /check-cloud-service-health/
keywords: "Aspose.Cells Cloud, API health check, REST status, cloud service monitoring"
description: "Monitor Aspose.Cells Cloud health in real‑time. Learn the GET /v4.0/cells/status/check endpoint, parameters, response format, and SDK examples."
weight: 100
---

Check the health status of Aspose.Cells Cloud services.

**Prerequisites**  
To call this endpoint you must have a valid Aspose Cloud access token. Obtain the token by registering an application in the Aspose Cloud Dashboard and using the client‑id and client‑secret to request a Bearer token via the OAuth2 token endpoint. Include the token in the `Authorization` header as shown below.

## **Check Cloud Service Health**

### **Web API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

| Parameter     | Type   | Required | Description                                                        |
| ------------- | ------ | -------- | ------------------------------------------------------------------ |
| Authorization | header | Yes      | Bearer token for authentication (`Authorization: Bearer <token>`). |
| detail        | query  | No       | Set to `true` to include detailed component information.           |
| Accept        | header | No       | Desired response format, default is `application/json`.            |

### **Response**

The service returns a JSON payload when the request succeeds.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Operational",
    "storage": "Operational",
    "database": "Operational"
  }
}
```

**HTTP status codes**

| Code | Meaning             | Description                                              |
| ---- | ------------------- | -------------------------------------------------------- |
| 200  | OK                  | The service is healthy; see the JSON example above.      |
| 401  | Unauthorized        | Invalid or missing authentication token.                 |
| 503  | Service Unavailable | The service is currently unhealthy or under maintenance. |
| 4xx  | Client error        | Incorrect request parameters or malformed request.       |
| 5xx  | Server error        | Unexpected server failure; retry later.                  |

## How to Use the Aspose.Cells Cloud Status API with SDKs

### OpenAPI Specification

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to implement a cloud health check for Cells with minimal code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

Below are sample snippets that demonstrate how to call the health‑check endpoint with the most common SDKs.
