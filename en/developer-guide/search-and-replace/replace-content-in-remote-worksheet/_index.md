---
title: "Aspose.Cells Cloud Replace Web API – Update Text in Remote Worksheet"
second_title: "Document"
ArticleTitle: "Find and Replace Text in Remote Worksheet with Aspose.Cells Cloud API"
linktitle: "Replace Remote Worksheet Content"
type: docs
url: /replace-content-in-remote-worksheet/
keywords: "Aspose.Cells, replace text, remote worksheet, Excel API, cloud spreadsheet, find and replace, REST API"
description: "Replace text in a specific worksheet of an Excel file stored in Aspose Cloud. Supports password‑protected workbooks, region‑aware search, bulk updates, and returns operation status for Excel API, cloud find‑replace, and remote worksheet editing."
weight: 100
---

Replace specified text within a particular worksheet of remote Excel files. Update content in targeted spreadsheet sheets efficiently using Aspose.Cells Find and Replace API for precise worksheet editing.

## **Replace Content in Remote Worksheet API**

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" target="_blank" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Request Parameters**

| Parameter Name | Type   | Path/Query String/HTTPBody | Description                                                                                                                                                                  |
| :------------- | :----- | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                       | The name of the workbook file stored in cloud storage to be modified (e.g., `"sales_report.xlsx"`, `"budget_2024.xls"`).                                                     |
| worksheet      | String | Path                       | The name of the specific worksheet where the find‑and‑replace operation will be performed (e.g., `"Q1_Sales"`, `"Sheet1"`).                                                  |
| searchText     | String | Query                      | The text string to search for within the specified worksheet. The search applies to all cells in the worksheet unless further constrained.                                   |
| replaceText    | String | Query                      | The text string that will replace all occurrences of `searchText` found within the specified worksheet.                                                                      |
| folder         | String | Query                      | The cloud storage folder path where the source workbook is located (e.g., `"/reports/monthly/"`, `"/finance/"`).                                                             |
| storageName    | String | Query                      | _(Optional)_ The name of the custom cloud storage (e.g., `"CorporateS3"`, `"AzureArchive"`). If omitted, the default cloud storage for your account is used.                 |
| region         | String | Query                      | _(Optional)_ Sets the locale for text handling, which may affect character encoding and language‑specific search behavior within the worksheet (e.g., `"en-GB"`, `"es-ES"`). |
| password       | String | Query                      | _(Optional)_ If the workbook is password‑protected, provide the password to open and modify the file.                                                                        |

**Example request (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/sales_report.xlsx/worksheets/Sheet1/replace/content?searchText=OldValue&replaceText=NewValue&folder=/reports" \
     -H "Authorization: Bearer {access_token}"
```

### **Response**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Response Status Codes**

- **200 OK** – The replace operation completed successfully. The response may include an additional field `ReplacedCount` indicating how many occurrences were replaced.  
- **202 Accepted** – The request has been accepted for asynchronous processing; a separate job ID will be returned.  
- **204 No Content** – The operation succeeded but there is no content to return (used when only status is needed).  
- **400 Bad Request** – Required parameters are missing or malformed.  
- **401 Unauthorized** – Access token is missing, invalid, or the client credentials are wrong.  
- **404 Not Found** – The specified workbook or worksheet cannot be found.  
- **500 Internal Server Error** – An unexpected error occurred while processing the request.

### **Error Codes**

| Code | Description                              | When it occurs                                                   |
|------|------------------------------------------|------------------------------------------------------------------|
| 400  | Bad Request                              | The request URI is malformed or required parameters are missing. |
| 401  | Unauthorized                             | Access token is missing, invalid, or the client credentials are wrong. |
| 404  | Not Found                                | The specified workbook or worksheet cannot be found.            |
| 500  | Internal Server Error                    | An unexpected error occurred while processing the request.      |

## Where should we use the Replace content of Worksheet in Remote Spreadsheet API?

- **Batch Cloud File Update**: Modify the contents of multiple Excel files stored in cloud storage such as AWS S3 and Azure Blob.  
- **Dynamic population of cloud templates**: Batch‑populate dynamic data for report templates stored in the cloud.  
- **Cross‑region file synchronization**: Synchronize the content consistency of Excel files in cloud storage across different geographical regions.

## Why should you use the Replace content of Worksheet in Remote Spreadsheet API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom chart‑rendering solutions, this significantly reduces development workload.  
- **Reduced Labor Costs**: Decreases the need for personnel dedicated to document consolidation.  
- **Pay‑per‑use**: No upfront investment; you only pay for API calls actually used.  
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.

## How to Use the Replace content of Worksheet in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and allows you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content of worksheet in spreadsheets for cells with minimal code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

Below are concise examples for the most popular languages. Each snippet demonstrates how to invoke the **Replace Content in Remote Worksheet** operation and handle the response status.

**C# (.NET)**  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new PutReplaceContentRequest(
    name: "sales_report.xlsx",
    worksheet: "Sheet1",
    searchText: "OldValue",
    replaceText: "NewValue",
    folder: "/reports",
    storageName: null);

var response = apiInstance.PutReplaceContent(request);
Console.WriteLine($"Status: {response.Status}, Replaced: {response.ReplacedCount}");
```

**Python**  

```python
from asposecellscloud import CellsApi, PutReplaceContentRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = PutReplaceContentRequest(
    name="sales_report.xlsx",
    worksheet="Sheet1",
    searchText="OldValue",
    replaceText="NewValue",
    folder="/reports"
)

response = api.put_replace_content(request)
print(f"Status: {response.status}, Replaced: {response.replaced_count}")
```

**Java**  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.PutReplaceContentRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
PutReplaceContentRequest request = new PutReplaceContentRequest()
        .name("sales_report.xlsx")
        .worksheet("Sheet1")
        .searchText("OldValue")
        .replaceText("NewValue")
        .folder("/reports");

var response = api.putReplaceContent(request);
System.out.println("Status: " + response.getStatus() + ", Replaced: " + response.getReplacedCount());
```

**Node.js**  

```javascript
const { CellsApi, PutReplaceContentRequest } = require('asposecellscloud');

const api = new CellsApi("client_id", "client_secret");
const request = new PutReplaceContentRequest({
    name: "sales_report.xlsx",
    worksheet: "Sheet1",
    searchText: "OldValue",
    replaceText: "NewValue",
    folder: "/reports"
});

api.putReplaceContent(request).then(response => {
    console.log(`Status: ${response.body.Status}, Replaced: ${response.body.ReplacedCount}`);
});
```

For additional language examples, see the SDK documentation linked above or explore the repository. You can also refer to the related **Replace Content in Remote Range** API for similar operations on cell ranges.