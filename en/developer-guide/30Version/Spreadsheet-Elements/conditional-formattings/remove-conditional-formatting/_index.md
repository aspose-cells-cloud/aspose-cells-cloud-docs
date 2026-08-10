---
title: "Delete Conditional Formatting – Aspose.Cells Cloud API Reference"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Conditional Formatting, Delete, API, Excel, Cloud"
description: "Remove a conditional formatting rule from a worksheet using Aspose.Cells Cloud REST API. Includes parameters, authentication, request/response examples, and SDK snippets."
weight: 60
---

# Delete Conditional Formatting

## Background
Conditional formatting lets you apply visual styles to cells that meet specific criteria (e.g., highlight values greater than a threshold). In automation scenarios you may need to remove an existing rule. This endpoint deletes a conditional‑formatting rule from a worksheet in an Excel workbook stored in Aspose Cloud storage.

## Prerequisites
- An **Aspose Cloud** account with **Cells** product enabled.  
- **JWT access token** generated via the OAuth 2.0 client‑credentials flow.  
- The workbook (`{name}`) must already exist in the specified **folder** and **storage** (if any).  
- API version **v3.0** (default) is used in the URLs shown below.

## Authentication
All Aspose.Cells Cloud endpoints require **JWT token‑based authentication**.

```http
Authorization: Bearer <access_token>
```

### Obtain an access token (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Response**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Use the returned `access_token` in the `Authorization` header for every request.

## HTTP Request

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Path Parameters

| Name      | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `name`    | string | Yes      | The workbook file name (e.g., `Book1.xlsx`). |
| `sheetName` | string | Yes   | The worksheet that contains the conditional formatting. |
| `index`   | integer| Yes      | Zero‑based index of the conditional‑formatting rule to delete. |

### Query Parameters

| Name        | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `folder`    | string | No       | Cloud folder where the workbook resides. |
| `storageName`| string| No      | Name of the Aspose Cloud storage service. |

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Successful Response

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## Error Responses

| HTTP Code | Reason | Example Body |
|-----------|--------|--------------|
| **400**   | Bad Request – missing or invalid parameters. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**   | Unauthorized – missing or invalid JWT token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – workbook or worksheet does not exist. | `{ "Code":"404", "Message":"File not found." }` |
| **500**   | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## SDK Examples
The following snippets demonstrate how to invoke the **Delete Conditional Formatting** operation using the official Aspose.Cells Cloud SDKs.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// Configure API client
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Delete conditional formatting
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Conditional formatting deleted.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Conditional formatting removed.")
```

*(Additional SDK snippets for Ruby, Go, Perl, and Swift are available in the [GitHub repository](https://github.com/aspose-cells-cloud).)*

## See Also
- **Authentication Guide** – [JWT token‑based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **OpenAPI Specification** – Detailed schema for this endpoint (opens in a new tab)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>`  
- **Conditional Formatting Overview** – Learn how to create, update, and list formatting rules.  
- **Aspose.Cells Cloud SDKs** – Full list of supported languages on the [GitHub repository](https://github.com/aspose-cells-cloud).  

---  

*This page follows the standard Aspose.Cells Cloud API documentation template, includes a Prerequisites section, and adheres to accessibility and SEO best practices.*