---
title: "Aspose.Cells Cloud Web API - Get Aspose Cells Cloud Status"
second_title: "Document"
ArticleTitle: "Get Aspose.Cells Cloud Status"
linktitle: "Get Aspose Cells Cloud Status"
type: docs
url: /get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, Cloud API, Health Check, Excel, REST"
description: "Monitor the Health Status of Aspose.Cells Cloud Service in real-time."
weight: 100
---

Get the Health Status of the Aspose.Cells Cloud Service in real-time.

**Prerequisites:** To call this API you must obtain a Bearer access token using your Aspose Cloud client credentials. Include the token in the `Authorization` header as `Bearer {access_token}`.

## **Get Aspose.Cells Cloud Status**

### **Web API**

The endpoint uses the HTTP **GET** method and does not require a request body.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                 |
| -------------- | ------ | --------------------------- | ------------------------------------------- |
| Authorization  | String | Header                      | Bearer token for authentication (required). |
| format         | String | Query                       | Desired response format, e.g., `json`.      |

### **Response**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Response Schema**

| Field     | Type              | Description                              |
| --------- | ----------------- | ---------------------------------------- |
| status    | string            | Service health (`OK`, `Degraded`, etc.). |
| service   | string            | Name of the service.                     |
| timestamp | string (ISO‑8601) | Time of the status check.                |

The API returns a standard JSON payload that includes the current health **status** of the Aspose.Cells Cloud service.

**HTTP Status Codes**

- **200 OK** – The service is healthy and the response contains the status information.
- **401 Unauthorized** – Missing or invalid authentication token.
- **503 Service Unavailable** – The service is currently down for maintenance or experiencing issues.

## How to Use the Get Aspose.Cells Cloud Status API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) defines a publicly accessible programming interface that allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK simplifies integration and reduces boilerplate code. The SDK handles the underlying details, allowing you to retrieve the Aspose.Cells Cloud run status with minimal effort. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
