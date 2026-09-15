---
title: "Download File API (v4.0)"
linktitle: "Download File API"
type: docs
url: /download-file/
keywords: "Aspose.Cells, Download File API, Excel cloud storage, REST API, file download, PDF, CSV, SDK"
description: "Download files (Excel, PDF, CSV) from Aspose.Cells Cloud storage via REST API. Includes cURL & SDK examples (C#, Java, Python, etc.), authentication, and response handling."
date: 2024-05-10
lastmod: 2024-06-14
weight: 100
---

# Download File API (v4.0)

The **DownloadFile** API enables you to retrieve files stored in Aspose.Cells Cloud storage. Use this endpoint to download Excel spreadsheets, PDFs, CSVs, and other supported formats directly from the cloud.

## Excel API: Download File

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/){:target="\_blank" rel="noopener noreferrer"}.

Include your access token in the `Authorization` header:

```bash
-H "Authorization: Bearer {YOUR_ACCESS_TOKEN}"
```

### Request Parameters

| Parameter Name | Type     | Location | Required | Description                                                                                                                         |
| -------------- | -------- | -------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `path`         | `string` | Path     | ✅ Yes   | The virtual path to the file in cloud storage (e.g., `input/Report.xlsx`).                                                          |
| `storageName`  | `string` | Query    | ❌ No    | The name of the storage (e.g., `MyStorage`). Defaults to the first configured storage if omitted.                                   |
| `versionId`    | `string` | Query    | ❌ No    | Optional version identifier for versioned storage (e.g., `v1.2`). Use only when multiple file versions exist in enterprise storage. |

### Response

The API returns a **binary file stream**. The `Content-Type` header matches the file format (e.g., `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` for XLSX, `application/pdf` for PDF, `text/csv` for CSV). No JSON payload is returned.

#### HTTP Status Codes

| Code  | Meaning               | Description                                                                    |
| ----- | --------------------- | ------------------------------------------------------------------------------ |
| `200` | OK                    | File downloaded successfully; response body contains the binary file stream.   |
| `400` | Bad Request           | Missing or invalid parameters (e.g., unsupported file type, malformed `path`). |
| `401` | Unauthorized          | Invalid, expired, or missing JWT token.                                        |
| `404` | Not Found             | File not found at the specified `path` or `storageName` does not exist.        |
| `413` | Payload Too Large     | Requested file exceeds maximum download size (1 GB).                           |
| `500` | Internal Server Error | Unexpected server error.                                                       |

### Example: cURL Command

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/input/Report.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer {YOUR_ACCESS_TOKEN}" \
     -H "Accept: application/octet-stream" \
     -o Report.xlsx
```

> ✅ Tip: Replace `{YOUR_ACCESS_TOKEN}` with your actual JWT access token. Ensure the `path` matches the file’s virtual location in storage.

---

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. SDKs handle low-level details like authentication, request formatting, and error handling, enabling you to focus on business logic.

Check out the [GitHub repository](https://github.com/aspose-cells-cloud){:target="\_blank" rel="noopener noreferrer"} for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to download a file using various SDKs:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}

```csharp
// Aspose.Cells Cloud SDK v23.5 for .NET
var config = new Configuration { ClientId = "your_client_id", ClientSecret = "your_client_secret" };
var apiInstance = new FileController(config);

string path = "input/Report.xlsx";
string storageName = "MyStorage";

var response = apiInstance.DownloadFile(path, storageName: storageName);
// Save to local file
System.IO.File.WriteAllBytes("Report.xlsx", response);
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```java
// Aspose.Cells Cloud SDK v23.5 for Java
Configuration config = new Configuration("your_client_id", "your_client_secret");
FileApi api = new FileApi(config);

String path = "input/Report.xlsx";
String storageName = "MyStorage";

File response = api.downloadFile(path, storageName, null, null);
System.out.println("File downloaded to: " + response.getAbsolutePath());
```

{{< /tab >}}
{{< tab tabNum="3" >}}

```php
// Aspose.Cells Cloud SDK v23.5 for PHP
$config = new Configuration();
$config->setClientId("your_client_id");
$config->setClientSecret("your_client_secret");
$api = new FileApi($config);

$path = "input/Report.xlsx";
$storageName = "MyStorage";

$response = $api->downloadFile($path, $storageName);
file_put_contents("Report.xlsx", $response);
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```ruby
# Aspose.Cells Cloud SDK v23.5 for Ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = 'your_client_id'
config.client_secret = 'your_client_secret'
api_instance = AsposeCellsCloud::FileApi.new(config)

path = 'input/Report.xlsx'
storage_name = 'MyStorage'

response = api_instance.download_file(path, storage_name: storage_name)
File.write('Report.xlsx', response)
```

{{< /tab >}}
{{< tab tabNum="5" >}}

```typescript
// Aspose.Cells Cloud SDK v23.5 for Node.js (TypeScript)
import { FileApi } from "@aspose/cells-cloud";
import { Configuration } from "@aspose/cells-cloud";

const config = new Configuration({
  clientId: "your_client_id",
  clientSecret: "your_client_secret",
});
const api = new FileApi(config);

const path = "input/Report.xlsx";
const storageName = "MyStorage";

const response = await api.downloadFile(path, storageName);
import * as fs from "fs";
fs.writeFileSync("Report.xlsx", Buffer.from(response.data as string));
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```python
# Aspose.Cells Cloud SDK v23.5 for Python
from asposecellscloud.configuration import Configuration
from asposecellscloud.api_client import FileApi

config = Configuration(
    client_id="your_client_id",
    client_secret="your_client_secret"
)
api = FileApi(config)

path = "input/Report.xlsx"
storage_name = "MyStorage"

response = api.download_file(path, storage_name=storage_name)
with open("Report.xlsx", "wb") as f:
    f.write(response.content)
```

{{< /tab >}}
{{< tab tabNum="7" >}}

```perl
# Aspose.Cells Cloud SDK v23.5 for Perl
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::FileApi;

my $config = AsposeCellsCloud::Configuration->new(
    client_id => 'your_client_id',
    client_secret => 'your_client_secret'
);
my $api = AsposeCellsCloud::FileApi->new(config => $config);

my $path = 'input/Report.xlsx';
my $storage_name = 'MyStorage';

my $response = $api->download_file($path, { storage_name => $storage_name });
open(my $fh, '>', 'Report.xlsx') or die "Could not open file: $!";
print $fh $$response;
close $fh;
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```go
// Aspose.Cells Cloud SDK v23.5 for Go
import (
    "context"
    "io"
    "os"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v23.5/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v23.5/model"
)

config := &api.Config{
    ClientID: "your_client_id",
    ClientSecret: "your_client_secret",
}
apiInstance := api.NewFileApi(config)

path := "input/Report.xlsx"
storageName := "MyStorage"

response, _, err := apiInstance.DownloadFile(context.Background(), path).
    StorageName(storageName).Execute()
if err != nil {
    panic(err)
}
f, _ := os.Create("Report.xlsx")
defer f.Close()
io.Copy(f, response)
```

{{< /tab >}}
{{< /tabs >}}

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) defines a publicly accessible programming interface for this operation.

You can interact directly with the API using tools like Postman or Swagger UI.

---

### Architecture Overview

![Aspose.Cells Cloud file download architecture](https://docs.aspose.cloud/download/flow-download.png){:width="600" alt="Architecture diagram: Client → API Gateway → Cloud Storage → Binary File Stream"}
