---
title: "Get Chart Category Axis"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, Chart Category Axis, REST API, Excel, Cloud API"
description: "Retrieves the category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Get Chart Category Axis – Aspose.Cells Cloud API Documentation"
---

This REST API retrieves the **Category Axis** of a chart.  
To call this endpoint you must provide a valid OAuth 2.0 access token, and the workbook must be stored in Aspose Cloud storage.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### Request parameters

| Parameter Name | Type    | Location | Description                                            |
| -------------- | ------- | -------- | ------------------------------------------------------ |
| name           | string  | path     | The name of the workbook file.                         |
| sheetName      | string  | path     | The name of the worksheet containing the chart.        |
| chartIndex     | integer | path     | Zero‑based index of the chart whose axis is requested. |
| folder         | string  | query    | The folder path in storage where the workbook resides. |
| storageName    | string  | query    | The name of the storage service (if not the default).  |

**Status Codes**

| Status Code | Description                                             |
| ----------- | ------------------------------------------------------- |
| 200         | Successful response with Category Axis details.        |
| 400         | Bad request – missing or invalid parameters.           |
| 401         | Unauthorized – authentication failed.                  |
| 404         | Not found – workbook, worksheet, or chart does not exist. |
| 500         | Internal server error.                                  |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
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

For modifying the category axis, see the **[Update Chart Category Axis](/charts/category-axis/update/)** page.

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Get Chart Category Axis – Aspose.Cells Cloud API",
  "description": "Retrieves the category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API.",
  "url": "https://docs.aspose.cloud/cells/charts/category-axis/get/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-08",
  "keywords": "Aspose.Cells, Chart Category Axis, REST API, Excel, Cloud API"
}
</script>