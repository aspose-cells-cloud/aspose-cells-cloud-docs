---
title: "Set Cell Value in Worksheet – Aspose.Cells Cloud REST API v3.0"
date: 2024-05-15
tags:
  - rest-api
  - excel
  - cell-update
  - cells-cloud
categories:
  - api-reference
  - aspose-cells
weight: 70
description: "Aspose.Cells Cloud REST API v3.0: Set Excel cell values via POST /cells/{name}/worksheets/{sheetName}/cells/{cellName}. Includes cURL, .NET, Java, Python, and Node.js examples."
---

# Set Cell Value in Worksheet

Use the Aspose.Cells Cloud REST API to programmatically set the value of a specific cell in an Excel worksheet. This operation supports strings, numbers, formulas, and typed values, with full integration via cURL, SDKs (C#, Java, Python, Node.js, PHP, Ruby, Perl, Go), and OpenAPI-compliant tools.

> 📝 **Note**: This documentation covers Aspose.Cells Cloud API v3.0. For the latest features, see the [v4.0 Preview](/total/getting-started/v4-preview/). Always verify SDK version compatibility before integration.

## REST API Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

### Path Parameters

| Parameter | Type   | Required | Description                     |
|-----------|--------|----------|---------------------------------|
| `name`    | string | Yes      | The Excel file name (e.g., `myWorkbook.xlsx`). |
| `sheetName` | string | Yes    | The worksheet name (case-sensitive). |
| `cellName` | string | Yes     | A1-style cell address (e.g., `A1`, `B15`, `Z100`). |

### Query Parameters

| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `value`   | string | No       | The value to assign to the cell. |
| `type`    | string | No       | Data type of `value`: `int`, `string`, `float`, `bool`, `date`, `duration`. Defaults to `string` if omitted. |
| `formula` | string | No       | A formula to assign (e.g., `=SUM(A2:A15)`). Overrides `value` if both provided. |
| `folder`  | string | No       | Folder path containing the file (e.g., `/docs/`). |
| `storageName` | string | No   | Custom storage name (e.g., `First Storage`). |

> ⚠️ **Security Note**: Replace `<jwt token>` with your actual JWT token (see [Authentication](/total/getting-started/rest-api-overview/authenticating-api-requests/)). Never commit tokens to source control, logs, or public repositories.

## Authentication

All requests require a valid [JWT token](/total/getting-started/rest-api-overview/authenticating-api-requests/) in the `Authorization` header:

```http
Authorization: Bearer <your-jwt-token>
```

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9..."
```

> ✅ **Tip**: Use the [Aspose.Cells Cloud Dashboard](https://dashboard.aspose.cloud/) to generate and manage your client credentials and tokens securely.

## Response

Returns a `CellResponse` object with HTTP status `200 OK` on success.

### CellResponse Fields

| Field           | Type    | Description |
|-----------------|---------|-------------|
| `Name`          | string  | Cell address (e.g., `A3`). |
| `Row`           | integer | Zero-based row index. |
| `Column`        | integer | Zero-based column index. |
| `Value`         | string  | Displayed cell value. |
| `Type`          | string  | Internal type (e.g., `IsString`, `IsNumeric`). |
| `Formula`       | string  | Formula text (if present). |
| `IsFormula`     | bool    | `true` if the cell contains a formula. |
| `IsMerged`      | bool    | `true` if part of a merged range. |
| `IsArrayHeader` | bool    | `true` if cell is an array formula header. |
| `IsInArray`     | bool    | `true` if cell belongs to an array formula. |
| `IsErrorValue`  | bool    | `true` if cell contains an error (e.g., `#DIV/0!`). |
| `IsInTable`     | bool    | `true` if cell is inside an Excel table. |
| `IsStyleSet`    | bool    | `true` if a custom style is applied. |
| `HtmlString`    | string  | HTML-formatted representation of the value. |
| `Style.link`    | object  | Link to the cell’s style resource. |

### Example Response (200 OK)

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "1234",
    "Type": "IsNumeric",
    "Formula": null,
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "1234",
    "Style": {
      "link": {
        "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/styles/0",
        "Rel": "self",
        "Type": "application/json"
      }
    }
  }
}
```

### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Cell value updated successfully. |
| 400  | Bad Request           | Invalid path/query parameters (e.g., missing `name`, unsupported `type`). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token. |
| 403  | Forbidden             | Insufficient permissions for the operation. |
| 404  | Not Found             | File, worksheet, or cell not found. |
| 413  | Payload Too Large     | Request exceeds size limits (e.g., formula too long). |
| 500  | Internal Server Error | Unexpected server error. |

## SDK Examples

Using SDKs automates authentication, serialization, and error handling. See the [Aspose.Cells Cloud SDKs GitHub repository](https://github.com/aspose-cells-cloud) for full source code.

{{< tabs tabTotal="8" tabID="sdk-tabs" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Install-Package Aspose.Cells-Cloud -Version 22.8.0

var config = new Configuration 
{ 
    ClientId = "YOUR_CLIENT_ID", 
    ClientSecret = "YOUR_CLIENT_SECRET" 
};
var cellsApi = new CellsApi(config.ClientId, config.ClientSecret, "v3.0", "https://api.aspose.cloud");

string fileName = "myWorkbook.xlsx";
string sheetName = "Sheet1";
string cellName = "A3";
string value = "1234";
string type = "int";

var response = cellsApi.PostWorksheetCellSetValue(fileName, sheetName, cellName, value, type);
Console.WriteLine($"Cell {response.Cell.Name} updated: {response.Cell.Value}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Add dependency: com.aspose:aspose-cells-cloud:22.8.0

ApiClient apiClient = new ApiClient("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET", "v3.0");
CellsApi cellsApi = new CellsApi(apiClient);

String fileName = "myWorkbook.xlsx";
String sheetName = "Sheet1";
String cellName = "A3";
String value = "1234";
String type = "int";

CellResponse response = cellsApi.postWorksheetCellSetValue(fileName, sheetName, cellName, value, type, null, null);
System.out.println("Updated cell: " + response.getCell().getName() + " = " + response.getCell().getValue());
```
{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// composer require aspose-cells-cloud/aspose-cells-cloud-php

$config = [
    'clientId' => 'YOUR_CLIENT_ID',
    'clientSecret' => 'YOUR_CLIENT_SECRET',
    'basePath' => 'https://api.aspose.cloud',
    'apiVersion' => 'v3.0'
];

$cellsApi = new Aspose\Cells\CellsApi(null, null, null, $config['clientId'], $config['clientSecret']);

$response = $cellsApi->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "int"
);
echo "Cell {$response->getCell()->getName()} updated to {$response->getCell()->getValue()}\n";
```
{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# gem install aspose_cells_cloud

require 'aspose_cells_cloud'

AsposeCellsCloud.configure do |config|
  config.client_id = 'YOUR_CLIENT_ID'
  config.client_secret = 'YOUR_CLIENT_SECRET'
end

api_instance = AsposeCellsCloud::CellsApi.new
name = 'myWorkbook.xlsx'
sheet_name = 'Sheet1'
cell_name = 'A3'
value = '1234'
type = 'int'

response = api_instance.post_worksheet_cell_set_value(name, sheet_name, cell_name, value, type)
puts "Cell #{response.cell.name} updated: #{response.cell.value}"
```
{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
// npm install @aspose/cells-cloud --save

import { CellsApi } from "@aspose/cells-cloud";

const cellsApi = new CellsApi(
  "YOUR_CLIENT_ID",
  "YOUR_CLIENT_SECRET"
);

const fileName = "myWorkbook.xlsx";
const sheetName = "Sheet1";
const cellName = "A3";
const value = "1234";
const type = "int";

const response = await cellsApi.postWorksheetCellSetValue(
  fileName,
  sheetName,
  cellName,
  value,
  type
);
console.log(`Cell ${response.body.cell.name} updated: ${response.body.cell.value}`);
```
{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# pip install aspose-cells-cloud

from asposecellscloud.api import CellsApi
from asposecellscloud.models import Cell

api = CellsApi(
    client_id="YOUR_CLIENT_ID",
    client_secret="YOUR_CLIENT_SECRET"
)

response = api.post_worksheet_cell_set_value(
    name="myWorkbook.xlsx",
    sheet_name="Sheet1",
    cell_name="A3",
    value="1234",
    type="int"
)
print(f"Cell {response.cell.name} updated: {response.cell.value}")
```
{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new(
    client_id => 'YOUR_CLIENT_ID',
    client_secret => 'YOUR_CLIENT_SECRET'
);

my $cells_api = AsposeCellsCloud::CellsApi->new(
    'ApiClient' => AsposeCellsCloud::ApiClient->new($config)
);

my $response = $cells_api->post_worksheet_cell_set_value(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "int"
);

print "Cell $response->{Cell}->{Name} updated: $response->{Cell}->{Value}\n";
```
{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go

import (
    "context"
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)

config := cells.NewConfiguration()
config.AppKey = "YOUR_CLIENT_ID"
config.AppSid = "YOUR_CLIENT_SECRET"

api := cells.NewCellsApiWithConfiguration(config)
ctx := context.Background()

resp, _, err := api.PostWorksheetCellSetValue(ctx, "myWorkbook.xlsx", "Sheet1", "A3", "1234", "int", nil, nil, nil)
if err != nil {
    log.Fatal(err)
}
fmt.Printf("Cell %s updated: %s\n", *resp.Cell.Name, *resp.Cell.Value)
```
{{< /tab >}}

{{< /tabs >}}

## Internal Links

- [Authentication Overview](/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Read Cell Values](/cells-cloud/api-reference/read-cell/)  
- [Apply Styles to Cells](/cells-cloud/api-reference/set-cell-style/)  
- [SDK Documentation & Source Code](/cells-cloud/sdks/overview/)

## See Also

- [Aspose.Cells Cloud API Reference](https://apireference.aspose.cloud/cells/#/Cells)  
- [OpenAPI Specification for `PostWorksheetCellSetValue`](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue)  
- [GitHub SDK Repositories](https://github.com/aspose-cells-cloud)