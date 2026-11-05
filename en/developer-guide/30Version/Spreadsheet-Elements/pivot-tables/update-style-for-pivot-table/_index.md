---
title: "Update style for pivot table"
second_title: "Developer Guide"
linktitle: "Format all"
type: docs
url: /pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: "pivot table, update style, Aspose.Cells Cloud, REST API, Excel, spreadsheet, API, pivot table style, format all"
description: "Update pivot table style via Aspose.Cells Cloud REST API using PostPivotTableStyle endpoint with cURL and SDK examples."
weight: 100
ArticleTitle: "Update style for pivot table - Aspose.Cells Cloud API"
---
The **PostPivotTableStyle** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll`) enables developers to update the style of a specific pivot table within a worksheet using Aspose.Cells Cloud, allowing programmatic application of formatting such as cell borders, fonts, and colors to all cells in the pivot table structure in a single request.

## The Post Pivot Table Style Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request parameters**

| Parameter Name  | Type        | Path/Query String/HTTPBody | Description                                            |
| --------------- | ----------- | -------------------------- | ------------------------------------------------------ |
| name            | String      | Path                       | The file name.                                         |
| sheetName       | String      | Path                       | The worksheet name.                                    |
| pivotTableIndex | Integer     | Path                       | The PivotTable index.                                  |
| style           | class:style | HTTPBody                   | StyleStyle description in request body.                |
| needReCalculate | Boolean     | Query                      | Whether the specific PivotTable calculate(true/false). |
| folder          | String      | Query                      | The folder where the file is situated.                 |
| storageName     | String      | Query                      | The storage name where the file is situated.           |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
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

### **Response**

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

**Prerequisites / Authentication**  
A valid JWT access token must be supplied in the `Authorization` header (e.g., `Bearer <jwt token>`). Ensure the token has permission to access the specified workbook and worksheet.

## How to Use the Post Pivot Table Style API with SDKs?

### Post Pivot Table Style API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle" rel="noopener noreferrer">Post Pivot Table Style API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

The following code example demonstrates how to call the API using the Go SDK:

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPivotTableStyle.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPivotTableStyle.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPivotTableStyle.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPivotTableStyle.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPivotTableStyle.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPivotTableStyle.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPivotTableStyle.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPivotTableStyle.go" >}}
{{</tab>}}
{{< /tabs >}}
