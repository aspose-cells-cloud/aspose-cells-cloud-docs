---
title: Convert OLE Object to Image – Aspose.Cells Cloud REST API
date: 2023-11-15
description: "Convert embedded OLE objects in Excel to images (PNG, JPEG, TIFF, GIF, EMF, BMP) via Aspose.Cells Cloud API"
linktitle: Convert OLE Object to Image
type: docs
url: /oleobjects/convert/
aliases: [/convert-oleobject-to-image/]
weight: 40
keywords:
  - convert OLE object to image
  - Aspose.Cells Cloud
  - REST API
  - Excel
  - OLE
  - image conversion
  - PNG
  - JPEG
  - TIFF
  - GIF
  - EMF
  - BMP
ArticleTitle: "Convert OLE Object to Image with Aspose.Cells Cloud REST API"
---

![OLE Object Conversion Workflow](/images/ole-object-workflow.png "OLE Object Conversion: Workbook → API → Output Image")

Retrieve an embedded OLE object from a worksheet and return it in the requested image format.

> **Note**: All Aspose.Cells Cloud APIs require HTTPS. HTTP endpoints are unsupported.

## The Convert OLE Object to Image Web API

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Path Parameters

| Name           | Type    | Required | Description                                |
| -------------- | ------- | -------- | ------------------------------------------ |
| `name`         | string  | ✅       | Name of the workbook (e.g., `Book1.xlsx`). |
| `sheetName`    | string  | ✅       | Worksheet containing the OLE object.       |
| `objectNumber` | integer | ✅       | Zero-based index of the OLE object.        |

### Query Parameters

| Name          | Type   | Required | Description                                                                         |
| ------------- | ------ | -------- | ----------------------------------------------------------------------------------- |
| `format`      | string | ❌       | Target image format: `png`, `jpeg`, `tiff`, `gif`, `emf`, or `bmp`. Default: `png`. |
| `folder`      | string | ❌       | Path to the folder containing the workbook (e.g., `/docs`).                         |
| `storageName` | string | ❌       | Name of the storage (e.g., `MyCloud`).                                              |

### Response

The API returns raw binary image data. Examples for common use cases:

- **Save to file (Linux/macOS)**:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/.../oleobjects/0?format=jpeg" \
    -H "Authorization: Bearer <token>" > oleobject.jpg
  ```

- **Base64 encode (debugging)**:
  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/.../oleobjects/0?format=png" \
    -H "Authorization: Bearer <token>" | base64
  ```

![Sample Converted OLE Object](/images/ole-object-output.png "Result: Converted OLE object as PNG")

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Convert Worksheet OLE Object to Image API with SDKs?

### Convert Worksheet OLE Object to Image API Specification

The <a href="https://reference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObjectRequest" rel="noopener noreferrer">Convert Worksheet OLE Object to Image API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

**cURL Example**

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Authorization: Bearer <jwt-token>" \
  -o oleobject.png
```

> **Tip**: Use `-o` to save the image directly. Replace `<jwt-token>` with your valid token.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

<details>
<summary><strong>C#</strong></summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var config = new Configuration { AccessToken = "YOUR_JWT_TOKEN" };
var api = new OleObjectsApi(config);
var request = new GetWorksheetOleObjectRequest(
    name: "Embedded_OleObject_Sample_Book1.xlsx",
    sheetName: "Sheet1",
    objectNumber: 0,
    format: "png"
);
var stream = api.GetWorksheetOleObject(request);
using var file = File.Create("oleobject.png");
stream.CopyTo(file);
```

</details>

<details>
<summary><strong>Java</strong></summary>

```java
import com.aspose.cells.cloud.ApiException;
import com.aspose.cells.cloud.api.OleObjectsApi;
import com.aspose.cells.cloud.model.requests.*;
import java.io.FileOutputStream;
import java.io.InputStream;

OleObjectsApi api = new OleObjectsApi();
api.getApiClient().setAccessToken("YOUR_JWT_TOKEN");
GetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(
    "Embedded_OleObject_Sample_Book1.xlsx",
    "Sheet1",
    0,
    "png",
    null,
    null
);
InputStream stream = api.getWorksheetOleObject(req);
try (FileOutputStream out = new FileOutputStream("oleobject.png")) {
    stream.transferTo(out);
}
```

</details>

<details>
<summary><strong>Python</strong></summary>

```python
from asposecellscloud import CellsApi, GetWorksheetOleObjectRequest

api = CellsApi()
api.api_client.configuration.access_token = "YOUR_JWT_TOKEN"
request = GetWorksheetOleObjectRequest(
    name="Embedded_OleObject_Sample_Book1.xlsx",
    sheet_name="Sheet1",
    object_number=0,
    format="png"
)
stream = api.get_worksheet_ole_object(request)
with open('oleobject.png', 'wb') as f:
    f.write(stream.read())
```

</details>

<details>
<summary><strong>Node.js</strong></summary>

```javascript
const { CellsApi, GetWorksheetOleObjectRequest } = require("asposecellscloud");

const api = new CellsApi();
api.apiClient.configuration.accessToken = "YOUR_JWT_TOKEN";

const request = new GetWorksheetOleObjectRequest({
  name: "Embedded_OleObject_Sample_Book1.xlsx",
  sheetName: "Sheet1",
  objectNumber: 0,
  format: "png",
});

api.getWorksheetOleObject(request).then((stream) => {
  const fs = require("fs");
  const writeStream = fs.createWriteStream("oleobject.png");
  stream.pipe(writeStream);
});
```

</details>

<details>
<summary><strong>Go</strong></summary>

```go
package main

import (
    "io"
    "os"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "YOUR_JWT_TOKEN"
    api := cells.NewOleObjectsApi(cfg)
    req := cells.GetWorksheetOleObjectRequest{
        Name:         "Embedded_OleObject_Sample_Book1.xlsx",
        SheetName:    "Sheet1",
        ObjectNumber: 0,
        Format:       "png",
    }
    stream, _, err := api.GetWorksheetOleObject(req)
    if err != nil { panic(err) }
    out, _ := os.Create("oleobject.png")
    defer out.Close()
    io.Copy(out, stream)
}
```

</details>

<details>
<summary><strong>PHP</strong></summary>

```php
<?php
require_once 'vendor/autoload.php';
use Aspose\Cells\Cloud\Api\OleObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetOleObjectRequest;

$config = new \Aspose\Cells\Cloud\Configuration();
$config->setAccessToken('YOUR_JWT_TOKEN');
$apiInstance = new OleObjectsApi($config);
$request = new GetWorksheetOleObjectRequest(
    'Embedded_OleObject_Sample_Book1.xlsx',
    'Sheet1',
    0,
    'png'
);
$stream = $apiInstance->getWorksheetOleObject($request);
file_put_contents('oleobject.png', $stream);
?>
```

</details>

<details>
<summary><strong>Ruby</strong></summary>

```ruby
require 'aspose_cells_cloud'
api = AsposeCellsCloud::OleObjectsApi.new
api.api_client.config.access_token = 'YOUR_JWT_TOKEN'
request = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(
  name: 'Embedded_OleObject_Sample_Book1.xlsx',
  sheet_name: 'Sheet1',
  object_number: 0,
  format: 'png'
)
stream = api.get_worksheet_ole_object(request)
File.open('oleobject.png', 'wb') { |f| f.write(stream) }
```

</details>

<details>
<summary><strong>Perl</strong></summary>

```perl
use AsposeCellsCloud::Api::OleObjectsApi;
use AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;

my $api = AsposeCellsCloud::Api::OleObjectsApi->new();
$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';
my $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(
    name => 'Embedded_OleObject_Sample_Book1.xlsx',
    sheet_name => 'Sheet1',
    object_number => 0,
    format => 'png'
);
my $stream = $api->get_worksheet_ole_object(request => $req);
open my $fh, '>', 'oleobject.png' or die $!;
binmode $fh;
print $fh $stream;
close $fh;
```

</details>
