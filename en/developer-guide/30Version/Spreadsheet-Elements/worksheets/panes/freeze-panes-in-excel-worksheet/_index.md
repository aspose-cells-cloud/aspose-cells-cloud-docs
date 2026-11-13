---
title: "Freeze Panes on an Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Freeze"
type: docs
url: /worksheets/panes/freeze/
aliases: [/freeze-panes-in-excel-worksheet/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, Freeze Panes, Excel, REST API, Worksheet"
description: "Freeze rows and columns in an Excel worksheet using Aspose.Cells Cloud REST API with cURL or SDK examples."
weight: 190
ArticleTitle: "Freeze Panes in Excel Worksheet using Aspose.Cells Cloud REST API"
---
The **PutWorksheetFreezePanes** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes`) enables developers to set freeze panes in an Excel worksheet using Aspose.Cells Cloud, specifying the top-left frozen cell via `row` and `column` indices along with the number of visible rows (`freezedRows`) and columns (`freezedColumns`) in the top and left panes, respectively; this supports precise control over worksheet navigation for large datasets without requiring manual Excel interaction.

## The Put Worksheet Freeze Panes Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
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

### Error‑Response

| HTTP Status               | Code | Message                         | Example                                                  |
| ------------------------- | ---- | ------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400  | Invalid parameters              | `{ "Code": 400, "Message": "Invalid frozenRows value" }` |
| 401 Unauthorized          | 401  | Missing or invalid JWT token    | `{ "Code": 401, "Message": "Invalid access token" }`     |
| 404 Not Found             | 404  | Workbook or worksheet not found | `{ "Code": 404, "Message": "File not found" }`           |
| 500 Internal Server Error | 500  | Unexpected server error         | `{ "Code": 500, "Message": "Internal server error" }`    |

The request parameters are:

| Parameter Name | Type    | Location | Description                                         |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name           | string  | path     | The name of the workbook file.                      |
| sheetName      | string  | path     | The name of the worksheet where panes are frozen.   |
| row            | integer | query    | Zero‑based index of the first **unfrozen** row.     |
| column         | integer | query    | Zero‑based index of the first **unfrozen** column.  |
| frozenRows     | integer | query    | Number of rows to freeze starting from the top.     |
| frozenColumns  | integer | query    | Number of columns to freeze starting from the left. |
| folder         | string  | query    | Folder path in storage where the workbook resides.  |
| storageName    | string  | query    | Name of the storage service.                        |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

## How to Use the Put Worksheet Freeze Panes API with SDKs?

### Put Worksheet Freeze Panes API Specification

The <a href="https://reference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes" rel="noopener noreferrer">Put Worksheet Freeze Panes API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFreezePanes.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFreezePanes.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFreezePanes.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFreezePanes.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFreezePanes.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFreezePanes.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFreezePanes.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFreezePanes.go" >}}
{{</tab>}}
{{< /tabs >}}
