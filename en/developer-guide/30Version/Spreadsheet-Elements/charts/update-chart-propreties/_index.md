---
title: "Update Chart Properties"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, chart properties, update chart, Excel API, REST API, cURL, SDK, C#, Java, PHP, Ruby, Node.js, Go, Perl"
description: "Learn how to update chart properties (type, title, legend, etc.) in an Excel workbook using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL example, and SDK snippets for C#, Java, PHP, Ruby, Node.js, Perl, and Go."
---

This REST API updates chart properties.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Request parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                                   |
| -------------- | ------- | -------------------------- | ------------------------------------------------------------- |
| name           | string  | path                       | The name of the Excel file.                                   |
| sheetName      | string  | path                       | The name of the worksheet containing the chart.               |
| chartIndex     | integer | path                       | Zero-based index of the chart to be updated.                  |
| chart          | object  | body                       | JSON object that defines the chart properties to be modified. |
| folder         | string  | query                      | The folder in storage where the file is located.              |
| storageName    | string  | query                      | The name of the storage service.                              |

### Request Body Schema

The **`chart`** object contains the properties you can modify. Below is a representative JSON example that includes several commonly used fields:

```json
{
  "Title": {
    "Text": "Quarterly Sales"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Note:** Only the fields you need to change have to be supplied. Omitted properties retain their existing values.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

## Response

The API returns a JSON object indicating the operation result. A successful update yields:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Possible error responses include:

| HTTP Status | Description                                     |
| ----------- | ----------------------------------------------- |
| 400         | Bad Request – invalid parameters or body        |
| 401         | Unauthorized – missing or invalid token         |
| 404         | Not Found – file, worksheet, or chart not found |
| 500         | Internal Server Error                           |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}
