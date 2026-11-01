---
title: "Find Text in Excel Files – Aspose.Cells Cloud API"
description: "Search for text in Excel (XLS, XLSX, XLSM, XLSB) and ODS files using Aspose.Cells Cloud API with cURL and SDK examples."
keywords: "Aspose.Cells, Excel, search, API, REST"
type: docs
url: /search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
linktitle: "Search Excel Files"
ArticleTitle: "Find Text in Excel Files with Aspose.Cells Cloud API"
---
The **PostSearch** API (`POST https://api.aspose.cloud/v3.0/cells/search`) enables developers to search for specified text within Excel files (XLS, XLSX, XLSM, XLSB) and OpenDocument Spreadsheet (ODS) files using Aspose.Cells Cloud, supporting optional parameters like worksheet name and file password, and returning all matching cells with their worksheet locations.

## Overview

Aspose.Cells Cloud provides a **POST** endpoint that searches for a given text string inside Excel workbooks (XLS, XLSX, XLSM, XLSB) and OpenDocument Spreadsheet (ODS) files. The API returns every cell that contains the requested text together with a link to the worksheet where the match was found.

> **Use Cases**
>
> - Validate that a particular value exists in a report before further processing.
> - Build a quick “find‑and‑replace” tool that first lists all occurrences.
> - Generate an index of key terms across a batch of spreadsheets.

---

## The Post Search Web API

```http
POST https://api.aspose.cloud/v3.0/cells/search
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| text | String | Query | Find content |
| password | String | Query | The password needed to open an Excel file. |
| sheetname | String | Query | The worksheet name. Locate the specified text content in the worksheet. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |

---

### **Response**

```json
[
  {
    "Name": "IList`1",
    "DataType": {
      "Identifier": "Container",
      "Reference": "TextItem"
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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

| Item            | Value                                                        |
| --------------- | ------------------------------------------------------------ |
| **HTTP Method** | `POST`                                                       |
| **URL**         | `https://api.aspose.cloud/v3.0/cells/search`                 |
| **Purpose**     | Search for specified text within an uploaded Excel workbook. |
| **Security**    | JWT token (Bearer) – see _Prerequisites_ above.              |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

_Replace `<jwt-token>` with a valid token and adjust the query parameters as needed._

---

## Successful Response

**HTTP 200 – Search succeeded; response contains found text items.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Invoice #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      },
      {
        "Text": "Invoice #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sheet1",
          "Rel": "parent",
          "Title": "Sheet1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Response Fields

| Field                    | Type    | Description                                                                                              |
| ------------------------ | ------- | -------------------------------------------------------------------------------------------------------- |
| `Status`                 | string  | Overall request status (`OK` for success).                                                               |
| `Code`                   | integer | HTTP status code (200).                                                                                  |
| `TextItems.link`         | object  | Hypermedia link to the collection resource.                                                              |
| `TextItems.TextItemList` | array   | List of matches. Each item contains:                                                                     |
| `Text`                   | string  | The cell value that matched the search text.                                                             |
| `link`                   | object  | Hyperlink to the worksheet where the match was found (`Href` points to `Workbook/worksheets/SheetName`). |

---

## Error Responses

| HTTP Code | Meaning               | Typical Cause                                                                | Example Body                                                                          |
| --------- | --------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **400**   | Bad Request           | Missing required parameters, unsupported file type, or invalid query values. | `{ "Status":"Error","Code":400,"Message":"The 'text' query parameter is required." }` |
| **401**   | Unauthorized          | Missing or invalid JWT token.                                                | `{ "Status":"Error","Code":401,"Message":"Invalid or expired access token." }`        |
| **413**   | Payload Too Large     | Uploaded file exceeds the 150 MB limit.                                      | `{ "Status":"Error","Code":413,"Message":"File size exceeds the allowed limit." }`    |
| **500**   | Internal Server Error | Unexpected server‑side problem.                                              | `{ "Status":"Error","Code":500,"Message":"An unexpected error occurred." }`           |

---

## SDK Examples

Below are minimal code snippets for the **PostSearch** operation using the official Aspose.Cells Cloud SDKs. Replace `YOUR_JWT_TOKEN` and the file path with your own values.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Invoice",
            sheetname: "Sheet1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Invoice",
                null,          // password
                "Sheet1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Invoice",
        password=None,
        sheetname="Sheet1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
  accessToken: "YOUR_JWT_TOKEN",
  basePath: "https://api.aspose.cloud",
});

const api = new CellsApi(config);

api
  .postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Invoice",
    sheetname: "Sheet1",
    checkExcelRestriction: true,
  })
  .then((response) => {
    response.textItems?.textItemList?.forEach((item) => {
      console.log(`${item.text} -> ${item.link?.href}`);
    });
  })
  .catch((err) => console.error(err));
```

_(SDKs for PHP, Ruby, Go, and Perl are available in the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).)_

---

## Additional Notes

- **`checkExcelRestriction`** defaults to `true`. Set it to `false` only when you are certain the workbook does not contain protected cells that could interfere with the search.
- The API returns **hypermedia links** (`Href`) that can be used with other Aspose.Cells endpoints (e.g., to download the worksheet or retrieve cell formatting).
- When searching large workbooks, consider narrowing the scope with the `sheetname` parameter to improve response time.

---

## Related Links

- **Authentication guide** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **OpenAPI specification for PostSearch** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDKs** – <https://github.com/aspose-cells-cloud>
- **Rate limits & quotas** – <https://docs.aspose.cloud/total/getting-started/limits/>

---
