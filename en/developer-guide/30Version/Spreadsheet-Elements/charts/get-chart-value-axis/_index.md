---
title: "Get Chart Value Axis"
type: docs
url: /charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Chart Value Axis, REST API, Excel, Cloud SDK, Get Chart Value Axis
description: "Aspose.Cells Cloud REST API - Retrieve the value axis of a chart in an Excel worksheet."
ArticleTitle: "Get Chart Value Axis - Aspose.Cells Cloud REST API"
linktitle: "Get Chart Value Axis"
---

The **GetChartValueAxis** API (`GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis`) retrieves the value axis properties of a chart from a worksheet in an Excel file stored in the cloud, using Aspose.Cells Cloud REST API; it accepts required path parameters `name`, `sheetName`, and `chartIndex`, and optional query parameters `folder` and `storageName`, returning an AxisResponse that enables developers to programmatically access and analyze chart axis configuration without local Excel installation.

For related operations, see the **[Get Chart Category Axis](/charts/category-axis/get/)** endpoint.

## GetChartValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type    | Location | Description                                             |
| -------------- | ------- | -------- | ------------------------------------------------------- |
| name           | string  | path     | The name of the Excel file (including extension).       |
| sheetName      | string  | path     | The name of the worksheet that contains the chart.      |
| chartIndex     | integer | path     | The zero‑based index of the chart within the worksheet. |
| folder         | string  | query    | The folder in cloud storage where the file is located.  |
| storageName    | string  | query    | The name of the storage service (e.g., Aspose Cloud).   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
 -X GET \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Values",
    "Format": {
      "NumberFormat": "General",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Possible HTTP status codes**

| Code | Description                                 |
|------|---------------------------------------------|
| 200  | Success – the value axis information is returned. |
| 400  | Bad Request – required parameters are missing or invalid. |
| 401  | Unauthorized – authentication token is missing or invalid. |
| 404  | Not Found – the specified workbook, worksheet, or chart does not exist. |
| 500  | Internal Server Error – an unexpected error occurred on the server. |

The response contains a detailed `ValueAxis` object with properties such as `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title`, and `Format`. In a full implementation, additional formatting details may be provided.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}