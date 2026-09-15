---
title: Convert OLE Object to Image – Aspose.Cells Cloud REST API
date: 2023-11-15
description: >-
  Extract and convert embedded OLE objects in Excel files to PNG, JPEG, TIFF, GIF, EMF, or BMP using Aspose.Cells Cloud REST API. Includes cURL examples, SDK snippets for 8+ languages, and best practices.
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
---

![OLE Object Conversion Workflow](/images/ole-object-workflow.png "OLE Object Conversion: Workbook → API → Output Image")

## Convert OLE Object to Image

Retrieve an embedded OLE object from a worksheet and return it in the requested image format.

> **Note**: All Aspose.Cells Cloud APIs require HTTPS. HTTP endpoints are unsupported.

---

## Prerequisites

Before calling this endpoint, ensure you have:

1. **Aspose.Cells Cloud account** – Sign up at the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).
2. **Workbook uploaded to cloud storage** – Use the [Upload File API](/cells/storage/file/upload/) or the Aspose Cloud UI.
3. **JWT access token** – Follow the [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) to generate a valid token.

---

## Security & Authentication

All requests must include a valid JWT token in the `Authorization` header:

```http
Authorization: Bearer <jwt-token>
```

> **Important**: Always use `https://api.aspose.cloud`. HTTP (`http://`) is unsupported and will fail.

---

## Request

### HTTP Method

`GET`

### Endpoint

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}
```

### Path Parameters

| Name           | Type   | Required | Description                               |
|----------------|--------|----------|-------------------------------------------|
| `name`         | string | ✅       | Name of the workbook (e.g., `Book1.xlsx`). |
| `sheetName`    | string | ✅       | Worksheet containing the OLE object.      |
| `objectNumber` | integer| ✅       | Zero-based index of the OLE object.       |

### Query Parameters

| Name          | Type   | Required | Description                                                                 |
|---------------|--------|----------|-----------------------------------------------------------------------------|
| `format`      | string | ❌       | Target image format: `png`, `jpeg`, `tiff`, `gif`, `emf`, or `bmp`. Default: `png`. |
| `folder`      | string | ❌       | Path to the folder containing the workbook (e.g., `/docs`).                |
| `storageName` | string | ❌       | Name of the storage (e.g., `MyCloud`).                                     |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Authorization: Bearer <jwt-token>" \
  -o oleobject.png
```

> **Tip**: Use `-o` to save the image directly. Replace `<jwt-token>` with your valid token.

---

## Response

| Status | Content-Type              | Description                                     |
|--------|---------------------------|-------------------------------------------------|
| `200`  | `image/png` (or specified format) | Binary image data of the converted OLE object. |
| `400`  | `application/json`        | Invalid request parameters.                    |
| `401`  | `application/json`        | Authentication failed.                         |
| `404`  | `application/json`        | Workbook, worksheet, or OLE object not found.  |
| `500`  | `application/json`        | Internal server error.                         |

### Handling the Response

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

---

## Error Responses

| Status | Error Code           | Message                                          |
|--------|----------------------|--------------------------------------------------|
| `400`  | `InvalidParameter`   | One or more parameters are invalid or missing.   |
| `401`  | `AuthenticationFailed`| Token expired, missing, or malformed.           |
| `404`  | `PropertyNotFound`   | Workbook, worksheet, or OLE object does not exist. |
| `500`  | `InternalError`      | Unexpected server error.                         |

---

## SDK Examples

The following snippets demonstrate how to call the operation using official Aspose.Cells Cloud SDKs. Replace `YOUR_JWT_TOKEN` with your actual token.

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
const { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');

const api = new CellsApi();
api.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';

const request = new GetWorksheetOleObjectRequest({
    name: 'Embedded_OleObject_Sample_Book1.xlsx',
    sheetName: 'Sheet1',
    objectNumber: 0,
    format: 'png'
});

api.getWorksheetOleObject(request).then(stream => {
    const fs = require('fs');
    const writeStream = fs.createWriteStream('oleobject.png');
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

> **Tip**: Full SDK source code and samples are available in the [Aspose.Cells Cloud GitHub Repository](https://github.com/aspose-cells-cloud).

---

## Related Operations

| Operation              | Description                                     | Documentation Link                     |
|------------------------|-------------------------------------------------|----------------------------------------|
| `POST /cells/{name}/worksheets/{sheetName}/oleobjects` | Add a new OLE object to a worksheet. | [/cells/add-ole-object/](/cells/add-ole-object/) |
| `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}` | Update an existing OLE object. | [/cells/update-ole-object/](/cells/update-ole-object/) |
| `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}` | Remove an OLE object. | [/cells/delete-ole-object/](/cells/delete-ole-object/) |
| `GET /cells/{name}/worksheets/{sheetName}/oleobjects` | List all OLE objects in a worksheet. | [/cells/list-ole-objects/](/cells/list-ole-objects/) |

---

## Additional Resources

- **[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject)**  
- **[Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)**  
- **[SDK Source Code & Examples](https://github.com/aspose-cells-cloud)**  
- **[Performance & Accessibility](https://docs.aspose.cloud/cells/performance-accessibility/)**  
  - Lighthouse Target: >90 performance, >95 accessibility (WCAG 2.1 AA)  
  - All images include descriptive `alt` text for screen readers.

---

> **Next Steps**: Try converting an OLE object interactively using our [Swagger UI Demo](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject).