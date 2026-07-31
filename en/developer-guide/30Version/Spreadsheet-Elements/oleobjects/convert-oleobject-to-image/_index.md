---
title: "Convert OLE Object to Image – Aspose.Cells Cloud REST API"
description: "Retrieve an embedded OLE object from an Excel worksheet and convert it to PNG, JPEG, TIFF, GIF, EMF, or BMP using Aspose.Cells Cloud REST API."
keywords:
  - "convert OLE object to image"
  - "Aspose.Cells Cloud"
  - "REST API"
  - "Excel"
  - "OLE"
  - "image conversion"
  - "PNG"
  - "JPEG"
  - "TIFF"
  - "GIF"
  - "EMF"
  - "BMP"
weight: 40
---

# Convert OLE Object to Image

Retrieve an embedded OLE object from a worksheet and return it in the requested image format.

---

## Prerequisites

Before calling this endpoint make sure you have:

1. **Aspose.Cells Cloud account** – sign‑up at the [Aspose Cloud portal](https://dashboard.aspose.cloud/).  
2. **Workbook uploaded to cloud storage** – use the **Upload File** API or the Aspose Cloud UI.  
3. **JWT access token** – obtain a token following the [authentication guide](/total/getting-started/rest-api-overview/authenticating-api-requests/).  

---

## Security & Authentication

All Aspose.Cells Cloud APIs require **JWT token‑based authentication**. Include the token in the `Authorization` header:

```http
Authorization: Bearer <jwt-token>
```

Only HTTPS endpoints are supported; never use `http://`.

---

## Request

### HTTP Method
`GET`

### Endpoint
```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Path Parameters

| Name          | Type   | Required | Description                              |
|---------------|--------|----------|------------------------------------------|
| `name`        | string | ✅       | Name of the workbook file (e.g., `Book1.xlsx`). |
| `sheetName`   | string | ✅       | Worksheet that contains the OLE object. |
| `objectNumber`| integer| ✅       | Zero‑based index of the OLE object.      |

### Query Parameters

| Name        | Type   | Required | Description |
|-------------|--------|----------|-------------|
| `format`    | string | ❌       | Desired image format (`png`, `jpeg`, `tiff`, `gif`, `emf`, `bmp`). If omitted the default is `png`. |
| `folder`    | string | ❌       | Path to the folder where the workbook resides. |
| `storageName`| string| ❌       | Name of the storage service (e.g., `MyCloud`). |

---

## Request Example (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*Replace `<jwt-token>` with a valid JWT token.*

---

## Response

| Status | Content‑Type            | Description |
|--------|-------------------------|-------------|
| `200`  | `image/png` (or requested format) | Binary image data representing the OLE object. |
| `400`  | `application/json`      | Invalid request parameters. |
| `401`  | `application/json`      | Authentication failed (missing/invalid JWT). |
| `404`  | `application/json`      | Specified workbook, worksheet, or OLE object not found. |
| `500`  | `application/json`      | Server‑side error. |

### Handling the Binary Payload

The API returns raw image bytes. You can:

* **Save directly to a file** (Linux/macOS example):

  ```bash
  curl -o oleobject.png "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>"
  ```

* **Encode to Base64** for debugging or embedding in JSON:

  ```bash
  curl -s "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
       -H "Authorization: Bearer <jwt-token>" | base64
  ```

  *Sample (truncated) Base64 output:*

  ```
  iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkY…
  ```

---

## Error Responses

| HTTP Status | Code                   | Message |
|-------------|------------------------|---------|
| `400`       | `InvalidParameter`     | One or more request parameters are invalid. |
| `401`       | `AuthenticationFailed`| Missing or invalid JWT token. |
| `404`       | `PropertyNotFound`     | The requested workbook, worksheet, or OLE object does not exist. |
| `500`       | `InternalError`        | An unexpected error occurred on the server. |

---

## SDK Examples

The following snippets demonstrate how to call the operation with the official SDKs. Replace `YOUR_JWT_TOKEN` and other placeholders with your actual values.

| Language | Example |
|----------|---------|
| **C#** | <details><summary>Show code</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model.Requests;\n\nvar config = new Configuration { AccessToken = \"YOUR_JWT_TOKEN\" };\nvar api = new OleObjectsApi(config);\nvar request = new GetWorksheetOleObjectRequest(\n    name: \"Embedded_OleObject_Sample_Book1.xlsx\",\n    sheetName: \"Sheet1\",\n    objectNumber: 0,\n    format: \"png\"\n);\nvar stream = api.GetWorksheetOleObject(request);\nusing var file = File.Create(\"oleobject.png\");\nstream.CopyTo(file);\n```</details> |
| **Java** | <details><summary>Show code</summary>```java\nimport com.aspose.cells.cloud.ApiException;\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.model.*;\nimport com.aspose.cells.cloud.model.requests.*;\nimport java.io.FileOutputStream;\nimport java.io.InputStream;\n\nOleObjectsApi api = new OleObjectsApi();\napi.getApiClient().setAccessToken(\"YOUR_JWT_TOKEN\");\nGetWorksheetOleObjectRequest req = new GetWorksheetOleObjectRequest(\n    \"Embedded_OleObject_Sample_Book1.xlsx\",\n    \"Sheet1\",\n    0,\n    \"png\",\n    null,\n    null\n);\nInputStream stream = api.getWorksheetOleObject(req);\ntry (FileOutputStream out = new FileOutputStream(\"oleobject.png\")) {\n    stream.transferTo(out);\n}\n```</details> |
| **Python** | <details><summary>Show code</summary>```python\nfrom asposecellscloud import CellsApi, GetWorksheetOleObjectRequest\n\napi = CellsApi()\napi.api_client.configuration.access_token = \"YOUR_JWT_TOKEN\"\nrequest = GetWorksheetOleObjectRequest(\n    name=\"Embedded_OleObject_Sample_Book1.xlsx\",\n    sheet_name=\"Sheet1\",\n    object_number=0,\n    format=\"png\"\n)\nstream = api.get_worksheet_ole_object(request)\nwith open('oleobject.png', 'wb') as f:\n    f.write(stream.read())\n```</details> |
| **Node.js** | <details><summary>Show code</summary>```javascript\nconst { CellsApi, GetWorksheetOleObjectRequest } = require('asposecellscloud');\n\nconst api = new CellsApi();\napi.apiClient.configuration.accessToken = 'YOUR_JWT_TOKEN';\n\nconst request = new GetWorksheetOleObjectRequest({\n    name: 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheetName: 'Sheet1',\n    objectNumber: 0,\n    format: 'png'\n});\napi.getWorksheetOleObject(request).then(stream => {\n    const fs = require('fs');\n    const writeStream = fs.createWriteStream('oleobject.png');\n    stream.pipe(writeStream);\n});\n```</details> |
| **Go** | <details><summary>Show code</summary>```go\npackage main\nimport (\n    \"io\"\n    \"os\"\n    cells \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\nfunc main() {\n    cfg := cells.NewConfiguration()\n    cfg.AccessToken = \"YOUR_JWT_TOKEN\"\n    api := cells.NewOleObjectsApi(cfg)\n    req := cells.GetWorksheetOleObjectRequest{\n        Name:         \"Embedded_OleObject_Sample_Book1.xlsx\",\n        SheetName:    \"Sheet1\",\n        ObjectNumber: 0,\n        Format:       \"png\",\n    }\n    stream, _, err := api.GetWorksheetOleObject(req)\n    if err != nil { panic(err) }\n    out, _ := os.Create(\"oleobject.png\")\n    defer out.Close()\n    io.Copy(out, stream)\n}\n```</details> |
| **PHP** | <details><summary>Show code</summary>```php\n<?php\nrequire_once 'vendor/autoload.php';\nuse Aspose\\Cells\\Cloud\\Api\\OleObjectsApi;\nuse Aspose\\Cells\\Cloud\\Model\\Requests\\GetWorksheetOleObjectRequest;\n\n$config = new \\Aspose\\Cells\\Cloud\\Configuration();\n$config->setAccessToken('YOUR_JWT_TOKEN');\n$apiInstance = new OleObjectsApi($config);\n$request = new GetWorksheetOleObjectRequest(\n    'Embedded_OleObject_Sample_Book1.xlsx',\n    'Sheet1',\n    0,\n    'png'\n);\n$stream = $apiInstance->getWorksheetOleObject($request);\nfile_put_contents('oleobject.png', $stream);\n?>\n```</details> |
| **Ruby** | <details><summary>Show code</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::OleObjectsApi.new\napi.api_client.config.access_token = 'YOUR_JWT_TOKEN'\nrequest = AsposeCellsCloud::GetWorksheetOleObjectRequest.new(\n  name: 'Embedded_OleObject_Sample_Book1.xlsx',\n  sheet_name: 'Sheet1',\n  object_number: 0,\n  format: 'png'\n)\nstream = api.get_worksheet_ole_object(request)\nFile.open('oleobject.png', 'wb') { |f| f.write(stream) }\n```\n</details> |
| **Perl** | <details><summary>Show code</summary>```perl\nuse AsposeCellsCloud::Api::OleObjectsApi;\nuse AsposeCellsCloud::Object::GetWorksheetOleObjectRequest;\n\nmy $api = AsposeCellsCloud::Api::OleObjectsApi->new();\n$api->{api_client}->{config}->{access_token} = 'YOUR_JWT_TOKEN';\nmy $req = AsposeCellsCloud::Object::GetWorksheetOleObjectRequest->new(\n    name => 'Embedded_OleObject_Sample_Book1.xlsx',\n    sheet_name => 'Sheet1',\n    object_number => 0,\n    format => 'png'\n);\nmy $stream = $api->get_worksheet_ole_object(request => $req);\nopen my $fh, '>', 'oleobject.png' or die $!;\nbinmode $fh;\nprint $fh $stream;\nclose $fh;\n```</details> |

*(The full list of SDKs is available in the [GitHub repository](https://github.com/aspose-cells-cloud).)*

---

## Related Operations

- **Add OLE Object** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`
- **Update OLE Object** – `PUT /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Delete OLE Object** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}`
- **Get OLE Object List** – `GET /cells/{name}/worksheets/{sheetName}/oleobjects`

For details, see the corresponding API reference pages.

---

## Additional Resources

- **OpenAPI Specification** – <https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject>
- **Authentication guide** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **SDK repositories** – <https://github.com/aspose-cells-cloud>
- **Performance & Accessibility** – Run Lighthouse and axe‑core audits to ensure optimal load times and WCAG 2.1 AA compliance.

---