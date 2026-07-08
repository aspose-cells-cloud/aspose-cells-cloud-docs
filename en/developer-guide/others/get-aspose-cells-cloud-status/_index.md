---
title: "Aspose.Cells Cloud Web API - Get Aspose Cells Cloud Status"
second_title: "Document"
ArticleTitle: "Get Aspose.Cells Cloud Run Status"
linktitle: "Get Aspose Cells Cloud Status"
type: docs
url: /get-aspose-cells-cloud-status/
keywords: "Aspose.Cells Cloud, health status, API, Excel, REST, service monitoring, SLA, status check"
description: "Monitor the Health Status of Aspose.Cells Cloud Service in real-time."
weight: 100
---


Get the Health Status of the Aspose.Cells Cloud Service in real-time.

## **Get Aspose.Cells Cloud Status**

### **Web API**

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                 |
|----------------|--------|-----------------------------|---------------------------------------------|
| Authorization  | String | Header                      | Bearer token for authentication (required).|
| format         | String | Query                       | Desired response format, e.g., `json`.     |

### **Response**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

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

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

*Add SDK-specific examples here as needed.*

For more information on overall cloud service health, see the [Health Check API](./health-check/) page.  

---