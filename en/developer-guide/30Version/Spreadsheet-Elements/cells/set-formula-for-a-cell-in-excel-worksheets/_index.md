---
title: "Set Cell Formula in Excel Worksheets"
type: docs
url: /set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, Set Formula, Worksheet, Cell, Cloud SDK, cURL"
description: "Learn how to set a formula for a specific cell in an Excel worksheet using Aspose.Cells Cloud REST API. Includes cURL example, full parameter list, error handling, and SDK code samples."
---

This REST API sets a **cell formula** in an Excel file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

**Prerequisites**  
Before calling this endpoint you must obtain an OAuth2 access token and include it in the `Authorization` header. The workbook must already exist in the selected storage (or be uploaded beforehand).

**Request parameters**

| Parameter Name | Type   | Location | Required | Description                              |
|----------------|--------|----------|----------|------------------------------------------|
| name           | string | path     | Y        | Name of the Excel document.              |
| sheetName      | string | path     | Y        | Name of the worksheet.                   |
| cellName       | string | path     | Y        | Address of the target cell (e.g., **A1**).|
| value          | string | query    | N        | Value to assign to the cell.             |
| type           | string | query    | N        | Data type of the value (e.g., **string**).|
| formula        | string | query    | N        | Formula to apply to the cell (e.g., **sum(A1,A2)**). |
| folder         | string | query    | N        | Folder that contains the document.       |
| storageName    | string | query    | N        | Name of the storage service.             |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

Use the cURL command‑line tool to call Aspose.Cells web services.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=string&formula=sum(A1,A2)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
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

**Error handling**  
The API can return the following status codes:

| Code | Meaning                | Example JSON payload |
|------|------------------------|----------------------|
| 400  | Bad Request – missing or invalid parameters | `{ "Code": 400, "Message": "The 'formula' parameter is required." }` |
| 401  | Unauthorized – invalid or missing token | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| 404  | Not Found – workbook or worksheet does not exist | `{ "Code": 404, "Message": "File not found." }` |
| 500  | Internal Server Error – unexpected condition | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# example – set formula for a cell
// Replace <access-token>, <file-name>, etc. with your values.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java example – set formula for a cell
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP example – set formula for a cell
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby example – set formula for a cell
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python example – set formula for a cell
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js example – set formula for a cell
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) example – set formula for a cell
// Similar to the standard Java example; ensure you use the Android-compatible SDK.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Swift example not available**. The SDK for Swift is currently under development.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl example – set formula for a cell
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Go example – set formula for a cell
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}