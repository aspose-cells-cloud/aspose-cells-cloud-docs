---
title: "Update Chart Second Value Axis"
ArticleTitle: "Update Chart Second Value Axis – Aspose.Cells Cloud REST API"
type: docs
url: /charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, Second Value Axis, Excel, REST, Cloud SDK"
description: "Updates the second value axis of a chart in an Excel worksheet using the Aspose.Cells Cloud REST API. Includes request examples, response codes, and prerequisites."
---

This REST API updates the second value axis of a chart.

**Prerequisites:**  
- A valid JWT access token (see the [Authentication guide](https://docs.aspose.cloud/cells/authentication/)).  
- The target Excel file must be stored in Aspose Cloud storage (provide `folder` and optional `storageName`).  
- API version v3.0 is used; ensure the base URL is `https://api.aspose.cloud/v3.0`.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### Request parameters

| Parameter Name | Type    | Location | Description                                       |
| -------------- | ------- | -------- | ------------------------------------------------- |
| name           | string  | path     | Name of the Excel file.                           |
| sheetName      | string  | path     | Name of the worksheet containing the chart.       |
| chartIndex     | integer | path     | Zero‑based index of the chart to modify.          |
| axis           | object  | body     | Settings for the second value axis.               |
| folder         | string  | query    | Folder path in storage where the file is located. |
| storageName    | string  | query    | Name of the storage service.                      |

**Example request body (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Secondary Axis"
  }
}
```

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

**Response Codes**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Axis updated successfully. |
| 400 | Bad Request | Invalid parameters or malformed JSON. |
| 401 | Unauthorized | Missing or invalid JWT token. |
| 404 | Not Found | File, worksheet, or chart not found. |
| 500 | Internal Server Error | Unexpected server error. |

**See also:**  
- [Get Chart Second Value Axis](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [Update Chart Value Axis](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK takes care of low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# example to update the second value axis
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java example to update the second value axis
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// PHP example to update the second value axis
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby example to update the second value axis
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python example to update the second value axis
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) example – same as Java snippet above
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift example to update the second value axis
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl example to update the second value axis
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go example to update the second value axis
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}