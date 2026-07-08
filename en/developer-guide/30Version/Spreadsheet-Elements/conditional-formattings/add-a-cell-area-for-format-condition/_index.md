---
title: "Add CellArea to Conditional Formatting"
type: docs
url: /conditional-formattings/add-cell-area/
aliases: [/add-a-cell-area-for-format-condition/]
keywords: "Aspose.Cells Cloud, conditional formatting, add cell area, REST API, Excel, SDK"
description: "Add a cell area to a conditional formatting rule in Excel via Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL, SDK examples, and error handling."
weight: 30
---

This REST API adds a cell area to a format condition.

## Security and Authentication
The Aspose.Cells Cloud APIs are secure and require [JWT token‑based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Request Parameters

| Parameter Name | Type    | Location | Description                                                    |
| -------------- | ------- | -------- | -------------------------------------------------------------- |
| name           | string  | path     | The name of the Excel file.                                    |
| sheetName      | string  | path     | The name of the worksheet that contains the condition.         |
| index          | integer | path     | The zero‑based index of the conditional formatting rule.       |
| cellArea       | string  | query    | The cell range to add, expressed in A1 notation (e.g., A1:C3). |
| folder         | string  | query    | The folder where the file is stored.                           |
| storageName    | string  | query    | The name of the storage service.                               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionArea) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Successful response –

A JSON object containing `Code` `200` and `Status` `OK`. The body may also include the updated `CellArea` object.

#### Updated CellArea schema
| Property | Type   | Description                         |
|----------|--------|-------------------------------------|
| StartRow | int    | Zero‑based index of the first row.  |
| StartColumn | int | Zero‑based index of the first column. |
| EndRow   | int    | Zero‑based index of the last row.   |
| EndColumn| int    | Zero‑based index of the last column.|

### Common error responses

- **400 Bad Request** – `{ "Code":"400", "Message":"Invalid cellArea format." }`
- **401 Unauthorized** – `{ "Code":"401", "Message":"Invalid or missing JWT token." }`
- **403 Forbidden** – `{ "Code":"403", "Message":"Insufficient permissions." }`
- **404 Not Found** – `{ "Code":"404", "Message":"Worksheet or conditional formatting rule not found." }`
- **409 Conflict** – `{ "Code":"409", "Message":"CellArea overlaps with an existing area." }`
- **500 Internal Server Error** – `{ "Code":"500", "Message":"Unexpected server error." }`

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-FormatConditionArea-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$apiInstance = new ConditionalFormattingsApi($config);
$name = 'Book1.xlsx';
$sheetName = 'sheet1';
$index = 0;
$cellArea = 'A1:C3';
$folder = null;
$storageName = null;

try {
    $result = $apiInstance->putWorksheetFormatConditionArea($name, $sheetName, $index, $cellArea, $folder, $storageName);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ConditionalFormattingsApi->putWorksheetFormatConditionArea: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-FormatConditionArea-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))
name = 'Book1.xlsx'
sheet_name = 'sheet1'
index = 0
cell_area = 'A1:C3'

try:
    result = api_instance.put_worksheet_format_condition_area(name, sheet_name, index, cell_area)
    print(result)
except ApiException as e:
    print("Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_area: %s\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) example using Aspose.Cells Cloud SDK
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

String name = "Book1.xlsx";
String sheetName = "sheet1";
Integer index = 0;
String cellArea = "A1:C3";

try {
    com.aspose.cloud.cells.model.ResponseMessage response = api.putWorksheetFormatConditionArea(name, sheetName, index, cellArea, null, null);
    System.out.println(response);
} catch (Exception e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

let name = "Book1.xlsx"
let sheetName = "sheet1"
let index = 0
let cellArea = "A1:C3"

api.putWorksheetFormatConditionArea(name: name, sheetName: sheetName, index: index, cellArea: cellArea, folder: nil, storageName: nil) { result, error in
    if let err = error {
        print("Error: \\(err)")
    } else if let res = result {
        print(res)
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-FormatConditionArea-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "597f99e44a3ac676ca8273b28f088ad2" >}}

{{< /tab >}}

{{< /tabs >}}

Developers can also refer to related operations such as **Delete Cell Area** and **Add Condition to Conditional Formatting** for further workflow integration.