---
title: Add Condition to Conditional Formatting
description: Learn how to add a condition to a worksheet's conditional formatting using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, authentication, cURL example, SDK snippets, and error handling.
keywords: "Aspose.Cells Cloud, Conditional Formatting, Add Condition, REST API, Excel, Worksheet"
type: docs
url: /conditional-formattings/add-a-condition/
aliases:
  - /add-a-condition-for-format-condition/
weight: 40
---

# Add Condition to Conditional Formatting

Add a condition to an existing conditional‑formatting rule in a worksheet using Aspose.Cells Cloud REST API (v3.0).

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Authentication** | A valid JWT access token (Bearer) obtained via the OAuth 2.0 flow. |
| **API Version** | v3.0 – the endpoint URL contains `/v3.0/`. |
| **Storage** | The workbook must reside in a storage location accessible to Aspose.Cells Cloud (default is `Default`). |
| **Permissions** | Read/Write permission on the target workbook. |
| **Supported Formats** | Any workbook format supported by Aspose.Cells (e.g., `.xlsx`, `.xls`, `.xlsm`). |

---

## Endpoint

**HTTP Method:** `PUT`  
**URL:**  

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition
```

| Parameter | Location | Type | Required | Description |
|-----------|----------|------|----------|-------------|
| `name` | Path | string | **Yes** | Name of the workbook file (including extension). |
| `sheetName` | Path | string | **Yes** | Name of the worksheet that contains the conditional formatting. |
| `index` | Path | integer | **Yes** | Zero‑based index of the conditional‑formatting collection to modify. |
| `type` | Query | string | **Yes** | Condition type. Allowed values: `CellValue`, `Expression`, `ColorScale`, `DataBar`, `IconSet`, `Top10`, `UniqueValues`, `DuplicateValues`, `ContainsText`, `NotContainsText`, `BeginsWith`, `EndsWith`, `ContainsBlanks`, `NotContainsBlanks`, `ContainsErrors`, `NotContainsErrors`, `TimePeriod`, `AboveAverage`. |
| `operatorType` | Query | string | **Yes** | Operator for the condition. Allowed values: `Between`, `Equal`, `GreaterThan`, `GreaterOrEqual`, `LessThan`, `None`, `NotBetween`, `NotEqual`. |
| `formula1` | Query | string | **Yes** | First formula/value associated with the condition. |
| `formula2` | Query | string | No | Second formula/value (required only for operators that need two values, e.g., `Between`). |
| `folder` | Query | string | No | Folder in storage where the workbook is located. |
| `storageName` | Query | string | No | Name of the storage service. |

> **Note:** All path parameters (`name`, `sheetName`, `index`) and the query parameters `type`, `operatorType`, `formula1` are mandatory. `formula2`, `folder`, and `storageName` are optional.

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition?type=CellValue&operatorType=Equal&formula1=v1&formula2=v2" \
 -X PUT \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt_token>"
```

*Replace `<jwt_token>` with a valid access token and adjust `name`, `sheetName`, `index`, and query values as needed.*

---

## Successful Response

```json
{
  "Code": "200",
  "Status": "OK"
}
```

The response indicates that the condition was added successfully. The operation returns a generic `CellsCloudResponse` object that contains the HTTP status code and a short status message.

---

## Error Responses

| HTTP Code | Reason | Example Body |
|-----------|--------|--------------|
| **400** | Bad Request – missing or invalid parameters. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | Unauthorized – missing or invalid JWT token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | Not Found – workbook, worksheet, or conditional‑formatting index does not exist. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | Internal Server Error – unexpected server failure. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

---

## Notes & Common Pitfalls

* **Parameter Encoding** – URL‑encode special characters in `formula1`/`formula2` (e.g., spaces → `%20`).  
* **Operator Compatibility** – Some operators (e.g., `Between`) require both `formula1` and `formula2`. Omit `formula2` for operators that need only a single value.  
* **Conditional‑Formatting Index** – The index is zero‑based. Use the **Get Conditional Formattings** endpoint to retrieve the correct index if you are unsure.  
* **Storage Folder** – If the workbook resides in a non‑default folder, supply the `folder` query parameter; otherwise the API assumes the root folder.  
* **Rate Limiting** – Aspose.Cells Cloud enforces per‑account request limits. If you receive a 429 response, back‑off and retry after a short delay.

---

## SDK Examples

Below are ready‑to‑run snippets for the most popular SDKs. Replace placeholder values (`YOUR_FILE`, `YOUR_SHEET`, etc.) with your own data.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var apiInstance = new ConditionalFormattingsApi();
        string name = "Book1.xlsx";
        string sheetName = "Sheet1";
        int index = 0;
        string type = "CellValue";
        string operatorType = "Equal";
        string formula1 = "v1";
        string formula2 = "v2";
        string folder = null;          // optional
        string storageName = null;     // optional

        try
        {
            var response = apiInstance.PutWorksheetFormatConditionCondition(
                name, sheetName, index, type, operatorType, formula1, formula2, folder, storageName);
            Console.WriteLine($"Status: {response.Status}");
        }
        catch (Exception e)
        {
            Console.WriteLine("Exception when calling ConditionalFormattingsApi.PutWorksheetFormatConditionCondition: " + e.Message);
        }
    }
}
```

### Java

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class AddConditionExample {
    public static void main(String[] args) {
        ConditionalFormattingsApi api = new ConditionalFormattingsApi();

        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        int index = 0;
        String type = "CellValue";
        String operatorType = "Equal";
        String formula1 = "v1";
        String formula2 = "v2";

        try {
            CellsCloudResponse resp = api.putWorksheetFormatConditionCondition(
                    name, sheetName, index, type, operatorType, formula1, formula2, null, null);
            System.out.println("Response: " + resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Node.js

```javascript
const { ConditionalFormattingsApi, ApiClient } = require('asposecellscloud');
const api = new ConditionalFormattingsApi();

const name = "Book1.xlsx";
const sheetName = "Sheet1";
const index = 0;
const type = "CellValue";
const operatorType = "Equal";
const formula1 = "v1";
const formula2 = "v2";

api.putWorksheetFormatConditionCondition(
    name,
    sheetName,
    index,
    type,
    operatorType,
    formula1,
    formula2,
    null,
    null
).then((response) => {
    console.log('Status:', response.body.Status);
}).catch((err) => {
    console.error(err);
});
```

### Ruby

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
name = 'Book1.xlsx'
sheet_name = 'Sheet1'
index = 0
type = 'CellValue'
operator_type = 'Equal'
formula1 = 'v1'
formula2 = 'v2'

begin
  result = api_instance.put_worksheet_format_condition_condition(
    name, sheet_name, index, type, operator_type, formula1, formula2, nil, nil
  )
  puts "Status: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: #{e}"
end
```

### Perl

```perl
use AsposeCellsCloud::ConditionalFormattingsApi;

my $api_instance = AsposeCellsCloud::ConditionalFormattingsApi->new();

my $name         = 'Book1.xlsx';
my $sheet_name   = 'Sheet1';
my $index        = 0;
my $type         = 'CellValue';
my $operatorType = 'Equal';
my $formula1     = 'v1';
my $formula2     = 'v2';

eval {
    my $result = $api_instance->put_worksheet_format_condition_condition(
        name => $name,
        sheet_name => $sheet_name,
        index => $index,
        type => $type,
        operator_type => $operatorType,
        formula1 => $formula1,
        formula2 => $formula2,
        folder => undef,
        storage_name => undef
    );
    print "Status: " . $result->{status} . "\n";
};
if ($@) {
    warn "Exception when calling ConditionalFormattingsApi->put_worksheet_format_condition_condition: $@\n";
}
```

### Go

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := sdk.NewConditionalFormattingsApi(cfg)

    name := "Book1.xlsx"
    sheetName := "Sheet1"
    index := int32(0)
    condType := "CellValue"
    operatorType := "Equal"
    formula1 := "v1"
    formula2 := "v2"

    resp, _, err := api.PutWorksheetFormatConditionCondition(
        name, sheetName, index, condType, operatorType, formula1, formula2, nil, nil,
    )
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

> **Missing SDKs** – If a language you need is not listed, refer to the generic **API Reference** and construct the HTTP request manually.

---

## See Also

- **[Get Conditional Formattings](https://docs.aspose.cloud/cells/conditional-formattings/get-conditional-formattings/)** – Retrieve the list of conditional‑formatting rules for a worksheet.  
- **[Delete Conditional Formatting](https://docs.aspose.cloud/cells/conditional-formattings/delete-a-conditional-formatting/)** – Remove an existing conditional‑formatting rule.  
- **[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionCondition)** – Full machine‑readable definition of this operation.  

---