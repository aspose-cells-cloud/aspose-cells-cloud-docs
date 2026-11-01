---
title: "Clear Objects in an Excel File"
second_title: "Aspose.Cells Cloud"
date: 2023-11-15T10:00:00Z
lastmod: 2024-06-15T14:30:00Z
version: "v3.0"
linktitle: "Clear"
url: /clear/
aliases: [/clearobjects/]
keywords: ["clear objects", "Excel API", "remove comments", "Aspose.Cells Cloud", "REST API clear charts", "delete shapes Excel", "clear pivot tables Cloud"]
description: "Use Aspose.Cells Cloud REST API to delete comments, charts, shapes, list objects, hyperlinks, OLE objects, pivot tables, validations, and background elements from Excel workbooks. Includes cURL examples and SDK code snippets in 8 programming languages."
weight: 39
type: docs
ArticleTitle: "Clear Excel Objects with Aspose.Cells Cloud REST API"
---
The **PostClearObjects** API (`POST https://api.aspose.cloud/v3.0/cells/clearobjects`) enables developers to clear specific internal elements—such as charts, comments, shapes, pivot tables, hyperlinks, or validation rules—from Excel workbooks via Aspose.Cells Cloud, returning a cleaned workbook in a requested output format like XLSX, PDF, or CSV, with optional scope control via sheet name and support for password-protected files.

## The Post Clear Objects Web API

```http
POST https://api.aspose.cloud/v3.0/cells/clearobjects
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| objecttype | String | Query | chart/comment/picture/shape/listobject/hyperlink/oleobject/pivottable/validation/Background |
| sheetname | String | Query | The worksheet name, specify the scope of the deletion. |
| outFormat | String | Query | The output data file format.(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers) |
| password | String | Query | The password needed to open an Excel file. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| region | String | Query | The regional settings for workbook. |

> **Note**: While `File` and `objecttype` are both marked as required in the API spec, `objecttype` may be optional if you intend to clear *all* supported objects (behavior depends on backend defaults). For clarity and predictability, always specify `objecttype`.

---

### Example Response

```json
[
  {
    "Name": "FilesResult",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesResult"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

> **Note**: The response returns Base64-encoded content for all processed files. For large files, consider using the `disk` or `folder` parameters (if supported in future versions) or streaming the response.

---

### Example Request (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/clearobjects?objecttype=comment,chart&outFormat=XLSX" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>" \
  -F "File=@sample.xlsx"
```

## Cloud SDK Family

Using an SDK is the recommended approach to accelerate development. SDKs abstract low-level details (e.g., authentication, multipart handling, Base64 decoding) and improve code maintainability.

For the full list of SDKs and source code, see the [Aspose.Cells Cloud GitHub Repository](https://github.com/aspose-cells-cloud).

### Code Examples

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

> **Figure 1**: C# SDK example for clearing comments and charts from an Excel file.  
```csharp
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet
var config = new Configuration { ClientId = "xxxx", ClientSecret = "xxxx" };
var cellsApi = new CellsApi(config);
var response = cellsApi.PostClearObjects("sample.xlsx", objecttype: "comment,chart", outFormat: "XLSX");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

> **Figure 2**: Java SDK example for clearing comments and charts.  
```java
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java
CellsApi cellsApi = new CellsApi(System.getenv("CellsCloudClientID"), System.getenv("CellsCloudClientSecret"));
FilesResult response = cellsApi.postClearObjects("sample.xlsx", "comment,chart", "XLSX", null, null, null, null, null);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

> **Figure 3**: PHP SDK example for clearing comments and charts.  
```php
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php
$apiInstance = new CellsApi(getenv("CellsCloudClientID"), getenv("CellsCloudClientSecret"));
$response = $apiInstance->postClearObjects("sample.xlsx", "comment,chart", "XLSX");
```

{{< /tab >}}

{{< tab tabNum="4" >}}

> **Figure 4**: Ruby SDK example for clearing comments and charts.  
```ruby
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby
cells_api = AsposeCellsCloud::LightCellsApi.new('client_id', 'client_secret')
response = cells_api.post_clear_objects('sample.xlsx', objecttype: 'comment,chart', out_format: 'XLSX')
```

{{< /tab >}}

{{< tab tabNum="5" >}}

> **Figure 5**: Node.js SDK example for clearing comments and charts.  
```typescript
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node
const cellsApi = new CellsApi(process.env.CLIENT_ID, process.env.CLIENT_SECRET);
const res = await cellsApi.postClearObjects('sample.xlsx', 'comment,chart', 'XLSX');
```

{{< /tab >}}

{{< tab tabNum="6" >}}

> **Figure 6**: Python SDK example for clearing comments and charts.  
```python
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python
api = CellsApi(os.environ['CLIENT_ID'], os.environ['CLIENT_SECRET'])
response = api.post_clear_objects('sample.xlsx', objecttype='comment,chart', out_format='XLSX')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

> **Figure 7**: Perl SDK example for clearing comments and charts.  
```perl
# See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl
my $config = AsposeCellsCloud::Configuration->new(
  client_id => 'xxxx',
  client_secret => 'xxxx'
);
my $api = AsposeCellsCloud::LightCellsApi->new(config => $config);
my $res = $api->post_clear_objects('sample.xlsx', 'comment,chart', 'XLSX');
```

{{< /tab >}}

{{< tab tabNum="8" >}}

> **Figure 8**: Go SDK example for clearing comments and charts.  
```go
// See full example: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go
cfg := cells.NewConfiguration(os.Getenv("CLIENT_ID"), os.Getenv("CLIENT_SECRET"))
api := cells.NewLightCellsApi(cfg)
resp, _, err := api.PostClearObjects(context.Background(), "sample.xlsx", "comment,chart", "XLSX")
```

{{< /tab >}}

{{< /tabs >}}

---

## See Also

- [Encrypt Excel Files](/encrypt/)  
- [Protect Workbooks](/protect/)  
- [Delete Worksheets](/delete-worksheets/)  
- [Merge Excel Files](/merge/)  

---

> **Version Note**: This documentation reflects API version `v3.0`. For the latest changes, see the [Aspose.Cells Cloud Release Notes](https://docs.aspose.cloud/cells/release-notes/).