---
title: "Update Chart Category Axis"
type: docs
url: /charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart Category Axis, REST API, Excel, Cloud SDK, Excel chart, category axis update"
description: "Updates the category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Update Chart Category Axis – Aspose.Cells Cloud API"
---

This REST API updates a chart’s category axis.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### Request parameters

| Parameter Name | Type    | Location | Description |
| -------------- | ------- | -------- | ----------- |
| name           | string  | path     | Name of the Excel file. |
| sheetName      | string  | path     | Name of the worksheet that contains the chart. |
| chartIndex     | integer | path     | Zero‑based index of the chart to be updated. |
| axis           | object  | body     | JSON object that defines the category axis properties. |
| folder         | string  | query    | Folder in cloud storage where the file is located (optional). |
| storageName    | string  | query    | Name of the storage (optional). |

**Request Body Schema – `axis` object**

| Property | Type   | Description |
|----------|--------|-------------|
| IsAutomaticMajorUnit | boolean | Determines whether the major unit is calculated automatically. |
| MajorUnit | number | Value of the major unit when `IsAutomaticMajorUnit` is `false`. |
| IsAutomaticMinorUnit | boolean | Determines whether the minor unit is calculated automatically. |
| MinorUnit | number | Value of the minor unit when `IsAutomaticMinorUnit` is `false`. |
| Title | object | Title settings for the axis (e.g., `Text`, `Font`, `Visible`). |
| TickLabelPosition | string | Position of tick labels (e.g., `Low`, `High`, `NextToAxis`). |
| ... | ... | Additional axis properties as defined in the API spec. |

**Response Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200  | OK      | The category axis was updated successfully. |
| 400  | Bad Request | The request is malformed or missing required parameters. |
| 401  | Unauthorized | Authentication failed – invalid or missing JWT token. |
| 404  | Not Found | Specified file, worksheet, or chart does not exist. |
| 500  | Internal Server Error | An unexpected error occurred on the server. |

**Prerequisites / Authentication**

To call this endpoint you must obtain a JWT access token from the Aspose.Cells Cloud authentication service (`/connect/token`). Include the token in the `Authorization` header as shown in the example below.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Category Axis",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Notes

* The endpoint requires HTTPS; using HTTP may trigger mixed‑content warnings in browsers.
* All placeholder values (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) must be replaced with actual identifiers.
* Supported chart types for category‑axis updates are listed in the API reference.

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}