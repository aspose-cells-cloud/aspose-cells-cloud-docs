---
title: "Update Chart Second Category Axis"
type: docs
url: /charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart, Second Category Axis, REST API, Update Chart, Excel, Cloud API"
description: "Learn how to update the second category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Update Chart Second Category Axis – Aspose.Cells Cloud API"
---

This REST API updates the second category axis of a chart.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### Request parameters

| Parameter Name | Type    | Location | Description                                            |
| -------------- | ------- | -------- | ------------------------------------------------------ |
| name           | string  | path     | The name of the Excel file.                            |
| sheetName      | string  | path     | The worksheet name that contains the chart.            |
| chartIndex     | integer | path     | The zero‑based index of the chart to be updated.       |
| axis           | object  | body     | The second‑category‑axis object with the new settings. |
| folder         | string  | query    | The folder path where the file is stored.              |
| storageName    | string  | query    | The name of the storage service.                       |

**Authentication** – The API requires a valid OAuth 2.0 access token. Generate a JWT token by following the [Authentication Guide](https://docs.aspose.cloud/cells/authentication/). Include the token in the `Authorization` header as shown in the cURL example below.

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* axis settings, e.g., "Title": "New Axis Title", "IsVisible": true */
        }
      }'
```

*Replace `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, and `{storageName}` with your actual values. The request body must contain the `axis` object with the desired settings.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Successful response (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "New Axis Title",
      "IsVisible": true,
      /* additional axis properties */
    }
  }
}
```

**Error responses**  

| Status Code | Description                              |
|-------------|------------------------------------------|
| 400         | Bad request – missing or invalid parameters. |
| 401         | Unauthorized – invalid or missing JWT token. |
| 404         | Not found – the specified file, worksheet, or chart does not exist. |
| 500         | Internal server error – unexpected condition on the server. |

```json
{
  "Code": 400,
  "Message": "Invalid request payload."
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

SDKs simplify development by handling low‑level details and allowing you to focus on your business logic. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
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

**Notes & Best Practices**

* The `chartIndex` parameter is zero‑based; the first chart in a worksheet is index 0.  
* The API supports both `.xlsx` and `.xls` workbook formats.  
* Include only the properties you need in the `axis` object; unspecified properties retain their existing values.  
* Respect rate‑limit guidelines (typically 100 requests per minute per account) to avoid throttling.