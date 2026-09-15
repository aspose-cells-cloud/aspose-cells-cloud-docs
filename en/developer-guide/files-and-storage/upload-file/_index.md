---
title: "Upload File to Cloud Storage"
url: /cells/upload-file/
linktitle: "Upload File"
description: "Securely upload Excel files to cloud storage using Aspose.Cells Cloud REST API. Includes cURL examples, JWT authentication, request parameters, and SDK support for C#, Java, Python, and more."
keywords: "Aspose.Cells Cloud upload API, Excel file upload REST API, cloud storage upload, multipart/form-data, JWT authentication"
type: docs
weight: 100
last_updated: 2024-06-20
tags:
  - upload
  - cloud
  - excel
  - rest-api
---

The **Upload File** API enables developers to upload Excel and other supported files directly to cloud storage for subsequent processing with Aspose.Cells Cloud services. Files are transmitted via `multipart/form-data`, and the API supports overwrite operations with optional storage targeting via `storageName`. This guide covers authentication, request structure, response format, error handling, and practical usage examples.

## **Aspose.Cells Cloud Upload File API**

```
PUT https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Prerequisites**

- An active [Aspose Cloud account](https://dashboard.aspose.cloud/)
- Valid App SID and App Key (used to generate JWT tokens)
- File size ≤ 2 GB (per API limit)
- Supported formats: XLS, XLSX, XLSB, XLSM, CSV, TSV, ODS, and more

---

### **Authentication**

All requests require a [JWT token](https://docs.aspose.cloud/cells/getting-started/rest-api-overview/authenticating-api-requests/) issued via OAuth 2.0.

```bash
-H "Authorization: Bearer {access_token}"
```

> 🔒 **Security Note**: Tokens expire after 24 hours. Refresh tokens are required for long-running integrations.

---

### **Request Parameters**

| Parameter    | Type   | Location | Required | Description                                                                 |
|--------------|--------|----------|----------|-----------------------------------------------------------------------------|
| `UploadFiles`| File   | FormData | Yes      | The file to upload (multipart/form-data field name: `UploadFiles`)        |
| `path`       | String | Path     | Yes      | Destination path in cloud storage (e.g., `input/Report.xlsx`)              |
| `storageName`| String | Query    | No       | Name of the cloud storage (defaults to first configured storage if omitted) |

---

### **Response Format**

On success, the API returns a `FilesUploadResult` object:

```json
{
  "Uploaded": ["Report.xlsx"],
  "Errors": []
}
```

| Field     | Type       | Description                                  |
|-----------|------------|----------------------------------------------|
| `Uploaded`| `string[]` | List of successfully uploaded file names    |
| `Errors`  | `Error[]`  | List of errors (empty on success)            |

#### HTTP Status Codes

| Code | Description |
|------|-------------|
| `200 OK` | File uploaded successfully |
| `400 Bad Request` | Invalid `path`, malformed request, or missing `UploadFiles` |
| `401 Unauthorized` | Missing, expired, or invalid JWT token |
| `403 Forbidden` | Insufficient permissions for target storage |
| `500 Internal Server Error` | Unexpected server-side failure |

---

### **How to Use the Upload File API**

#### **cURL Example**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/input/Report.xlsx?storageName=MyStorage" \
  -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -H "Content-Type: multipart/form-data" \
  -F "UploadFiles=@/local/path/Report.xlsx"
```

#### **Response Example**

```json
{
  "Uploaded": ["Report.xlsx"],
  "Errors": []
}
```

---

### **SDK Examples**

Using Aspose.Cells Cloud SDKs simplifies authentication, error handling, and request construction.

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
```csharp
// Aspose.Cells Cloud SDK for C# v24.6.0
var cellsApi = new CellsApi(clientId, clientSecret);
using var fileStream = File.OpenRead("Report.xlsx");
var response = await cellsApi.UploadFile("input/Report.xlsx", fileStream, "MyStorage");
Console.WriteLine($"Uploaded: {string.Join(", ", response.Uploaded)}");
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```java
// Aspose.Cells Cloud SDK for Java v24.6
CellsApi cellsApi = new CellsApi(clientId, clientSecret);
File file = new File("Report.xlsx");
FilesUploadResult result = cellsApi.uploadFile("input/Report.xlsx", file, "MyStorage");
System.out.println("Uploaded: " + result.getUploaded());
```
{{< /tab >}}
{{< tab tabNum="3" >}}
```php
// Aspose.Cells Cloud SDK for PHP v24.6
$cellsApi = new CellsApi($clientId, $clientSecret);
$file = fopen("Report.xlsx", "r");
$result = $cellsApi->uploadFile("input/Report.xlsx", $file, "MyStorage");
echo "Uploaded: " . implode(", ", $result->Uploaded);
```
{{< /tab >}}
{{< tab tabNum="4" >}}
```ruby
# Aspose.Cells Cloud SDK for Ruby v24.6
cells_api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
file = File.open("Report.xlsx", "rb")
result = cells_api.upload_file("input/Report.xlsx", file, storage_name: "MyStorage")
puts "Uploaded: #{result.uploaded.join(', ')}"
```
{{< /tab >}}
{{< tab tabNum="5" >}}
```typescript
// Aspose.Cells Cloud SDK for Node.js v24.6
const cellsApi = new CellsApi(clientId, clientSecret);
const fileStream = fs.createReadStream("Report.xlsx");
const response = await cellsApi.uploadFile("input/Report.xlsx", fileStream, "MyStorage");
console.log(`Uploaded: ${response.body.uploaded.join(', ')}`);
```
{{< /tab >}}
{{< tab tabNum="6" >}}
```python
# Aspose.Cells Cloud SDK for Python v24.6
api = CellsApi(client_id, client_secret)
with open("Report.xlsx", "rb") as f:
    response = api.upload_file("input/Report.xlsx", f, storage_name="MyStorage")
print(f"Uploaded: {', '.join(response.uploaded)}")
```
{{< /tab >}}
{{< tab tabNum="7" >}}
```perl
# Aspose.Cells Cloud SDK for Perl v24.6
my $cells_api = AsposeCellsCloud::API::CellsApi->new(
    client_id => $client_id,
    client_secret => $client_secret
);
my $file = IO::File->new("Report.xlsx", "r");
my $result = $cells_api->upload_file("input/Report.xlsx", $file, storage_name => "MyStorage");
print "Uploaded: " . join(", ", @{$result->uploaded});
```
{{< /tab >}}
{{< tab tabNum="8" >}}
```go
// Aspose.Cells Cloud SDK for Go v24.6
api := cells.NewCellsApi(clientId, clientSecret)
file, _ := os.Open("Report.xlsx")
defer file.Close()
result, _, err := api.UploadFile("input/Report.xlsx", file, "MyStorage")
fmt.Printf("Uploaded: %v\n", result.Uploaded)
```
{{< /tab >}}
{{< /tabs >}}

> ℹ️ **Note**: All SDK examples above assume v24.6.0. Update to the latest version via [GitHub](https://github.com/aspose-cells-cloud).

---

### **Advanced Notes**

- **Overwrite Behavior**: Existing files at the target path are silently overwritten. To avoid accidental overwrites, use unique paths or check file existence first.
- **Multipart Handling**: Ensure your client sends `Content-Type: multipart/form-data` with the file as field `UploadFiles`.
- **Storage Selection**: Specify `storageName` to target a specific cloud storage (e.g., `MyStorage`) instead of the default.
- **Error Handling**: Inspect the `Errors` array in the response for partial failures (e.g., multi-file uploads).

---

### **Visual Overview**

![Upload File Flow](https://docs.aspose.cloud/cells/upload-flow.svg)  
*Client → JWT Auth → UploadFile Endpoint → Cloud Storage*

---

### **See Also**

- [Download File API](https://docs.aspose.cloud/cells/download-file/)  
- [Copy File API](https://docs.aspose.cloud/cells/copy-file/)  
- [Delete File API](https://docs.aspose.cloud/cells/delete-file/)  
- [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/UploadFile)  
- [Authentication Guide](https://docs.aspose.cloud/cells/getting-started/rest-api-overview/authenticating-api-requests/)  

---

> 📝 **Last Updated**: 2024-06-20  
> ⚙️ **API Version**: v4.0  
> 🛠️ **SDK Version**: 24.6.0