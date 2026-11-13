---
title: "Hide pivot field item in a pivot table"
second_title: "Developer Guide"
linktitle: Hide
type: docs
url: /pivot-tables/hide-pivot-field-item/
aliases: [/hide-pivot-field-item/]
keywords: "Aspose.Cells, hide pivot field item, PivotTable API, REST API, cloud SDK"
description: "Hide pivot field items in Aspose.Cells Cloud via REST API with JWT, cURL, and SDK examples for C# and Go"
weight: 110
ArticleTitle: "Hide Pivot Field Item in a Pivot Table – Aspose.Cells Cloud API Guide"
---
The **PostPivotTableFieldHideItem** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide`) enables hiding a specific pivot field item in a PivotTable via Aspose.Cells Cloud, requiring path parameters for the file name, worksheet name, and PivotTable index, plus query parameters specifying the field type, field index, item index, and hide status, allowing precise control over PivotTable item visibility and supporting recalculating the PivotTable on demand.

This REST API hides a pivot field item in a pivot table.

## The Post Pivot Table Field Hide Item Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| pivotTableIndex | Integer | Path | The PivotTable index. |
| pivotFieldType | String | Query | Represents PivotTable field type(Undefined/Row/Column/Page/Data). |
| fieldIndex | Integer | Query | The pivot field index. |
| itemIndex | Integer | Query | The index of the pivot item in the pivot field. |
| isHide | Boolean | Query | Whether the specific PivotItem is hidden(true/false). |
| needReCalculate | Boolean | Query | Whether the specific PivotTable calculate(true/false). |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

**Quick reference of required query parameters**

- **pivotFieldType** – type of the field (e.g., `Row`).
- **fieldIndex** – zero‑based index of the field to modify.
- **itemIndex** – zero‑based index of the item to hide/show.
- **isHide** – `true` to hide, `false` to show.
- **needReCalculate** – optional, defaults to `false`.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
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

**Response details**


**Note:** If the supplied `fieldIndex` or `itemIndex` is out of range, the API returns a **400 Bad Request** response.

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

## How to Use the Post Pivot Table Field Hide Item API with SDKs?

### Post Pivot Table Field Hide Item API Specification

The <a href="https://reference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem" rel="noopener noreferrer">Post Pivot Table Field Hide Item API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**Note:** The SDK examples assume that you have already configured authentication (JWT token) and that the workbook resides in the specified storage folder. Adjust the `folder` and `storageName` parameters as needed for your environment.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPivotTableFieldHideItem.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPivotTableFieldHideItem.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPivotTableFieldHideItem.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPivotTableFieldHideItem.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPivotTableFieldHideItem.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPivotTableFieldHideItem.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPivotTableFieldHideItem.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPivotTableFieldHideItem.go" >}}
{{</tab>}}
{{< /tabs >}}
