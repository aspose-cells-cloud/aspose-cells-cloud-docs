---
title: "Aspose.Cells Cloud Excel Text Search Web API – Find Text in Remote Worksheet"
second_title: "Document"
ArticleTitle: "Search Text in Remote Excel Spreadsheet Worksheet – Find Specific Data"
linktitle: "Search Remote Worksheet Content"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Aspose Cells, Excel API, text search, remote worksheet"
description: "Search for text, numbers, or formulas in a remote Excel worksheet using Aspose.Cells Cloud API. Supports case‑insensitive and password‑protected files."
weight: 100
---

## **Search Content in Remote Worksheet**

Programmatically search for specific text within any Excel worksheet using the Aspose.Cells Cloud API. The service can locate text, numbers, or formulas in remote files stored in cloud storage, enabling automated data‑discovery, content‑analysis, and spreadsheet‑auditing workflows.

**API version:** This page documents **v4.0** of the API. A newer v5.x version is available; see the changelog for additional parameters.

### **Web API**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Request Parameters**

| Parameter Name | Type    | Path/Query String/HTTP Body | Description                                                                                       |
| -------------- | ------- | --------------------------- | ------------------------------------------------------------------------------------------------- |
| name           | String  | Path                        | **Required.** The filename of the target workbook (e.g., `annual_report.xlsx`).                   |
| worksheet      | String  | Path                        | **Required.** The worksheet within the workbook where the search is performed.                    |
| searchText     | String  | Query                       | **Required.** The exact text string or number to locate.                                          |
| ignoreCase     | Boolean | Query                       | **Optional.** When `true`, the search is case‑insensitive. Default is `false`.                    |
| folder         | String  | Query                       | **Optional.** Path to the folder containing the workbook. If omitted, the root folder is used.    |
| storageName    | String  | Query                       | **Optional.** Name of a custom‑configured cloud storage. If omitted, the default storage is used. |
| region         | String  | Query                       | **Optional.** Locale setting (e.g., `ja-JP`) that may affect text comparison.                     |
| password       | String  | Query                       | **Optional.** Password for a protected workbook. Omit if the file is not encrypted.               |

### **Response**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Array of matches. Each item contains the cell address (`cellName`), the matched string (`text`), and how many times it appears in that cell (`occurrences`).
- **code** – HTTP status code returned by the service.
- **status** – Textual description of the result.

### **Error Codes**

- **400 Bad Request** – Invalid API URI or malformed parameters.
- **401 Unauthorized** – Missing or invalid OAuth 2.0 token.
- **404 Not Found** – The workbook or worksheet cannot be located.
- **500 Server Error** – An unexpected condition occurred while processing the request.

## Where should we use the Search content within the worksheet of the Spreadsheet API?

- **Workbook compliance audit:** Quickly locate sensitive terms (e.g., “Confidential”) across the entire file.
- **Cross‑sheet data association:** Find a project number or customer name that appears on multiple sheets.
- **Template verification:** After generating reports, confirm that placeholders such as `{{Date}}` have been replaced.
- **Historical data mining:** Search for specific event codes in legacy spreadsheets to understand past business logic.

## Why should you use the Search content within the worksheet of the Spreadsheet API?

- **Developer‑friendly:** SDKs for many languages accelerate development and are fully documented.
- **Reduced labor costs:** Decreases the need for staff dedicated to manual data consolidation.
- **Pay‑per‑use:** You only pay for the API calls you actually make.
- **Zero maintenance:** No servers to manage, no software updates, and no compatibility concerns.
- **Preserves complex Excel formatting** when exporting results to PDF or other formats.

## How to Use the Search for broken links within the worksheet of the Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) defines a publicly accessible programming interface and enables REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement search content within worksheet of spreadsheets for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

**Prerequisites**  
Before running the examples, ensure you have:

1. An Aspose Cloud **client ID** and **client secret**.  
2. Generated an OAuth 2.0 **access token** (see the authentication guide).  
3. The target workbook uploaded to your chosen storage location.  

**C# Example**

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.Collections.Generic;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET",
            BaseUrl = "https://api.aspose.cloud"
        };
        var api = new CellsApi(config);

        // Build request parameters
        var name = "sample.xlsx";
        var worksheet = "Sheet1";
        var searchText = "Total";
        var ignoreCase = true;

        // Execute search
        var response = api.SearchContentInRemoteWorksheet(
            name, worksheet, searchText, ignoreCase: ignoreCase);

        // Process results
        foreach (var item in response.TextItems)
        {
            Console.WriteLine($"{item.CellName}: \"{item.Text}\" (Occurrences: {item.Occurrences})");
        }
    }
}
```

**Java Example**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.SearchResponse;
import com.aspose.cells.cloud.Configuration;

public class SearchExample {
    public static void main(String[] args) {
        Configuration config = new Configuration();
        config.setClientId("YOUR_CLIENT_ID");
        config.setClientSecret("YOUR_CLIENT_SECRET");

        CellsApi api = new CellsApi(config);

        String name = "sample.xlsx";
        String worksheet = "Sheet1";
        String searchText = "Total";
        Boolean ignoreCase = true;

        SearchResponse result = api.searchContentInRemoteWorksheet(
            name, worksheet, searchText, null, null, null, null, null, ignoreCase, null, null);

        result.getTextItems().forEach(item ->
            System.out.println(item.getCellName() + ": \"" + item.getText() +
                               "\" (Occurrences: " + item.getOccurrences() + ")"));
    }
}
```

**Python Example**

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk.apis.cells_api import CellsApi
from asposecellscloudsdk.models import *

# Configure client
api_client = asposecellscloudsdk.ApiClient()
api_client.configuration.client_id = "YOUR_CLIENT_ID"
api_client.configuration.client_secret = "YOUR_CLIENT_SECRET"

cells_api = CellsApi(api_client)

# Parameters
name = "sample.xlsx"
worksheet = "Sheet1"
search_text = "Total"
ignore_case = True

try:
    response = cells_api.search_content_in_remote_worksheet(
        name=name,
        worksheet=worksheet,
        search_text=search_text,
        ignore_case=ignore_case
    )
    for item in response.text_items:
        print(f"{item.cell_name}: \"{item.text}\" (Occurrences: {item.occurrences})")
except ApiException as e:
    print("Exception when calling CellsApi->search_content_in_remote_worksheet:", e)
```

**Node.js Example**

```javascript
const { CellsApi, Configuration } = require('asposecellscloudsdk');

const config = new Configuration();
config.clientId = 'YOUR_CLIENT_ID';
config.clientSecret = 'YOUR_CLIENT_SECRET';

const cellsApi = new CellsApi(config);

const name = 'sample.xlsx';
const worksheet = 'Sheet1';
const searchText = 'Total';
const ignoreCase = true;

cellsApi.searchContentInRemoteWorksheet(name, worksheet, searchText, null, null, null, null, null, ignoreCase, null, null)
  .then(response => {
    response.textItems.forEach(item => {
      console.log(`${item.cellName}: "${item.text}" (Occurrences: ${item.occurrences})`);
    });
  })
  .catch(err => {
    console.error('Error:', err);
  });
```

**Notes**  
- When searching password‑protected workbooks, include the `password` query parameter.  
- The `ignoreCase` flag defaults to `false`; set it to `true` for case‑insensitive searches.  
- Large worksheets may return many matches; consider paging or filtering on the client side if performance becomes an issue.