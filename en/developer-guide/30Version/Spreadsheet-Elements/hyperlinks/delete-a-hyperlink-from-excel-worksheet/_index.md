---
title: "Delete Worksheet Hyperlink"
type: docs
url: /hyperlinks/delete/
keywords: "Aspose.Cells Cloud, delete hyperlink, Excel API, REST delete hyperlink, worksheet hyperlink removal"
description: "Delete a worksheet hyperlink by index using Aspose.Cells Cloud API. Learn required parameters, authentication, and see code samples for C#, Java, Python, and more."
weight: 40
---

This REST API deletes a worksheet hyperlink by its index on an Excel worksheet.

**Quick‑Start**

1️⃣ Obtain a **Bearer JWT token** (see the *Authentication* section).  
2️⃣ Build the request URL using your file name, worksheet name, and the zero‑based `hyperlinkIndex`.  
3️⃣ (Optional) Append `folder` and `storageName` query parameters if the file is not in the root folder.  
4️⃣ Send a **DELETE** request. A successful call returns `200 OK`.

### Prerequisites
- A valid **Aspose Cloud** account.  
- An active **JWT access token** with the `Cells` scope.  
- The target Excel file must already exist in the selected storage location.  

### Authentication
Aspose.Cells Cloud uses OAuth 2.0. To obtain a token, POST to the token endpoint:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

The response contains an `access_token`. Use this token in the `Authorization` header of every request:

```http
Authorization: Bearer <access_token>
```

### REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

The request parameters are:

| Parameter Name | Type    | Location | Required | Description |
|----------------|---------|----------|----------|-------------|
| **name**           | string  | path     | ✅ | Name of the Excel document. |
| **sheetName**      | string  | path     | ✅ | Name of the worksheet. |
| **hyperlinkIndex** | integer | path     | ✅ | Zero‑based index of the hyperlink to delete. |
| **folder**         | string  | query    | ❌ | Folder containing the document (default: root). |
| **storageName**    | string  | query    | ❌ | Name of the storage service (default storage used if omitted). |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

#### Responses
| Status Code | Description | Example Body |
|------------|-------------|--------------|
| **200 OK** | Hyperlink deleted successfully. | `{"Code":200,"Status":"OK"}` |
| **400 Bad Request** | Missing or invalid parameters. | `{"Code":400,"Message":"Invalid hyperlinkIndex."}` |
| **401 Unauthorized** | Authentication token is missing or invalid. | `{"Code":401,"Message":"Invalid access token."}` |
| **404 Not Found** | The file, worksheet, or hyperlink index does not exist. | `{"Code":404,"Message":"Resource not found."}` |
| **500 Internal Server Error** | Unexpected server error. | `{"Code":500,"Message":"Internal server error."}` |

#### Notes / Edge Cases
- Deleting a **non‑existent** `hyperlinkIndex` returns **404 Not Found**.  
- If the worksheet is empty, the same **404** response is returned.  
- `folder` and `storageName` are optional; omit them only when the file resides in the default storage root.  

## Cloud SDK Family

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. Please check the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs. Inline snippets are provided for reliability; a link to the original Gist is kept for reference.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Source: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Source: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Status: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Source: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
# Source: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Source: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require('asposecellscloud');
const api = new AsposeCellsCloud.CellsApi('<client_id>', '<client_secret>');

api.deleteWorksheetHyperlink('test1.xlsx', 'Sheet1', 0, null, null)
   .then(() => console.log('Hyperlink deleted'))
   .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
# Source: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hyperlink deleted')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
# Source: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Status: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Source: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hyperlink deleted")
    }
}
```

{{< /tab >}}

{{< /tabs >}}

**FAQ**

**Q:** *How do I delete a hyperlink from a worksheet using Aspose.Cells Cloud?*  
**A:** Send a **DELETE** request to `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}` with a valid Bearer token. Supply `name`, `sheetName`, and the zero‑based `hyperlinkIndex`. Optional query parameters `folder` and `storageName` can be used to target non‑default locations.

**Q:** *What HTTP status codes can be returned when deleting a worksheet hyperlink?*  
**A:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, and 500 Internal Server Error (see the **Responses** table above).

**Q:** *Do I need to specify a folder or storage name when deleting a hyperlink?*  
**A:** No. Both `folder` and `storageName` are optional. Omit them to use the default storage and the root folder. Include them only when the file resides elsewhere.