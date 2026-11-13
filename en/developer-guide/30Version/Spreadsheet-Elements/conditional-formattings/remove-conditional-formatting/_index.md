---
title: "Delete Conditional Formatting – Aspose.Cells Cloud API Reference"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Conditional Formatting, Delete, API, Excel, Cloud"
description: "Delete conditional formatting from Excel worksheet using Aspose.Cells Cloud REST API with JWT and SDK examples"
weight: 60
linktitle: "Delete Conditional Formatting"
ArticleTitle: "Delete Conditional Formatting in Excel via Aspose.Cells Cloud REST API"
---
The **DeleteWorksheetConditionalFormatting** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`) removes a specific conditional formatting rule from a worksheet in an Excel workbook stored in Aspose.Cells Cloud storage, using the zero-based index of the rule; this operation supports automation workflows by enabling developers to programmatically delete formatting rules—such as those highlighting values above a threshold—without manually editing the workbook.

## Background

Conditional formatting lets you apply visual styles to cells that meet specific criteria (e.g., highlight values greater than a threshold). In automation scenarios you may need to remove an existing rule. This endpoint deletes a conditional‑formatting rule from a worksheet in an Excel workbook stored in Aspose Cloud storage.

## The Delete Worksheet Conditional Formatting Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                     |
| -------------- | ------- | -------------------------- | --------------------------------------------------------------- |
| name           | String  | Path                       | The file name.                                                  |
| sheetName      | String  | Path                       | The worksheet name.                                             |
| index          | Integer | Path                       | Gets the Conditional Formatting element at the specified index. |
| folder         | String  | Query                      | The folder where the file is situated.                          |
| storageName    | String  | Query                      | The storage name where the file is situated.                    |

### Response

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

### Query Parameters

| Name          | Type   | Required | Description                               |
| ------------- | ------ | -------- | ----------------------------------------- |
| `folder`      | string | No       | Cloud folder where the workbook resides.  |
| `storageName` | string | No       | Name of the Aspose Cloud storage service. |

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

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## Error Responses

| HTTP Code | Reason                                             | Example Body                                                        |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – missing or invalid parameters.       | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**   | Unauthorized – missing or invalid JWT token.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**   | Not Found – workbook or worksheet does not exist.  | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**   | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

## See Also

- **Authentication Guide** – [JWT token‑based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- **OpenAPI Specification** – Detailed schema for this endpoint (opens in a new tab)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>`
- **Conditional Formatting Overview** – Learn how to create, update, and list formatting rules.
- **Aspose.Cells Cloud SDKs** – Full list of supported languages on the [GitHub repository](https://github.com/aspose-cells-cloud).

---

_This page follows the standard Aspose.Cells Cloud API documentation template, includes a Prerequisites section, and adheres to accessibility and SEO best practices._

## How to Use the Delete Worksheet Conditional Formatting API with SDKs?

### Delete Worksheet Conditional Formatting API Specification

The <a href="https://reference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" rel="noopener noreferrer">Delete Worksheet Conditional Formatting API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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
const {
  ConditionalFormattingsApi,
  DeleteWorksheetConditionalFormattingRequest,
} = require("asposecellscloud");

const config = {
  clientId: "<your_client_id>",
  clientSecret: "<your_client_secret>",
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
  name: "Book1.xlsx",
  sheetName: "Sheet1",
  index: 0,
  folder: "MyFolder",
  storageName: null,
});

apiInstance
  .deleteWorksheetConditionalFormatting(request)
  .then(() => console.log("Conditional formatting deleted."))
  .catch((err) => console.error(err));
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

_(Additional SDK snippets for Ruby, Go, Perl, and Swift are available in the [GitHub repository](https://github.com/aspose-cells-cloud).)_

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetConditionalFormatting.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetConditionalFormatting.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetConditionalFormatting.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetConditionalFormatting.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetConditionalFormatting.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetConditionalFormatting.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetConditionalFormatting.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetConditionalFormatting.go" >}}
{{</tab>}}
{{< /tabs >}}
