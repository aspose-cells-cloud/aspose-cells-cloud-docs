---
title: "Aspose.Cells Cloud – Check Service Health (API)"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Health Check"
linktitle: "Check Cloud Service Health"
type: docs
url: /check-cloud-service-health/
keywords: "Aspose Cells Cloud, API health check, service status, REST API, Excel cloud, monitoring"
description: "Monitor Aspose.Cells Cloud health in real‑time. Learn the GET /v4.0/cells/status/check endpoint, parameters, response format, and SDK examples."
weight: 100
---

Check the health status of Aspose.Cells Cloud services.

## **Check Cloud Service Health**

### **Web API**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Request Parameters**

### **Response**

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "2024-03-28T12:34:56Z",
  "components": {
    "api": "Operational",
    "storage": "Operational",
    "database": "Operational"
  }
}
```

## How to Use the Aspose.Cells Cloud Status API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to implement a cloud health check for Cells with minimal code.  
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
