---
title: "Hide Chart Legend in an Excel Worksheet – Aspose.Cells Cloud API"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, hide chart legend, REST API, Cloud SDK, chart legend"
description: "Learn how to hide a chart legend in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes HTTPS endpoint, required authentication, request syntax, response details, error handling, and SDK examples."
---

This REST API hides the legend in a chart. A **chart legend** is the box that identifies the data series plotted in the chart.

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Request parameters

| Parameter Name  | Type    | Location | Description                 |
| --------------- | ------- | -------- | --------------------------- |
| **name**        | string  | path     | Workbook name.              |
| **sheetName**   | string  | path     | Worksheet name.             |
| **chartIndex**  | integer | path     | Index of the chart.         |
| **folder**      | string  | query    | Workbook folder (optional). |
| **storageName** | string  | query    | Storage name (optional).    |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) defines this publicly accessible programming interface.

You can use the cURL command‑line tool to call the API easily. The example below demonstrates a request that hides the legend of chart 0 in _Sample_Test_Book.xls_.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
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

## Responses

| HTTP Status                   | Description                                   | Example JSON                                                  |
| ----------------------------- | --------------------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | Legend hidden successfully.                   | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | Missing or invalid JWT token.                 | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | Workbook, worksheet, or chart does not exist. | `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | Unexpected server error.                      | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## FAQ

**Q:** _How do I hide a chart legend using Aspose.Cells Cloud?_  
**A:** Send a `DELETE` request to `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` with a valid JWT token in the `Authorization` header. A `200 OK` response indicates success.

**Q:** _What authentication is required for the Hide Chart Legend API?_  
**A:** Include an `Authorization: Bearer <jwt token>` header. Obtain the token via the Aspose Cloud OAuth flow.

**Q:** _What error response will I receive if the chart index is invalid?_  
**A:** The service returns `404 Not Found` with a JSON body containing `Code: 404` and a message describing the missing chart.

**Q:** _Can I use HTTP instead of HTTPS?_  
**A:** No. All Aspose Cloud endpoints require HTTPS for security.

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project tasks. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**Coming soon** – Swift SDK example will be added shortly.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Hide Chart Legend in an Excel Worksheet – Aspose.Cells Cloud API",
  "description": "Step‑by‑step guide to hide a chart legend in an Excel worksheet using Aspose.Cells Cloud REST API. Includes HTTPS endpoint, authentication, request syntax, response details, error handling, and SDK examples.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Charts", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Hide Chart Legend", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Hide chart legend using Aspose.Cells Cloud API"
}
</script>
