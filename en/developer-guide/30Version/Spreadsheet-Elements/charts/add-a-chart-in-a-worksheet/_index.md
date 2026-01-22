---
title: "Add a Chart in a Worksheet"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "Learn how to add a chart to a worksheet using the Aspose.Cells Cloud REST API, including request parameters, cURL example, and SDK code samples for multiple languages."
keywords: ["Aspose Cells", "add chart", "worksheet", "REST API", "cURL", "SDK", ".NET", "Java", "PHP", "Ruby", "Python", "Node.js", "Go"]
---

This REST API adds a new chart to a worksheet.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

The request parameters are:

| Parameter Name          | Type    | Location                     | Description                                                                 |
|-------------------------|---------|------------------------------|-----------------------------------------------------------------------------|
| **name**                | string  | path                         | Workbook name.                                                              |
| **sheetName**           | string  | path                         | Worksheet name.                                                             |
| **chartType**           | string  | query                        | Chart type (see the **Type** property in the chart resource).              |
| **upperLeftRow**        | integer | query                        | Upper‑left row index of the chart area (0‑based).                           |
| **upperLeftColumn**     | integer | query                        | Upper‑left column index of the chart area (0‑based).                        |
| **lowerRightRow**       | integer | query                        | Lower‑right row index of the chart area (0‑based).                          |
| **lowerRightColumn**    | integer | query                        | Lower‑right column index of the chart area (0‑based).                       |
| **area**                | string  | query                        | Range that provides the values to plot (e.g., `A1:B5`).                     |
| **isVertical**          | boolean | query                        | Indicates whether the chart orientation is vertical.                       |
| **categoryData**        | string  | query                        | Range of category‑axis values (e.g., `D1:E10`).                             |
| **isAutoGetSerialName**| boolean | query                        | Automatically generate series names if `true`.                            |
| **title**               | string  | query                        | Title of the chart.                                                         |
| **folder**              | string  | query                        | Folder that contains the workbook.                                          |
| **storageName**         | string  | query                        | Name of the storage.                                                        |
| **dataLabels**          | boolean | query                        | Show data labels when `true`.                                               |
| **dataLabelsPosition**  | string  | query                        | Position of data labels (e.g., `Above`).                                    |
| **pivotTableSheet**     | string  | query                        | Name of the sheet that contains the pivot table.                            |
| **pivotTableName**      | string  | query                        | Name of the pivot table.                                                    |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

## Cloud SDK Family

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