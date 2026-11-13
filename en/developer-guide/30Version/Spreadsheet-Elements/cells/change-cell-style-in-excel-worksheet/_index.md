---
title: "Change Cell Style in Excel Worksheet – Aspose.Cells Cloud API Guide"
type: docs
url: /change-cell-style-in-excel-worksheet/
weight: 30
api_version: "v3.0"
keywords:
  - Aspose.Cells
  - Aspose.Cells Cloud
  - Excel
  - Cell Style
  - REST API
  - Cloud SDK
  - cURL
  - cell style update
  - Excel API
description: "Change Excel cell style using Aspose.Cells Cloud API with cURL or SDKs (C#, Java, Python) and authentication examples"
tags:
  - cell-style
  - excel-api
  - rest
  - cloud
  - aspose.cells
categories:
  - cells
  - api-reference
article_title: "Change Cell Style in Excel Worksheet – Aspose.Cells Cloud API Guide"
linktitle: "Update Cell Style"
ArticleTitle: "Update Excel Cell Style with Aspose.Cells Cloud REST API"
---
The **PostUpdateWorksheetCellStyle** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style`) enables developers to update the style of a specific cell in an Excel worksheet by specifying the workbook name, worksheet name, and cell name, with the style configuration sent in the request body; Aspose.Cells Cloud supports this operation via REST API and SDKs for .NET, Java, Python, Node.js, Go, and other languages, allowing precise, programmatic control over cell formatting without altering other worksheet content.

## The Post Update Worksheet Cell Style Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```http
Authorization: Bearer {access_token}
```

### Request Parameters

| Parameter Name | Type        | Path/Query String/HTTPBody | Description                                  |
| -------------- | ----------- | -------------------------- | -------------------------------------------- |
| name           | String      | Path                       | The file name.                               |
| sheetName      | String      | Path                       | The worksheet name.                          |
| cellName       | String      | Path                       | The cell name.                               |
| style          | class:style | HTTPBody                   | Style with update style settings.            |
| folder         | String      | Query                      | The folder where the file is situated.       |
| storageName    | String      | Query                      | The storage name where the file is situated. |

### Example Response

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

The `PostUpdateWorksheetCellStyle` API endpoint allows you to update the style of a single cell. Here’s how to use it with `cURL`.

### Example Request: Apply Background Theme Color

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer ${JWT_TOKEN}" \
  -d '{
    "BackgroundThemeColor": {
      "ColorType": "Text2",
      "Tint": 0.2
    }
  }'
```

### HTTP Status Codes

| Code  | Meaning               | Description                                                  |
| ----- | --------------------- | ------------------------------------------------------------ |
| `200` | OK                    | Style updated successfully.                                  |
| `400` | Bad Request           | Invalid cell name, malformed JSON, or unsupported file type. |
| `401` | Unauthorized          | Invalid or missing JWT token.                                |
| `413` | Payload Too Large     | Request body exceeds 50 MB limit.                            |
| `500` | Internal Server Error | Unexpected server error.                                     |

> **Note**: The `Style` object in the response reflects the _current_ state after applying the update.

## How to Use the Post Update Worksheet Cell Style API with SDKs?

### Post Update Worksheet Cell Style API Specification

The <a href="https://reference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetCellStyle" rel="noopener noreferrer">Post Update Worksheet Cell Style API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

SDKs abstract low-level HTTP details and simplify integration. All official SDKs are open-source on [GitHub](https://github.com/aspose-cells-cloud).

### Available SDKs

- [C# (.NET)](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)
- [Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java)
- [PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php)
- [Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python)
- [Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node)
- [Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby)
- [Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl)
- [Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go)

### Code Examples

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetCellStyle.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetCellStyle.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetCellStyle.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetCellStyle.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetCellStyle.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetCellStyle.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetCellStyle.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetCellStyle.go" >}}
{{</tab>}}
{{< /tabs >}}
