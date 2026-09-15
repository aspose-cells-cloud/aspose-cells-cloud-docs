---
title: "Get Cells Properties"
type: docs
url: /get-cells-properties/
date: 2024-06-15
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, Worksheet, Cell Properties, Get Cells Properties"
description: "Use Aspose.Cells Cloud REST API to retrieve detailed cell properties—including value, formula, type, and style—from Excel worksheets. Supports both cell references (e.g., A1) and predefined method names (e.g., firstcell, maxrow)."
---

This REST API demonstrates how to retrieve properties of a specific cell or a predefined method (such as `firstcell`, `maxrow`, or `maxdatacolumn`) in an Excel worksheet using Aspose.Cells Cloud.

## Prerequisites

Before using this API, ensure you have:
- An active [Aspose Cloud account](https://dashboard.aspose.cloud/)
- Valid `Client ID` and `Client Secret` obtained from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/)
- An Excel file uploaded to your cloud storage

Authentication is performed using [JWT tokens](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API Endpoint

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

### Request Parameters

| Parameter Name       | Type   | Location | Required | Description                                                                                                                                                                           |
|----------------------|--------|----------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **name**             | string | path     | Yes      | The name of the Excel document.                                                                                                                                                       |
| **sheetName**        | string | path     | Yes      | The name of the worksheet containing the cell.                                                                                                                                        |
| **cellOrMethodName** | string | path     | Yes      | The cell address (e.g., `A1`, `F341`) or a predefined method name (`firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`). |
| **folder**           | string | query    | No       | The folder where the document is stored.                                                                                                                                              |
| **storageName**      | string | query    | No       | The name of the storage service.                                                                                                                                                      |

### cURL Example

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?folder=&storageName=" \
     -H "Authorization: Bearer <JWT_TOKEN>" \
     -H "Accept: application/json"
```

> **Note**: Replace `<JWT_TOKEN>` with a valid access token. Use the `/oauth2/token` endpoint to obtain one.

## Response

Returns a `CellResponse` containing the requested cell’s properties.

### Cell Response Fields

| Field           | Type    | Description                                           |
|-----------------|---------|-------------------------------------------------------|
| `Name`          | string  | Cell address (e.g., `A3`).                            |
| `Row`           | integer | Zero-based row index.                                 |
| `Column`        | integer | Zero-based column index.                              |
| `Value`         | string  | Displayed cell value (formatted as text).             |
| `Type`          | string  | Data type (e.g., `String`, `Double`, `Bool`).         |
| `Formula`       | string  | Formula text (e.g., `=SUM(A1:A10)`), or empty.        |
| `IsFormula`     | boolean | `true` if the cell contains a formula.                |
| `IsMerged`      | boolean | `true` if the cell is part of a merged range.         |
| `IsArrayHeader` | boolean | `true` if the cell is the header of an array formula. |
| `IsInArray`     | boolean | `true` if the cell belongs to an array formula.       |
| `IsErrorValue`  | boolean | `true` if the cell contains an error (e.g., `#N/A`).  |
| `IsInTable`     | boolean | `true` if the cell is inside an Excel table.          |
| `IsStyleSet`    | boolean | `true` if a custom style is applied.                  |
| `HtmlString`    | string  | HTML-encoded representation of the cell value.        |
| `Style.link`    | object  | Hyperlink to the style resource.                      |
| `link`          | object  | Self-referencing link to the cell.                    |

### Example Response (200 OK)

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "String",
    "Formula": "",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": true,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

### HTTP Status Codes

| Code | Meaning               | Description                                      |
|------|-----------------------|--------------------------------------------------|
| 200  | OK                    | Cell retrieved successfully; response contains cell data. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type, invalid cell name). |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token.         |
| 404  | Not Found             | Document, worksheet, or cell not found.         |
| 413  | Payload Too Large     | Request exceeds size limits.                    |
| 500  | Internal Server Error | Unexpected server error during processing.      |

## SDK Examples

Using an SDK is the most efficient way to integrate the API. SDKs handle authentication, serialization, and error handling automatically.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Example: C#
var cellsApi = new CellsApi(clientId, clientSecret);
var result = cellsApi.GetWorksheetCell(name, sheetName, "A3", folder: folder, storage: storageName);
Console.WriteLine($"Cell Value: {result.Cell.Value}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example: Java
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
CellResponse response = cellsApi.getWorksheetCell(name, sheetName, "A3", folder, storageName, null);
System.out.println("Cell Value: " + response.getCell().getValue());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example: PHP
$cellsApi = new CellsApi($clientId, $clientSecret);
$response = $cellsApi->GetWorksheetCell($name, $sheetName, "A3", $folder, $storageName);
echo "Cell Value: " . $response->getCell()->getValue();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example: Ruby
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
response = cells_api.get_worksheet_cell(name, sheet_name, 'A3', folder: folder, storage_name: storage_name)
puts "Cell Value: #{response.cell.value}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
// Example: Node.js (TypeScript)
const cellsApi = new CellsApi(clientId, clientSecret);
const response = await cellsApi.getWorksheetCell(name, sheetName, "A3", folder, storageName);
console.log(`Cell Value: ${response.body.cell.value}`);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example: Python
from asposecellscloud.api import CellsApi
cells_api = CellsApi(client_id, client_secret)
response = cells_api.get_worksheet_cell(name, sheet_name, "A3", folder=folder, storage_name=storage_name)
print(f"Cell Value: {response.cell.value}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example: Perl
my $cells_api = AsposeCellsCloud::API->new(
    client_id => $client_id,
    client_secret => $client_secret,
);
my $response = $cells_api->GetWorksheetCell(
    name => $name,
    sheet_name => $sheet_name,
    cell_or_method_name => "A3",
    folder => $folder,
    storage_name => $storage_name
);
print "Cell Value: " . $response->{cell}->{value} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example: Go
cellsApi, err := NewCellsApi(clientId, clientSecret)
if err != nil { log.Fatal(err) }
resp, _, err := cellsApi.GetWorksheetCell(context.Background(), name, sheetName, "A3", folder, storageName)
if err != nil { log.Fatal(err) }
fmt.Printf("Cell Value: %s\n", resp.Cell.Value)
```

{{< /tab >}}

{{< /tabs >}}

See the full SDK list in the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).

## Related Operations

- [Get Cell Data from a Worksheet](/cells/get-cell-data-from-a-worksheet/)
- [Get First Cell from Excel Worksheet](/cells/get-first-cell-from-excel-worksheet/)
- [Get Last Cell of Excel Worksheet](/cells/get-last-cell-of-excel-worksheet/)
- [Get MaxRow from Excel Worksheet](/cells/get-maxrow-from-excel-worksheet/)
- [Get MaxDataRow from Excel Worksheet](/cells/get-maxdatarow-from-excel-worksheet/)
- [Get MaxColumn from Excel Worksheet](/cells/get-maxcolumn-from-excel-worksheet/)
- [Get MaxDataColumn from Excel Worksheet](/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Get MinRow from Excel Worksheet](/cells/get-minrow-from-excel-worksheet/)
- [Get MinDataRow from Excel Worksheet](/cells/get-mindatarow-from-excel-worksheet/)
- [Get MinColumn from Excel Worksheet](/cells/get-mincolumn-from-excel-worksheet/)
- [Get MinDataColumn from Excel Worksheet](/cells/get-mindatacolumn-from-excel-worksheet/)

## See Also

- [Set Cell Data](/cells/put-worksheet-cell/)
- [Get Worksheet Cells](/cells/get-worksheet-cells/)
- [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)