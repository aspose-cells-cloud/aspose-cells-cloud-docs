---
title: "Hide Chart Legend in an Excel Worksheet – Aspose.Cells Cloud API"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, hide chart legend, REST API, Cloud SDK, chart legend"
description: "Learn how to hide a chart legend in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes HTTPS endpoint, required authentication, request syntax, response details, error handling, and SDK examples."
linktitle: "Hide Chart Legend"
ArticleTitle: "Hide Chart Legend in Excel Worksheet via Aspose.Cells Cloud REST API"
---
The **DeleteWorksheetChartLegend** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend`) hides the chart legend in a worksheet, removing the box that identifies the data series plotted in the chart. Aspose.Cells Cloud enables this operation via a RESTful endpoint, supporting programmatic legend management without manual editing. Developers can integrate this functionality using SDKs for .NET, Java, Go, Node.js, Python, and other languages, streamlining dynamic chart customization in cloud-based spreadsheet workflows.

The API requires a valid Aspose Cloud JWT token, the workbook must be uploaded to Aspose Cloud storage, and the API version used is **v3.0**.

## The Delete Worksheet Chart Legend Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| chartIndex | Integer | Path | The chart index. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

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

## How to Use the Delete Worksheet Chart Legend API with SDKs?

### Delete Worksheet Chart Legend API Specification

The <a href="https://reference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend" rel="noopener noreferrer">Delete Worksheet Chart Legend API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetChartLegend.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetChartLegend.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetChartLegend.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetChartLegend.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetChartLegend.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetChartLegend.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetChartLegend.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetChartLegend.go" >}}
{{</tab>}}
{{< /tabs >}}
