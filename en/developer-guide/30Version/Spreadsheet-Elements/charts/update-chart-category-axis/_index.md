---
title: "Update Chart Category Axis"
type: docs
url: /charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart, Category Axis, REST API, Excel, Cloud SDK"
description: "Updates the category axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Update Chart Category Axis – Aspose.Cells Cloud API"
linktitle: "Update Category Axis"
---
The **PostChartCategoryAxis** API (`POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis`) updates the category axis of a specific chart in a worksheet using Aspose.Cells Cloud, allowing developers to programmatically modify axis properties such as scaling, formatting, and labels by sending an axis configuration object in the request body.

## The Post Chart Category Axis Web API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| chartIndex | Integer | Path | The chart index. |
| axis | class:axis | HTTPBody | Axis |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

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

**Example Response**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### **Response**

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
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

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