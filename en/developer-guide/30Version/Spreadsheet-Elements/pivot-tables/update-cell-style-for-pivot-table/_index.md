---
title: "Update Cell Style for Pivot Table"
second_title: "Developer Guide"
linktitle: Format
type: docs
url: /pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: "Aspose.Cells Cloud, pivot table style, update cell style API, REST API, Excel API, spreadsheet formatting, cloud SDK, cell style, pivot table"
description: "Format pivot table cell styles via Aspose.Cells Cloud REST API using PostPivotTableCellStyle with JWT authentication"
weight: 90
ArticleTitle: "Update Cell Style for Pivot Table - Aspose.Cells Cloud API Documentation"
---
The **PostPivotTableCellStyle** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format`) enables Aspose.Cells Cloud users to update the cell style of a specific cell within a pivot table by specifying the file name, worksheet name, pivot table index, and the zero-based row and column indices of the target cell, along with a style object in the request body; this operation supports precise formatting control for pivot table elements without requiring local file manipulation.

## The Post Pivot Table Cell Style Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name  | Type        | Path/Query String/HTTPBody | Description                                            |
| --------------- | ----------- | -------------------------- | ------------------------------------------------------ |
| name            | String      | Path                       | The file name.                                         |
| sheetName       | String      | Path                       | The worksheet name.                                    |
| pivotTableIndex | Integer     | Path                       | The PivotTable index.                                  |
| column          | Integer     | Query                      | The column index of the cell.                          |
| row             | Integer     | Query                      | The row index of the cell.                             |
| style           | class:style | HTTPBody                   | Style Style description in request body.               |
| needReCalculate | Boolean     | Query                      | Whether the specific PivotTable calculate(true/false). |
| folder          | String      | Query                      | The folder where the file is situated.                 |
| storageName     | String      | Query                      | The storage name where the file is situated.           |

The <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Response**  
On success the service returns HTTP 200 with an empty body indicating that the style has been applied. In case of an error, a JSON payload with an error code and message is returned.

| HTTP Status | Description                                                               |
| ----------- | ------------------------------------------------------------------------- |
| 200         | Style applied successfully.                                               |
| 400         | Bad request – e.g., invalid column/row index.                             |
| 401         | Unauthorized – missing or invalid JWT token.                              |
| 404         | Not found – specified document, worksheet, or pivot table does not exist. |
| 500         | Internal server error – unexpected condition.                             |

The response body is empty on success.

For more information, see the **Get Pivot Table** API documentation.

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
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Post Pivot Table Cell Style API with SDKs?

### Post Pivot Table Cell Style API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" rel="noopener noreferrer">Post Pivot Table Cell Style API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

The following code example demonstrates how to call Aspose.Cells web services using the **Go** SDK:

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Update Cell Style for Pivot Table",
  "description": "Guide to updating the style of a specific cell in an Aspose.Cells Cloud pivot table using the REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, pivot table, cell style, REST API, Go SDK",
  "url": "https://docs.aspose.cloud/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPivotTableCellStyle.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPivotTableCellStyle.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPivotTableCellStyle.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPivotTableCellStyle.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPivotTableCellStyle.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPivotTableCellStyle.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPivotTableCellStyle.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPivotTableCellStyle.go" >}}
{{</tab>}}
{{< /tabs >}}
