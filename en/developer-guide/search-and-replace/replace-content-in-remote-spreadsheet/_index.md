---
title: "Aspose.Cells Cloud Replace Web API – Update Text in Remote Spreadsheets"
second_title: "Document"
ArticleTitle: "Bulk Text Replacement in Cloud Excel Files – Find & Replace API"
linktitle: "Replace Remote Spreadsheet Content"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, Replace Content, Remote Spreadsheet, Find and Replace API"
description: "Use Aspose.Cells Cloud Find & Replace API to bulk‑update text in remote Excel workbooks. Secure HTTPS endpoint, OAuth2 authentication, and ready‑to‑use SDK examples for fast integration."
weight: 100
---

Perform bulk text replacement across remote Excel files stored in the cloud. Find and update specific text strings efficiently using Aspose.Cells Find & Replace API for cloud spreadsheets.


## Replace Content in Remote Spreadsheet API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

**Example cURL request**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/report.xlsx/replace/content?searchText=OldValue&replaceText=NewValue&folder=/documents/quarterly/" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### Security and Authentication

**Prerequisites:**  
- Obtain a JWT access token as described in the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
- Install the appropriate Aspose.Cells Cloud SDK for your language (e.g., npm package `asposecellscloud`, NuGet `Aspose.Cells-Cloud`, Maven `com.aspose:aspose-cells-cloud`).  

The Aspose.Cells Cloud APIs are secure and require JWT token‑based authentication.

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name  | Type   | Location | Description                                                                                                                                         |
| --------------- | ------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**        | String | Path     | The name of the workbook file stored in cloud storage to be modified (e.g., `"report.xlsx"`).                                                       |
| **searchText**  | String | Query    | The string to locate within the entire workbook. The search is case‑sensitive and applies to all worksheets unless constrained by other parameters. |
| **replaceText** | String | Query    | The string that will replace every occurrence of `searchText`.                                                                                      |
| **folder**      | String | Query    | The cloud storage folder path that contains the source workbook (e.g., `"/documents/quarterly/"`).                                                  |
| **storageName** | String | Query    | _(Optional)_ The name of a custom cloud storage (e.g., `"MyS3Bucket"`). If omitted, the default storage configured for the account is used.         |
| **region**      | String | Query    | _(Optional)_ Locale identifier that may affect character encoding and language‑specific search behavior (e.g., `"en-US"`).                          |
| **password**    | String | Query    | _(Optional)_ Password to open a protected workbook.                                                                                                 |

### Response

A typical successful response returns the status of the operation and the number of replacements performed:

```json
{
  "Code": 200,
  "Status": "OK",
  "ReplacementsCount": 12
}
```

### Error Codes

- **400 Bad Request** – Invalid Aspose.Cells Cloud API URI.  
- **401 Unauthorized** – Missing or invalid OAuth 2.0 access token.  
- **404 Not Found** – The specified spreadsheet file could not be accessed.  
- **500 Server Error** – An unexpected server‑side problem occurred while processing the request.

## When Should You Use the Replace Content in Remote Spreadsheet API?

- **Batch Cloud File Update** – Modify the contents of multiple Excel files stored in cloud storage such as AWS S3 or Azure Blob.  
- **Dynamic Population of Cloud Templates** – Populate report templates stored in the cloud with up‑to‑date data.  
- **Cross‑Region File Synchronization** – Keep Excel files consistent across different geographical storage regions.

## Why Use the Replace Content in Remote Spreadsheet API?

- **Developer‑Friendly** – SDK libraries for many programming languages reduce development effort compared with building a custom solution.  
- **Preserves Formatting, Formulas, and Charts** – All cell formatting, formulas, and charts remain unchanged after text replacement.  
- **Pay‑Per‑Use Model** – You are billed only for the API calls you make, without upfront costs.  
- **Zero Maintenance Overhead** – No servers to manage, no software updates, and no compatibility concerns.

## How to Use the Replace Content in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content in spreadsheets for cells with minimal code.

#### C# Example

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new PutReplaceContentRequest(
    name: "report.xlsx",
    searchText: "OldValue",
    replaceText: "NewValue",
    folder: "/documents/quarterly/",
    storageName: null,
    region: null,
    password: null);

var response = apiInstance.PutReplaceContent(request);
Console.WriteLine($"Replacements made: {response.ReplacementsCount}");
```

#### Python Example

```python
from asposecellscloud import CellsApi, PutReplaceContentRequest

api = CellsApi(client_id="your_client_id", client_secret="your_client_secret")
request = PutReplaceContentRequest(
    name="report.xlsx",
    searchText="OldValue",
    replaceText="NewValue",
    folder="/documents/quarterly/"
)

response = api.put_replace_content(request)
print(f"Replacements made: {response.replacements_count}")
```

For related operations, see the **[Replace Content in Remote Range](/replace-content-in-remote-range/)** API.