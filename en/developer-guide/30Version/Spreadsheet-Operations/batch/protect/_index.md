---
title: "Batch Protect Excel Files"
second_title: "Document"
description: "Protect multiple Excel files in bulk using Aspose.Cells Cloud REST API. Support for regex and exact name matching, password protection, and output folder configuration. Includes cURL and SDK examples for C#, Java, Python, Node.js, PHP, Ruby, Perl, and Go."
keywords: "batch protect Excel files, Aspose.Cells Cloud API, Excel protection, workbook encryption, REST API, batch file protection, regex file matching, password-protected Excel"
url: /batch/protect
type: docs
weight: 100
lastmod: "2024-05-22"
date: 2024-03-15
aliases:
  - /cells/batch-protect-excel-files/
  - /cells/workbook/batch-protection/
---

## Batch Protect Excel Files via REST API

Aspose.Cells Cloud’s **batch protection API** enables you to apply consistent security settings to multiple Excel files in a single request. Using flexible matching criteria—including regular expressions and exact file names—you can selectively protect files based on naming patterns. Supported protection types include full encryption (All), read-only locking (ReadOnly), and more. Protected files are saved to a designated output folder, preserving the original files.

This API supports 30+ file formats (Excel, CSV, PDF, Markdown, JSON, XML, HTML, and more) and provides SDKs for C#, Java, Python, Node.js, PHP, Ruby, Perl, and Go.

---

### REST API Endpoint

```http
POST https://api.aspose.cloud/v3.0/cells/batch/protect
```

#### Base URL

| Environment | Base URL |
|-------------|----------|
| Production  | `https://api.aspose.cloud/v3.0/cells/batch/protect` |
| Sandbox     | `https://testapi.aspose.cloud/v3.0/cells/batch/protect` |

> **Note**: All requests require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Obtain your `Client ID` and `Client Secret` from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

---

### Request Parameters

The request body must contain a `BatchProtectRequest` object.

| Parameter Name        | Type                | Location | Required | Description |
|-----------------------|---------------------|----------|----------|-------------|
| `batchProtectRequest` | `BatchProtectRequest` | Body     | ✅ Yes   | JSON payload defining source folder, file selection criteria, protection settings, and output location. |

#### `BatchProtectRequest` Properties

| Field            | Type                     | Required | Description |
|------------------|--------------------------|----------|-------------|
| `SourceFolder`   | `string`                 | ❌ No    | Cloud storage folder containing source files (e.g., `"CellsTests"`). Defaults to root if omitted. |
| `MatchCondition` | `MatchConditionRequest` | ❌ No    | Criteria to select files (regex or exact name matches). If omitted, *all* `.xlsx`/`.xls` files in `SourceFolder` are protected. |
| `ProtectionType` | `string`                 | ❌ No    | Type of protection: `"All"` (full encryption), `"ReadOnly"` (lock editing), `"Structure"` (lock sheet structure), `"Windows"` (lock window size/position). Default: `"All"`. |
| `Password`       | `string`                 | ❌ No    | Password to apply for protected files. If omitted, no password is set (use with caution). |
| `OutFolder`      | `string`                 | ❌ No    | Cloud storage folder where protected files are saved. Defaults to `SourceFolder` if omitted. |

#### `MatchConditionRequest` Properties

| Field               | Type       | Required | Description |
|---------------------|------------|----------|-------------|
| `RegexPattern`      | `string`   | ❌ No    | Regular expression to match file names (case-insensitive). Example: `"^Book\d+\.xlsx$"` matches `Book1.xlsx`, `Book123.xlsx`, etc. |
| `FullMatchConditions` | `string[]` | ❌ No    | List of exact file names to protect (e.g., `["Report.xlsx", "Summary.xlsx"]`). |

> **Tip**: Combine `RegexPattern` and `FullMatchConditions` for complex selection logic (files matching *either* condition are selected).

---

### Request Body Example

```json
{
  "SourceFolder": "input_files",
  "MatchCondition": {
    "RegexPattern": "^(Sales|Inventory).+\\.xlsx$",
    "FullMatchConditions": ["Template.xlsx"]
  },
  "ProtectionType": "All",
  "Password": "123456",
  "OutFolder": "protected_output"
}
```

This example protects all `.xlsx` files in `input_files` matching `Sales*.xlsx`, `Inventory*.xlsx`, or exactly `Template.xlsx`, applies full encryption with password `123456`, and saves results to `protected_output`.

---

### Response

#### Success Response (HTTP 200 OK)

```json
{
  "Code": 200,
  "Status": "Files processed successfully"
}
```

#### Error Responses

| Code | Meaning             | Cause |
|------|---------------------|-------|
| 400  | Bad Request         | Invalid JSON, missing required fields, or unsupported `ProtectionType`. |
| 401  | Unauthorized        | Missing, expired, or invalid JWT token. |
| 409  | Conflict            | Output file exists and `isWriteOver` is `false` (not applicable here but included for completeness). |
| 422  | Unprocessable Entity | `SourceFolder` or `OutFolder` does not exist, or no files match the `MatchCondition`. |

> **Note**: A 200 response confirms *processing completion* but does not guarantee *all files were protected*. Check logs or use the [Batch Status API](https://docs.aspose.cloud/cells/batch-status/) for per-file results.

---

### cURL Example

```bash
# Step 1: Get JWT token
TOKEN=$(curl -v "https://api.aspose.cloud/connect/token" \
  -X POST \
  -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -s | jq -r '.access_token')

# Step 2: Submit batch protect request
curl -v "https://api.aspose.cloud/v3.0/cells/batch/protect" \
  -X POST \
  -H "Authorization: Bearer $TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "SourceFolder": "CellsTests",
    "OutFolder": "Output",
    "MatchCondition": {
      "RegexPattern": "(^Book)(.+)(xlsx$)"
    },
    "Password": "123456",
    "ProtectionType": "All"
  }' \
  -o response.json
```

---

### SDK Code Examples

Using an SDK is the recommended approach for production integrations. SDKs handle authentication, serialization, and error handling.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Install-Package Aspose.Cells-Cloud -Version 22.8.0

using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var configuration = new Configuration
{
    AppSid = "YOUR_CLIENT_ID",
    AppKey = "YOUR_CLIENT_SECRET"
};

var cellsApi = new CellsApi(configuration);

var matchCondition = new MatchConditionRequest
{
    RegexPattern = "^Book.+\\.xlsx$"
};

var batchRequest = new BatchProtectRequest
{
    SourceFolder = "CellsTests",
    OutFolder = "Output",
    MatchCondition = matchCondition,
    Password = "123456",
    ProtectionType = "All"
};

var response = await cellsApi.PostBatchProtect(batchRequest);
Console.WriteLine($"Status: {response.Code}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Maven: <dependency>
//   <groupId>com.aspose</groupId>
//   <artifactId>aspose-cells-cloud</artifactId>
//   <version>22.8.0</version>
// </dependency>

import com.aspose.cells.cloud.*;
import com.aspose.cells.cloud.model.*;

ApiClient apiClient = new ApiClient();
apiClient.setAppSid("YOUR_CLIENT_ID");
apiClient.setAppKey("YOUR_CLIENT_SECRET");

CellsApi cellsApi = new CellsApi(apiClient);

MatchConditionRequest matchCondition = new MatchConditionRequest();
matchCondition.setRegexPattern("^Book.+\\.xlsx$");

BatchProtectRequest request = new BatchProtectRequest();
request.setSourceFolder("CellsTests");
request.setOutFolder("Output");
request.setMatchCondition(matchCondition);
request.setPassword("123456");
request.setProtectionType("All");

ApiResponse response = cellsApi.postBatchProtect(request, null, null);
System.out.println("Status: " + response.getMessage());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// composer require aspose-cells-cloud/aspose-cells-cloud-php

require_once 'vendor/autoload.php';

use Aspose\Cells\CellsApi;
use Aspose\Cells\Model\MatchConditionRequest;
use Aspose\Cells\Model\BatchProtectRequest;

$client = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

$matchCondition = new MatchConditionRequest();
$matchCondition->setRegexPattern("^Book.+\\.xlsx$");

$request = new BatchProtectRequest();
$request->setSourceFolder("CellsTests");
$request->setOutFolder("Output");
$request->setMatchCondition($matchCondition);
$request->setPassword("123456");
$request->setProtectionType("All");

$response = $client->postBatchProtect($request);
echo "Status: " . $response->getCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# gem install aspose_cells_cloud

require 'aspose_cells_cloud'

AsposeCellsCloud.configure do |config|
  config.app_sid = "YOUR_CLIENT_ID"
  config.app_key = "YOUR_CLIENT_SECRET"
end

api = AsposeCellsCloud::CellsApi.new

matchCondition = AsposeCellsCloud::MatchConditionRequest.new(
  regex_pattern: "^Book.+\\.xlsx$"
)

request = AsposeCellsCloud::BatchProtectRequest.new(
  source_folder: "CellsTests",
  out_folder: "Output",
  match_condition: matchCondition,
  password: "123456",
  protection_type: "All"
)

response = api.post_batch_protect(request)
puts "Status: #{response.code}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// npm install aspose-cells-cloud --save

const { CellsApi, MatchConditionRequest, BatchProtectRequest } = require("aspose-cells-cloud");

const client = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

const matchCondition = new MatchConditionRequest({
  regexPattern: "^Book.+\\.xlsx$"
});

const request = new BatchProtectRequest({
  sourceFolder: "CellsTests",
  outFolder: "Output",
  matchCondition: matchCondition,
  password: "123456",
  protectionType: "All"
});

client.postBatchProtect(request)
  .then(res => console.log(`Status: ${res.code}`))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# pip install asposecellscloud

from asposecellscloud.api import CellsApi
from asposecellscloud.models import MatchConditionRequest, BatchProtectRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

matchCondition = MatchConditionRequest(
    regex_pattern="^Book.+\\.xlsx$"
)

request = BatchProtectRequest(
    source_folder="CellsTests",
    out_folder="Output",
    match_condition=matchCondition,
    password="123456",
    protection_type="All"
)

response = api.post_batch_protect(batch_protect_request=request)
print(f"Status: {response.code}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new(
  app_sid => "YOUR_CLIENT_ID",
  app_key => "YOUR_CLIENT_SECRET"
);

my $api = AsposeCellsCloud::CellsApi->new(config => $config);

my $matchCondition = AsposeCellsCloud::Object::MatchConditionRequest->new(
  regex_pattern => "^Book.+\\.xlsx$"
);

my $request = AsposeCellsCloud::Object::BatchProtectRequest->new(
  source_folder => "CellsTests",
  out_folder => "Output",
  match_condition => $matchCondition,
  password => "123456",
  protection_type => "All"
);

my $response = $api->post_batch_protect(batch_protect_request => $request);
print "Status: " . $response->{code} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// go get github.com/aspose-cells-cloud/aspose-cells-cloud-go

import (
  "context"
  "fmt"
  cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)

config := cells.NewConfiguration()
config.AppSid = "YOUR_CLIENT_ID"
config.AppKey = "YOUR_CLIENT_SECRET"

client := cells.NewCellsApiClient(config.Context)

matchCondition := &cells.MatchConditionRequest{
  RegexPattern: cells.String("^Book.+\\.xlsx$"),
}

request := &cells.BatchProtectRequest{
  SourceFolder:    cells.String("CellsTests"),
  OutFolder:       cells.String("Output"),
  MatchCondition:  matchCondition,
  Password:        cells.String("123456"),
  ProtectionType:  cells.String("All"),
}

response, _, err := client.PostBatchProtect(context.Background(), request)
if err != nil {
  panic(err)
}
fmt.Printf("Status: %s\n", *response.Code)
```

{{< /tab >}}

{{< /tabs >}}

---

### Best Practices

1. **Use Specific Patterns**  
   Avoid overly broad regex (e.g., `.*`) that might accidentally match unintended files. Test patterns in a sandbox first.

2. **Secure Passwords**  
   Never hardcode passwords in code. Use environment variables or a secrets manager.

3. **Output Folder Isolation**  
   Always specify `OutFolder` to avoid overwriting originals.

4. **Error Handling**  
   Log responses to detect partial failures (e.g., some files skipped due to corruption).

5. **File Format Support**  
   While Aspose.Cells Cloud supports 30+ formats, batch protection is optimized for Excel formats (`.xlsx`, `.xls`, `.xlsm`, `.xlsb`). Use dedicated endpoints for non-Excel formats.

---

### Related Resources

- [Encrypt, Decrypt, and Digitally Sign Excel Files](https://docs.aspose.cloud/cells/protect/)  
- [Batch Merge Excel Files](https://docs.aspose.cloud/cells/batch/merge/)  
- [Batch Convert Excel Files](https://docs.aspose.cloud/cells/batch/convert/)  
- [Aspose.Cells Cloud SDKs on GitHub](https://github.com/aspose-cells-cloud)  

> **Last updated**: May 22, 2024