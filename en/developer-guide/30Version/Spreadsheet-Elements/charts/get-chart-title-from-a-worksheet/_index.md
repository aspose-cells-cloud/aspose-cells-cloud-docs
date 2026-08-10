---
title: "Get Chart Title from a Worksheet"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Chart Title"
  - "Excel"
  - "REST API"
  - "Get Chart Title"
  - "cURL"
  - "SDK"
  - "Excel chart automation"
  - "GET chart title"
description: "Learn how to retrieve a chart title from an Excel worksheet using Aspose.Cells Cloud REST API. Includes endpoint, parameters, authentication, sample cURL and SDK code."
ArticleTitle: "Get Chart Title from a Worksheet"
---

This REST API retrieves the title of a chart that is stored in a worksheet of an Excel workbook.

**Prerequisites**: To call this endpoint you must have a valid Aspose.Cells Cloud OAuth2/JWT access token with the `Cells.Read` scope. The workbook must already be uploaded to the specified storage location.

## GetWorksheetChartTitle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request parameters

| Parameter Name | Type    | Location | Description                                    |
| -------------- | ------- | -------- | ---------------------------------------------- |
| name           | string  | path     | Name of the workbook file.                     |
| sheetName      | string  | path     | Name of the worksheet that contains the chart. |
| chartIndex     | integer | path     | Zero‑based index of the chart.                 |
| folder         | string  | query    | Folder path where the workbook is stored.      |
| storageName    | string  | query    | Name of the storage service.                   |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Sales Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Response fields**

| Field               | Description                                     |
| ------------------- | ----------------------------------------------- |
| `Title.Text`        | The actual text displayed as the chart title.   |
| `Title.Font.Name`   | Font family used for the title (e.g., _Arial_). |
| `Title.Font.Size`   | Font size in points.                            |
| `Title.Font.IsBold` | Indicates whether the title text is bold.       |

**Response status codes**

| Code | Description |
|------|-------------|
| 200 OK | The chart title was retrieved successfully. |
| 401 Unauthorized | Authentication failed or token is missing/invalid. |
| 404 Not Found | The specified workbook, worksheet, or chart does not exist. |
| 500 Internal Server Error | An unexpected server error occurred. |

**Notes**: The chart index is zero‑based; ensure the chart exists. If the workbook has not been uploaded, upload it first using the appropriate API.

**How to extract the title in a script (using `jq`)**

```bash
# Assuming the JSON response is saved in response.json
title=$(jq -r '.Title.Text' response.json)
echo "Chart title: $title"
```

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# example using Aspose.Cells Cloud SDK
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java example using Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP example using Aspose.Cells Cloud SDK
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby example using Aspose.Cells Cloud SDK
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python example using Aspose.Cells Cloud SDK
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js example using Aspose.Cells Cloud SDK
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) example using Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift example using Aspose.Cells Cloud SDK
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Chart title: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl example using Aspose.Cells Cloud SDK
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

You can also refer to the individual SDK documentation for more advanced scenarios, such as updating or deleting a chart title.  

**See also**: [Update Chart Title](/charts/title/put/), [Delete Chart Title](/charts/title/delete/).