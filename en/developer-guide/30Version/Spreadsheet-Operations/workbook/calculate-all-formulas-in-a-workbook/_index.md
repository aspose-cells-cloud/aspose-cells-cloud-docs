---  
title: "Calculate All Formulas on an Excel Workbook"  
second_title: "Document"  
linktitle: "Calculate"  
type: docs  
url: /calculate-all-formulas-on-an-excel-file/  
aliases: [/calculate-all-formulas-in-a-workbook/,/workbook/calculate-all-formulas/]  
keywords: "Aspose.Cells, calculate formulas, Excel workbook, REST API, cloud SDK"  
description: "Learn how to calculate every formula in an Excel workbook using the Aspose.Cells Cloud REST API. Includes cURL example, request parameters, detailed response schema, prerequisites, error‑handling guidance, and inline SDK code samples for C#, Java, PHP, Ruby, Node.js, Python, Perl, and Go."  
weight: 140  
---  

This REST API calculates **all formulas** in an Excel workbook.

### Prerequisites  

Before calling the endpoint, ensure you have completed the following steps:

- **Aspose Cloud account** – sign up and obtain your *Client Id* and *Client Secret*.  
- **JWT token** – generate an access token using the authentication API.  
- **Workbook upload** – upload the target Excel file to the desired storage location (default storage is used if none is specified).  
- **Correct permissions** – the token must have permission to read and write the specified storage.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

The request parameters are listed below:

| Parameter Name | Type               | Location | Description                                                                                     |
|----------------|--------------------|----------|-------------------------------------------------------------------------------------------------|
| **name**       | string             | path     | Name of the workbook file.                                                                      |
| **options**    | CalculationOptions | body     | JSON object that specifies calculation settings (e.g., `CalcStackSize`, `IgnoreError`).       |
| **ignoreError**| boolean            | query    | When `true`, errors encountered during calculation are ignored.                                |
| **folder**     | string             | query    | Path to the folder that contains the workbook.                                                  |
| **storageName**| string             | query    | Name of the storage service where the workbook is stored.                                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### Response Details  

| Field          | Type   | Description                                                                                     |
|----------------|--------|-------------------------------------------------------------------------------------------------|
| **Code**       | int    | HTTP‑like status code (200 indicates success).                                                  |
| **Status**     | string | Short textual description of the result (e.g., `OK`).                                         |
| **WorkbookUrl**| string | Direct URL from which the updated workbook can be downloaded.                                   |
| **ErrorMessage**| string| Detailed error information when the request fails; `null` on success.                         |

#### Next Steps / Common Errors  

- **Handle calculation errors** – set `ignoreError=false` to receive an error response when a formula cannot be evaluated.  
- **Rate‑limit awareness** – check the `X-RateLimit-Remaining` header; if it reaches `0`, back‑off before retrying.  
- **HTTP status guidance**:  
  - `400` – Invalid request parameters.  
  - `401` – Authentication failed (invalid or expired JWT).  
  - `404` – Workbook not found.  
  - `500` – Server‑side error; contact Aspose support if it persists.  

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions } = require('asposecellscloud');

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
    name: "Book1.xlsx",
    ignoreError: true,
    options: options
});

api.postWorkbookCalculateFormula(request).then(response => {
    console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}