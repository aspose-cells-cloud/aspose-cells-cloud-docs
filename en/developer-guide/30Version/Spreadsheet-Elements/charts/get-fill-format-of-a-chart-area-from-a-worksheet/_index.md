---
title: "Get Chart Area Fill Format – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /charts/chart-area/fill-format/get/
aliases: [/get-fill-format-of-a-chart-area-from-a-worksheet/]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Chart Area"
  - "Fill Format"
  - "REST API"
  - "Excel"
description: "Retrieve the fill format (color, pattern, gradient) of a chart area in an Excel worksheet via Aspose.Cells Cloud API. Includes cURL example, SDK code snippets, authentication steps, and response details."
ArticleTitle: "Get Chart Area Fill Format Aspose.Cells Cloud API v3.0"
---

This REST API retrieves the fill‑format information of a **Chart Area**.

**Prerequisites**  
To call this endpoint you must have a valid OAuth/JWT access token. Obtain the token using the Aspose.Cells Cloud authentication flow and include it in the `Authorization` header as `Bearer <jwt token>`. If you are using one of the SDKs, ensure the SDK is configured with your `client_id` and `client_secret` before invoking the method.

## GetChartAreaFillFormat API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type    | Location | Description                        |
| -------------- | ------- | -------- | ---------------------------------- |
| name           | string  | path     | Workbook name.                     |
| sheetName      | string  | path     | Worksheet name.                    |
| chartIndex     | integer | path     | Index of the chart.                |
| folder         | string  | query    | Folder that contains the workbook. |
| storageName    | string  | query    | Name of the storage.               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services. The example below shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Notes**  
- A successful call returns HTTP 200 with the fill‑format details.  
- HTTP 401 indicates an authentication failure (invalid or missing token).  
- HTTP 404 is returned when the specified workbook, worksheet, or chart index does not exist.  
- HTTP 500 denotes a server‑side error; retry the request or contact support if the problem persists.

| Code | Meaning                                             |
|------|-----------------------------------------------------|
| 200  | Success – fill format returned                      |
| 401  | Unauthorized – invalid or missing token             |
| 404  | Not Found – workbook, worksheet, or chart not found |
| 500  | Internal Server Error                               |

For related operations, see **Get Chart Area Border** and **Get Chart Title** endpoints.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}