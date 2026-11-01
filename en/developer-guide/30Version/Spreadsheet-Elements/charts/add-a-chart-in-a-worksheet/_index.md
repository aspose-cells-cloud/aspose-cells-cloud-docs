---
title: "Add a Chart to a Worksheet"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 100
description: "Use Aspose.Cells Cloud REST API to add a chart to an Excel worksheet via PUT /charts endpoint with cURL or SDKs."
keywords:
  - "add chart Aspose.Cells"
  - "Aspose.Cells add chart API"
  - "chart API REST"
  - "Aspose.Cells SDK examples"
ArticleTitle: "Add a Chart to a Worksheet – Aspose.Cells Cloud API Guide"
linktitle: "Add Chart to Worksheet"
---
The **PutWorksheetChart** API (`PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts`) adds a new chart to a specified worksheet in an Aspose.Cells Cloud workbook, supporting parameters like chart type, position bounds, data range, axis settings, and title; it enables developers to programmatically generate charts—including pivot charts—by specifying source data ranges and display options through a REST interface.

## The Put Worksheet Chart Web API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| chartType | String | Query | Chart type, please refer property Type in chart resource. |
| upperLeftRow | Integer | Query | Upper-left row for the new chart. |
| upperLeftColumn | Integer | Query | Upper-left column for the new chart. |
| lowerRightRow | Integer | Query | Lower-left row for the new chart. |
| lowerRightColumn | Integer | Query | Lower-left column for the new chart. |
| area | String | Query | Specify the values from which to plot the data series. |
| isVertical | Boolean | Query | Specify whether to plot the series from a range of cell values by row or by column. |
| categoryData | String | Query | Get or set the range of category axis values. It can be a range of cells (e.g., "D1:E10"). |
| isAutoGetSerialName | Boolean | Query | Specify whether to auto-update the serial name. |
| title | String | Query | Specify the chart title name. |
| folder | String | Query | The folder where the file is situated. |
| dataLabels | Boolean | Query | Represents the specified chart's data label values display behavior. True to display the values, False to hide them. |
| dataLabelsPosition | String | Query | Represents data label position (Center/InsideBase/InsideEnd/OutsideEnd/Above/Below/Left/Right/BestFit/Moved). |
| pivotTableSheet | String | Query | The source is the data of the pivotTable. If PivotSource is not empty, the chart is a PivotChart. |
| pivotTableName | String | Query | The pivot table name. |
| storageName | String | Query | The storage name where the file is situated. |

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

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the PutWorksheetAddChart API with SDKs

### PutWorksheetAddChart API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# No request body is required for this operation
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK abstracts low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}
