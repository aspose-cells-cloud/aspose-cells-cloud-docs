---
title: "Aspose.Cells Cloud API – Update Chart Value Axis (POST /valueaxis)"
type: docs
url: /charts/value-axis/update/
weight: 160
keywords:
  - Aspose.Cells Cloud
  - Update Chart Value Axis
  - REST API
  - Excel chart axis
  - POST valueaxis
  - cURL example
  - SDK
  - JSON payload
  - chart axis settings
description: "Learn how to update the value axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes endpoint, parameters, request‑body schema, sample cURL/JSON payload, and error‑response details."
---

This REST API updates the chart value axis.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### Request Parameters

| Parameter Name | Type    | Location | Description |
|----------------|---------|----------|-------------|
| name           | string  | path     | Name of the Excel file stored in the cloud. |
| sheetName      | string  | path     | Name of the worksheet that contains the chart. |
| chartIndex     | integer | path     | Zero‑based index of the chart whose value axis will be updated. |
| axis           | object  | body     | JSON object that defines the new value‑axis settings (e.g., `minimum`, `maximum`, `majorUnit`). |
| folder         | string  | query    | Cloud folder path where the file is located (optional). |
| storageName    | string  | query    | Name of the storage service to use (optional). |

### Request Body Schema (`axis` object)

The **axis** object may contain any of the following properties:

- `minimum` (number) – Lower bound of the axis.
- `maximum` (number) – Upper bound of the axis.
- `majorUnit` (number) – Interval between major tick marks.
- `minorUnit` (number) – Interval between minor tick marks.
- `logBase` (number) – Base of the logarithm when `isLogarithmic` is `true`.
- `isLogarithmic` (boolean) – Indicates whether the axis uses a logarithmic scale.
- `displayUnit` (string) – Unit label displayed on the axis (e.g., `"Thousands"`).
- `tickMark` (string) – Style of tick marks (e.g., `"inside"`).
- `crossAt` (number) – Position where the axis crosses the perpendicular axis.

Only the properties you need to change have to be included in the JSON payload.

### Sample Request Body

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

### cURL Example

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false
      }'
```

### Successful Response

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Error Responses

| HTTP Status | Code | Message                              |
|-------------|------|--------------------------------------|
| 400         | 400  | Invalid request parameters or body. |
| 401         | 401  | Authentication failed.              |
| 404         | 404  | Specified file, worksheet, or chart not found. |
| 500         | 500  | Internal server error.               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false
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

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartValueAxis.js" >}}
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