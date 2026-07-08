---
title: "Aspose.Cells Cloud – Check Service Health (API)"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Health Check"
linktitle: "Check Cloud Service Health"
type: docs
url: /check-cloud-service-health/
keywords: "Aspose, Cells, Cloud, API, health check, REST"
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

| Parameter      | Type   | Required | Description                                                     |
|----------------|--------|----------|-----------------------------------------------------------------|
| Authorization  | header | Yes      | Bearer token for authentication (`Authorization: Bearer <token>`). |
| detail         | query  | No       | Set to `true` to include detailed component information.       |
| Accept         | header | No       | Desired response format, default is `application/json`.        |

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

| Code | Meaning                     | Description                                                                      |
|------|-----------------------------|----------------------------------------------------------------------------------|
| 200  | OK                          | The service is healthy; see the JSON example above.                             |
| 401  | Unauthorized                | Invalid or missing authentication token.                                         |
| 503  | Service Unavailable         | The service is currently unhealthy or under maintenance.                         |
| 4xx  | Client error                | Incorrect request parameters or malformed request.                               |
| 5xx  | Server error                | Unexpected server failure; retry later.                                          |

## How to Use the Aspose.Cells Cloud Status API with SDKs

### OpenAPI Specification

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to implement a cloud health check for Cells with minimal code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

Below are sample snippets that demonstrate how to call the health‑check endpoint with the most common SDKs.

**C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AccessToken = "<your_access_token>",
    BasePath = "https://api.aspose.cloud"
};

var statusApi = new CellsStatusApi(config);
var response = statusApi.CheckCloudServiceHealth();
Console.WriteLine($"Status: {response.Status}, Timestamp: {response.Timestamp}");
```

**Java**

```java
import com.aspose.cloud.cells.api.CellsStatusApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.model.CheckResponse;

ApiClient client = new ApiClient();
client.setAccessToken("<your_access_token>");
client.setBasePath("https://api.aspose.cloud");

CellsStatusApi api = new CellsStatusApi(client);
CheckResponse result = api.checkCloudServiceHealth();
System.out.println("Status: " + result.getStatus() + ", Timestamp: " + result.getTimestamp());
```

**Python**

```python
from asposecellscloud import CellsStatusApi, ApiClient

client = ApiClient()
client.access_token = "<your_access_token>"
client.base_path = "https://api.aspose.cloud"

api = CellsStatusApi(client)
response = api.check_cloud_service_health()
print(f"Status: {response.status}, Timestamp: {response.timestamp}")
```

**Node.js**

```javascript
const { CellsStatusApi, ApiClient } = require('asposecellscloud');

let client = new ApiClient();
client.accessToken = '<your_access_token>';
client.basePath = 'https://api.aspose.cloud';

let api = new CellsStatusApi(client);
api.checkCloudServiceHealth()
   .then(response => {
       console.log(`Status: ${response.status}, Timestamp: ${response.timestamp}`);
   })
   .catch(error => console.error(error));
```

These examples illustrate the basic pattern: instantiate the appropriate SDK client with your access token, call `CheckCloudServiceHealth`, and process the returned status information. Adjust the code as needed for error handling based on the HTTP status‑code table above.