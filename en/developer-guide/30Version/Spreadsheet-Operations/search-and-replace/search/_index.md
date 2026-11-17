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

The **PostSearch** API (`POST https://api.aspose.cloud/v3.0/cells/search`) lets developers search Excel workbooks (XLS, XLSX, XLSM, XLSB) and OpenDocument Spreadsheets (ODS) for a specified text string via Aspose.Cells Cloud, with optional parameters such as worksheet name and file password; it returns every matching cell along with a link to the worksheet where the match was found, making it useful for validating that a value exists in a report before further processing, building a quick find-and-replace tool that first lists all occurrences, or generating an index of key terms across a batch of spreadsheets.

## The Post Search Web API

```http
POST https://api.aspose.cloud/v3.0/cells/search
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name        | Type    | Path/Query String/HTTPBody | Description                                                                     |
| --------------------- | ------- | -------------------------- | ------------------------------------------------------------------------------- |
| File                  | File    | FormData                   | File to upload                                                                  |
| text                  | String  | Query                      | Find content                                                                    |
| password              | String  | Query                      | The password needed to open an Excel file.                                      |
| sheetname             | String  | Query                      | The worksheet name. Locate the specified text content in the worksheet.         |
| checkExcelRestriction | Boolean | Query                      | Whether check restriction of excel file when user modify cells related objects. |

### Response

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

### Response Fields

| Field                    | Type    | Description                                                                                              |
| ------------------------ | ------- | -------------------------------------------------------------------------------------------------------- |
| `Status`                 | string  | Overall request status (`OK` for success).                                                               |
| `Code`                   | integer | HTTP status code (200).                                                                                  |
| `TextItems.link`         | object  | Hypermedia link to the collection resource.                                                              |
| `TextItems.TextItemList` | array   | List of matches. Each item contains:                                                                     |
| `Text`                   | string  | The cell value that matched the search text.                                                             |
| `link`                   | object  | Hyperlink to the worksheet where the match was found (`Href` points to `Workbook/worksheets/SheetName`). |

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
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Post Search API with SDKs?

### Post Search API Specification

The <a href="https://reference.aspose.cloud/cells/#/LightCells/PostSearch" rel="noopener noreferrer">Post Search API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**Request Example (cURL)**

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Invoice&sheetname=Sheet1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

_Replace `<jwt-token>` with a valid token and adjust the query parameters as needed._

**Successful Response**

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

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSearch.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSearch.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSearch.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSearch.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSearch.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSearch.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSearch.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSearch.go" >}}
{{</tab>}}
{{< /tabs >}}
