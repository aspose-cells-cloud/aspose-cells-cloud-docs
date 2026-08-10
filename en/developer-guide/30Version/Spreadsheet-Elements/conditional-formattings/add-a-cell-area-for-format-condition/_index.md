---
title: Add CellArea to Conditional Formatting
description: Add a cell area to a conditional formatting rule in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL, SDK examples, response schema, and error handling.
keywords: Aspose.Cells, Conditional Formatting, CellArea, REST API, Excel, Cloud SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Add CellArea to Conditional Formatting

**Summary** – Adds a cell area to an existing conditional‑formatting rule in a worksheet.

---

## Prerequisites

1. **Aspose.Cells Cloud account** – obtain your **App SID** and **App Key**.  
2. **JWT token** – generate a JWT token using the App SID/Key (see the [Authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. The target Excel file must already exist in the specified storage/folder.

---

## Authentication

All calls require **JWT token‑based authentication**. Pass the token in the `Authorization` header:

```http
Authorization: Bearer <jwt token>
```

---

## HTTP Request

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Path Parameters

| Name      | Type   | Description                     |
|-----------|--------|---------------------------------|
| `name`    | string | Excel file name (e.g., `Book1.xlsx`). |
| `sheetName`| string| Worksheet that contains the rule (e.g., `Sheet1`). |
| `index`   | integer| Zero‑based index of the conditional‑formatting rule. |

### Query Parameters

| Name        | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `cellArea`  | string | **Yes**  | Cell range to add, in A1 notation (e.g., `A1:C3`). |
| `folder`    | string | No       | Folder path where the file is stored. |
| `storageName`| string| No       | Storage service name. |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Expected Successful Response

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Response schema – `CellArea`**

| Property   | Type | Description |
|------------|------|-------------|
| `StartRow` | int  | Zero‑based index of the first row. |
| `StartColumn`| int| Zero‑based index of the first column. |
| `EndRow`   | int  | Zero‑based index of the last row. |
| `EndColumn`| int  | Zero‑based index of the last column. |

---

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
---

## SDK Examples

Below are short snippets for the most common SDKs. Replace `YOUR_APP_SID` and `YOUR_APP_KEY` with your credentials, and set the generated JWT token where required.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Notes & Tips

- **CellArea format** – Must be a valid A1 range (`A1`, `A1:C3`, `Sheet2!B2:D5`). Invalid formats return **400 Bad Request**.
- **Overlapping areas** – Adding a range that overlaps an existing area of the same rule triggers **409 Conflict**.
- **Zero‑based indexing** – Row/column indices in the response start at `0`. Convert to Excel's 1‑based notation if needed.
- **Storage** – If you omit `folder` and `storageName`, the API uses the default storage/root folder.

---

## Related Operations

- **Delete Cell Area** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Add Condition to Conditional Formatting** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Get Conditional Formatting** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

These operations can be combined to build full conditional‑formatting workflows.

---