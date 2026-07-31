---
title: "Aspose.Cells Cloud API – Set Chart Title in an Excel Worksheet"
type: docs
url: /chart/title/add/
aliases: [/set-chart-title-in-excel-worksheet/]
weight: 30
keywords: "Aspose.Cells Cloud, chart title API, Excel chart title, REST API, SDK examples"
description: "Learn how to add or update a chart title in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes cURL, SDK samples, required parameters, authentication steps, and error handling."
---

Adds a chart title or makes an existing title visible.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### Request parameters

| Parameter Name | Type    | Location | Description                        |
| -------------- | ------- | -------- | ---------------------------------- |
| name           | string  | path     | Workbook name.                     |
| sheetName      | string  | path     | Worksheet name.                    |
| chartIndex     | integer | path     | Index of the chart.                |
| title          | string  | body     | Text of the chart title.           |
| folder         | string  | query    | Folder that contains the workbook. |
| storageName    | string  | query    | Name of the storage.               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
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

**Error Responses**

| HTTP Code | Example Payload                                                                        | Description                                               |
| --------- | -------------------------------------------------------------------------------------- | --------------------------------------------------------- |
| 400       | `{ "Code": "400", "Message": "Invalid request payload." }`                             | The request body is malformed or missing required fields. |
| 401       | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }` | The bearer token is missing, invalid, or expired.         |
| 404       | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`             | The specified resource does not exist.                    |
| 500       | `{ "Code": "500", "Message": "Internal server error." }`                               | An unexpected error occurred on the server.               |

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}
