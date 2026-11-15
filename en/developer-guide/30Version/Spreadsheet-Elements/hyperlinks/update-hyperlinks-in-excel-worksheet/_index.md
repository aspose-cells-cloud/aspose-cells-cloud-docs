---
title: "Update a Hyperlink in an Excel Worksheet – Aspose.Cells Cloud API Guide"
description: "Update Excel hyperlinks via Aspose.Cells Cloud API v3.0 using PostWorksheetHyperlink with cURL or SDKs."
tags:
  - aspose.cells
  - hyperlink
  - excel-api
  - rest-api
  - cloud-spreadsheet
  - v3.0
categories:
  - api-guides
  - cells
  - hyperlinks
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
url: /hyperlinks/update/
type: docs
linktitle: "Update Hyperlink"
ArticleTitle: "Update Excel Hyperlink via Aspose.Cells Cloud REST API v3.0"
keywords: "Aspose.Cells Cloud, update hyperlink, Excel hyperlink API, PostWorksheetHyperlink, REST API v3.0, Excel worksheet hyperlink, cURL example, SDK example, API documentation, hyperlink update example"
---

The **PostWorksheetHyperlink** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}`) enables developers to update an existing hyperlink in a specific worksheet by its zero-based index using Aspose.Cells Cloud’s REST API, supporting precise modification of hyperlink properties such as address, text to display, and screen tip without altering other worksheet content.

## Update a Hyperlink in an Excel Worksheet

**API version:** v3.0

The **PostWorksheetHyperlink** operation updates an existing hyperlink in a worksheet identified by its zero-based index.

## The Post Worksheet Hyperlink Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type            | Path/Query String/HTTPBody | Description                                  |
| -------------- | --------------- | -------------------------- | -------------------------------------------- |
| name           | String          | Path                       | The file name.                               |
| sheetName      | String          | Path                       | The worksheet name.                          |
| hyperlinkIndex | Integer         | Path                       | The hyperlink's index.                       |
| hyperlink      | class:hyperlink | HTTPBody                   | Hyperlink object                             |
| folder         | String          | Query                      | The folder where the file is situated.       |
| storageName    | String          | Query                      | The storage name where the file is situated. |

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

## How to Use the Post Worksheet Hyperlink API with SDKs?

### Post Worksheet Hyperlink API Specification

The <a href="https://reference.aspose.cloud/cells/#/Hypelinks/PostWorksheetHyperlink" rel="noopener noreferrer">Post Worksheet Hyperlink API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

## cURL Example

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC homepage",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Response**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

> _cURL command to update a hyperlink in test.xlsx, highlighting authorization and payload structure._

**Tip:** Save the JSON payload to a file (e.g., `payload.json`) and reference it with `--data @payload.json` for cleaner copy-pasting.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetHyperlink.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetHyperlink.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetHyperlink.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetHyperlink.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetHyperlink.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetHyperlink.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetHyperlink.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetHyperlink.go" >}}
{{</tab>}}
{{< /tabs >}}
