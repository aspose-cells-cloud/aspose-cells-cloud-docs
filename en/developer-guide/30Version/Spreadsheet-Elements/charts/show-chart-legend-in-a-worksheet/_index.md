---
title: "Show Chart Legend in a Worksheet"
type: docs
url: /charts/legend/show/
aliases: [/show-chart-legend-in-a-worksheet/]
weight: 100
keywords: "Aspose.Cells Cloud, chart legend API, Excel chart legend, REST PUT chart legend, Aspose API v3.0"
description: "Learn how to display a chart legend in an Excel worksheet using the Aspose.Cells Cloud REST API (v3.0). Includes endpoint details, parameters, a cURL example, and SDK snippets."
---

This REST API enables you to display the **legend**—the explanatory box that identifies data series—in a chart that resides in a worksheet of an Excel workbook.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

The request does **not** require a body; it only needs the parameters listed below.

| Parameter Name | Type    | Location | Description                              |
|----------------|---------|----------|------------------------------------------|
| name           | string  | path     | The workbook filename.                   |
| sheetName      | string  | path     | The worksheet name that contains the chart. |
| chartIndex     | integer | path     | The zero‑based index of the chart.       |
| folder         | string  | query    | The folder that contains the workbook.   |
| storageName    | string  | query    | The name of the storage service.         |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

Authentication is performed with a Bearer JWT token supplied in the **Authorization** header.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make the call with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
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

The API can return the following HTTP status codes:

- **200 OK** – The legend was displayed successfully.  
- **400 Bad Request** – Invalid parameters.  
- **401 Unauthorized** – Authentication failed.  
- **404 Not Found** – The specified workbook, worksheet, or chart does not exist.  
- **500 Internal Server Error** – An unexpected server error occurred.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}