---
title: "Unfreeze Panes on an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Unfreeze"
type: docs
url: /worksheets/panes/unfreeze/
aliases:
  - /unfreeze-panes-in-excel-worksheet/
  - /worksheets/unfreeze-panes/
keywords: "unfreeze panes, Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Python, Node.js, Go, Swift, Android, Ruby, Perl"
description: "Unfreeze Excel worksheet panes via Aspose.Cells Cloud API: DELETE /cells/{name}/worksheets/{sheetName}/freezepanes"
weight: 1000
ArticleTitle: "Unfreeze Panes in Excel Worksheet using Aspose.Cells Cloud REST API"
---
The **DeleteWorksheetFreezePanes** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes`) unfreezes panes in an Excel worksheet by removing previously frozen rows and columns, enabling dynamic reconfiguration of scrollable view regions; Aspose.Cells Cloud supports this operation with required parameters including `row`, `column`, `freezedRows`, and `freezedColumns` to precisely define the pane boundary being unfrozen.

## The Delete Worksheet Freeze Panes Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| row | Integer | Query | Row index. |
| column | Integer | Query | Column index. |
| freezedRows | Integer | Query | Number of visible rows in top pane, no more than row index. |
| freezedColumns | Integer | Query | Number of visible columns in left pane, no more than column index. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

_No additional query parameters (such as row, column, frozenRows, or frozenColumns) are required for the unfreeze operation._

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetFreezePanes) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes" \
-X DELETE \
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

## How to Use the Delete Worksheet Freeze Panes API with SDKs?

### Delete Worksheet Freeze Panes API Specification

The <a href="https://reference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetFreezePanes" rel="noopener noreferrer">Delete Worksheet Freeze Panes API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFreezePanes.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFreezePanes.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFreezePanes.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFreezePanes.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFreezePanes.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFreezePanes.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFreezePanes.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFreezePanes.go" >}}
{{</tab>}}
{{< /tabs >}}
