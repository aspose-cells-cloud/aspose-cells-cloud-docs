---
title: "Clear Contents and Styles of Cells in an Excel Worksheet"
type: docs
url: /clear-contents-and-styles-of-cells-in-excel-worksheet/
date: 2023-07-08
description: "Learn how to clear cell contents and styles in Excel worksheets using Aspose.Cells Cloud REST API, with cURL and SDK examples."
keywords:
  - aspose.cells
  - excel api
  - clear cell contents
  - clear cell styles
  - cloud spreadsheet
  - rest api
weight: 50
canonical: https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/
ArticleTitle: "Clear Contents and Styles of Cells in an Excel Worksheet – Aspose.Cells Cloud API"
linktitle: "Clear Cell Contents"
---
The **PostClearContents** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents`) enables developers to clear cell contents and styles within a specified worksheet of an Excel file using Aspose.Cells Cloud, supporting optional range-based clearing via query parameters like `range`, `startRow`, `startColumn`, `endRow`, and `endColumn` to target specific cell areas precisely.

## Clear Contents and Styles of Cells in an Excel Worksheet

Aspose.Cells Cloud provides robust support for clearing cell area contents in a worksheet—a process commonly required for data preparation, template resets, and dynamic report generation.

The REST API supports flexible clearing options via query parameters:
- **Range-based clearing** (`range`): Clear a named or A1-style range (e.g., `"A2:C11"`).
- **Grid-based clearing**: Use `startRow`, `startColumn`, `endRow`, and `endColumn` to specify a rectangular region by index.
- **Optional context**: Specify `folder` and `storageName` to locate the file.

> **Note**: This endpoint clears **cell contents only**. To clear styles, use the `PostClearStyles` endpoint (see [Clear Styles of Cells](/clear-styles-of-cells-in-excel-worksheet/)).

## The Post Clear Contents Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents
```

### Security and Authentication

The Aspose.Cells Cloud APIs require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). All requests must include a valid bearer token in the `Authorization` header.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| range | String | Query | Represents the range to which the specified cells applies. |
| startRow | Integer | Query | The start row index. |
| startColumn | Integer | Query | The start column index. |
| endRow | Integer | Query | The end row index. |
| endColumn | Integer | Query | The end column index. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

> **Tip**: Either `range` or the grid parameters (`startRow`, `startColumn`, `endRow`, `endColumn`) must be provided. Using both simultaneously may result in undefined behavior.

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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

On success, the API returns a `200 OK` status with the following payload:


#### HTTP Status Codes

### Using the PostClearContents API

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/clearcontents?range=A2:C11" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is recommended to streamline integration and reduce boilerplate code. The Aspose.Cells Cloud SDKs handle authentication, request/response serialization, and error handling automatically.

Please refer to the [GitHub repository](https://github.com/aspose-cells-cloud) for the full list of supported SDKs and installation instructions.

The following code examples demonstrate how to clear cell contents using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearContents.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearContents.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearContents.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearContents.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearContents.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearContents.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearContents.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearContents.go" >}}

{{< /tab >}}

{{< /tabs >}}

## API Reference

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents) defines the publicly accessible programming interface for this operation.

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Clear Contents and Styles of Cells in an Excel Worksheet",
  "description": "How to use Aspose.Cells Cloud REST API to clear cell contents and styles in an Excel worksheet.",
  "url": "https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/",
  "datePublished": "2023-07-08",
  "dateModified": "2023-07-08",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://docs.aspose.cloud/cells/images/Aspose-image-for-open-graph.jpg",
      "caption": "Aspose.Cells Cloud logo",
      "alt": "Aspose.Cells Cloud logo"
    }
  },
  "keywords": "Aspose.Cells, Excel API, clear cell contents, clear cell styles, REST API, cloud spreadsheet"
}
</script>