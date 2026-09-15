---
title: Replace Text in Excel Files
second_title: "Document"
linktitle: "Replace text without using storage"
type: docs
url: /replace/
keywords: "excel text replacement, aspose.cells cloud api, rest api example, c# excel automation, spreadsheet text find replace, replace text in excel"
description: "Replace specified text with new text in Excel files using Aspose.Cells Cloud REST API. Supports cURL, SDKs for C#, Java, Python, Node.js, PHP, Ruby, Go, and Perl. Secure JWT-authenticated processing with optional worksheet targeting."
date: 2024-03-15T10:00:00Z
lastmod: 2024-05-20T14:30:00Z
weight: 80
---

## Replace Text in Excel Files

Replace specified text with new text in Excel files using Aspose.Cells Cloud REST API. This operation supports multiple files in a single request, optional worksheet targeting, and password-protected workbooks. All API calls require JWT token-based authentication.

{{< figure
  src="https://docs.aspose.cloud/cells/images/sdk-icon.png"
  alt="Aspose.Cells Cloud SDK for Excel logo"
  caption="Aspose.Cells Cloud text replacement workflow"
>}}

## REST API Endpoint

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### Security and Authentication

All Aspose.Cells Cloud APIs require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Ensure your request includes a valid `Authorization: Bearer <jwt_token>` header.

---

## Request Parameters

| Parameter Name          | Type    | Location             | Required | Description                                                                 |
|-------------------------|---------|----------------------|----------|-----------------------------------------------------------------------------|
| **file**                | file    | formData (multipart) | Yes      | Excel file(s) to process. Multiple files can be uploaded in one request.   |
| **text**                | string  | query                | Yes      | Text string to locate and replace.                                          |
| **newtext**             | string  | query                | Yes      | Replacement text.                                                           |
| **password**            | string  | query                | No       | Password for protected workbooks (optional).                               |
| **sheetname**           | string  | query                | No       | Target worksheet name. If omitted, search occurs across all visible sheets.|
| **checkExcelRestriction**| boolean| query                | No       | Whether to enforce Excel cell modification restrictions. Default: `true`.  |

---

## Response Format

The API returns a `FilesResult` object containing the processed files:

```json
{
  "Files": [
    {
      "Filename": "[filename].xlsx",
      "FileSize": 274022,
      "FileContent": "UEsDBBQABgAIAAAAIQDf...[Base64-encoded XLSX content]..."
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                                 |
|------|-----------------------|-----------------------------------------------------------------------------|
| 200  | OK                    | Replacement completed successfully. Response includes updated file(s).      |
| 400  | Bad Request           | Missing required parameters, invalid file format, or malformed request.    |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token.                                     |
| 413  | Payload Too Large     | Total uploaded file size exceeds the 2 GB limit.                            |
| 500  | Internal Server Error | Unexpected server-side failure during processing.                           |

---

## Using the API

### cURL Example

Replace "1" with "aspose.cells.cloud" in two Excel files:

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <valid_jwt_token>" \
  -F 'file1=@/path/to/file1.xlsx' \
  -F 'file2=@/path/to/file2.xlsx'
```

### SDK Integration

Aspose.Cells Cloud SDKs reduce boilerplate code for authentication, request signing, and response parsing. Below are code examples for major languages. All examples use **v24.5** of the respective SDKs.

{{< tabs tabTotal="8" tabID="sdk-tabs" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Aspose.Cells Cloud SDK for .NET v24.5
// Example: Replace text in Excel files

var config = new Configuration { ClientId = "your_client_id", ClientSecret = "your_client_secret" };
var cellsApi = new CellsApi(config);

// Replace "1" with "aspose.cells.cloud" in file1.xlsx
var response = cellsApi.PostReplace("file1.xlsx", "1", "aspose.cells.cloud");
Console.WriteLine($"Replaced text in {response.Files[0].Filename}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Aspose.Cells Cloud SDK for Java v24.5
// Example: Replace text in Excel files

ApiClient client = new ApiClient("your_client_id", "your_client_secret", null);
CellsApi cellsApi = new CellsApi(client);

String filename = "file1.xlsx";
String text = "1";
String newtext = "aspose.cells.cloud";

FilesResult result = cellsApi.postReplace(filename, text, newtext, null, null, null);
System.out.println("Replaced text in: " + result.getFiles().get(0).getFilename());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Aspose.Cells Cloud SDK for PHP v24.5
// Example: Replace text in Excel files

require_once("vendor/autoload.php");

use Aspose\Cells\CellsApi;
use Aspose\Cells\ApiClient;

$clientId = "your_client_id";
$clientSecret = "your_client_secret";
$apiKey = "your_api_key";

$cellsApi = new CellsApi($clientId, $clientSecret);

$response = $cellsApi->postReplace("file1.xlsx", "1", "aspose.cells.cloud");
echo "Replaced text in: " . $response->getFiles()[0]->getFilename() . "\n";
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Aspose.Cells Cloud SDK for Ruby v24.5
# Example: Replace text in Excel files

require 'aspose_cells_cloud'

configure do |config|
  config.client_id = 'your_client_id'
  config.client_secret = 'your_client_secret'
end

api_instance = AsposeCellsCloud::CellsApi.new
filename = 'file1.xlsx'
text = '1'
newtext = 'aspose.cells.cloud'

response = api_instance.post_replace(filename, text, newtext)
puts "Replaced text in: #{response.files.first.filename}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```typescript
// Aspose.Cells Cloud SDK for Node.js v24.5
// Example: Replace text in Excel files

import { CellsApi, Configuration } from '@aspose/cells-cloud';

const config = new Configuration({
  clientId: 'your_client_id',
  clientSecret: 'your_client_secret'
});
const cellsApi = new CellsApi(config);

const response = await cellsApi.postReplace('file1.xlsx', '1', 'aspose.cells.cloud');
console.log(`Replaced text in: ${response.data.files[0].filename}`);
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Aspose.Cells Cloud SDK for Python v24.5
# Example: Replace text in Excel files

from asposecellscloud.api import cells_api
from asposecellscloud.configuration import Configuration

config = Configuration()
config.client_id = "your_client_id"
config.client_secret = "your_client_secret"

api = cells_api.CellsApi(config)
response = api.post_replace(
    name="file1.xlsx",
    text="1",
    new_text="aspose.cells.cloud"
)
print(f"Replaced text in: {response.files[0].filename}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Aspose.Cells Cloud SDK for Perl v24.5
# Example: Replace text in Excel files

use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new(
  client_id => 'your_client_id',
  client_secret => 'your_client_secret'
);
my $api = AsposeCellsCloud::CellsApi->new(config => $config);

my $filename = 'file1.xlsx';
my $text = '1';
my $newtext = 'aspose.cells.cloud';

my $response = $api->post_replace(
  name => $filename,
  text => $text,
  newtext => $newtext
);
print "Replaced text in: " . $response->{files}[0]{filename} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Aspose.Cells Cloud SDK for Go v24.5
// Example: Replace text in Excel files

package main

import (
  "context"
  "fmt"
  "os"
  "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v24.5/api"
  "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v24.5/client"
)

func main() {
  cfg := client.NewConfiguration()
  cfg.AppKey = "your_client_id"
  cfg.AppSid = "your_client_secret"
  
  api := api.NewCellsApiWithClientConfiguration(cfg)
  
  fileName := "file1.xlsx"
  text := "1"
  newText := "aspose.cells.cloud"
  
  resp, _, err := api.PostReplace(context.Background(), fileName, text, newText, nil, nil, nil)
  if err != nil {
    fmt.Fprintf(os.Stderr, "Error: %v\n", err)
    os.Exit(1)
  }
  
  fmt.Printf("Replaced text in: %s\n", *resp.Files[0].Filename)
}
```

{{< /tab >}}

{{< /tabs >}}

For full SDK examples and documentation, visit the [Aspose.Cells Cloud GitHub Repository](https://github.com/aspose-cells-cloud).

---

## Best Practices

- **Use specific `sheetname`** to avoid unintended replacements across multiple sheets.
- **Test in a non-production environment** first—especially when `checkExcelRestriction` is `false`.
- **Validate `newtext` length**—extremely long replacements may alter cell formatting unexpectedly.
- **Include `checkExcelRestriction=true`** unless you explicitly need to bypass Excel’s cell protection rules.

---

## Related Resources

- [Aspose.Cells Cloud SDKs Overview](https://docs.aspose.cloud/total/sdk/)
- [OpenAPI Specification for PostReplace](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace)
- [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)