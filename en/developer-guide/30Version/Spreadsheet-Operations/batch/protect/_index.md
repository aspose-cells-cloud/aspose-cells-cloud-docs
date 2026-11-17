---
title: "Batch Protect Excel Files"
second_title: "Developer Guide"
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
linktitle: "Batch Protect Excel Files"
ArticleTitle: "Batch Protect Excel Files with Aspose.Cells Cloud REST API"
---

The **PostBatchProtect** API (`POST https://api.aspose.cloud/v3.0/cells/batch/protect`) enables Aspose.Cells Cloud users to apply consistent security settings—such as full encryption or read-only locking—to multiple Excel files in a single request, using flexible matching criteria like regular expressions or exact filenames to selectively target files for protection while preserving originals and saving results to a designated output folder.

## The Post Batch Protect Web API

```http
POST https://api.aspose.cloud/v3.0/cells/batch/protect
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name      | Type                      | Path/Query String/HTTPBody | Description                                        |
| ------------------- | ------------------------- | -------------------------- | -------------------------------------------------- |
| batchProtectRequest | class:batchprotectrequest | HTTPBody                   | BatchProtectRequest Batch protection file request. |

The request body must contain a `BatchProtectRequest` object.

#### `BatchProtectRequest` Properties

| Field            | Type                    | Required | Description                                                                                                                                                                  |
| ---------------- | ----------------------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `SourceFolder`   | `string`                | ❌ No    | Cloud storage folder containing source files (e.g., `"CellsTests"`). Defaults to root if omitted.                                                                            |
| `MatchCondition` | `MatchConditionRequest` | ❌ No    | Criteria to select files (regex or exact name matches). If omitted, _all_ `.xlsx`/`.xls` files in `SourceFolder` are protected.                                              |
| `ProtectionType` | `string`                | ❌ No    | Type of protection: `"All"` (full encryption), `"ReadOnly"` (lock editing), `"Structure"` (lock sheet structure), `"Windows"` (lock window size/position). Default: `"All"`. |
| `Password`       | `string`                | ❌ No    | Password to apply for protected files. If omitted, no password is set (use with caution).                                                                                    |
| `OutFolder`      | `string`                | ❌ No    | Cloud storage folder where protected files are saved. Defaults to `SourceFolder` if omitted.                                                                                 |

#### `MatchConditionRequest` Properties

| Field                 | Type       | Required | Description                                                                                                                        |
| --------------------- | ---------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `RegexPattern`        | `string`   | ❌ No    | Regular expression to match file names (case-insensitive). Example: `"^Book\d+\.xlsx$"` matches `Book1.xlsx`, `Book123.xlsx`, etc. |
| `FullMatchConditions` | `string[]` | ❌ No    | List of exact file names to protect (e.g., `["Report.xlsx", "Summary.xlsx"]`).                                                     |

> **Tip**: Combine `RegexPattern` and `FullMatchConditions` for complex selection logic (files matching _either_ condition are selected).

---

### Response

```json
[
  {
    "Name": "Stream",
    "DataType": {
      "Identifier": "File"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning               | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | The request completed successfully.                                      |
| 400  | Bad Request           | The request is malformed or one or more parameters are invalid.          |
| 401  | Unauthorized          | Authentication failed, or the JWT token is missing or expired.           |
| 404  | Not Found             | The requested workbook, worksheet, or resource was not found.            |
| 413  | Payload Too Large     | The uploaded file exceeds the allowed size limit.                        |
| 500  | Internal Server Error | The server encountered an unexpected error while processing the request. |

## How to Use the Post Batch Protect API with SDKs?

### Post Batch Protect API Specification

The <a href="https://reference.aspose.cloud/cells/#/Batch/PostBatchProtect" rel="noopener noreferrer">Post Batch Protect API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

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

const {
  CellsApi,
  MatchConditionRequest,
  BatchProtectRequest,
} = require("aspose-cells-cloud");

const client = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

const matchCondition = new MatchConditionRequest({
  regexPattern: "^Book.+\\.xlsx$",
});

const request = new BatchProtectRequest({
  sourceFolder: "CellsTests",
  outFolder: "Output",
  matchCondition: matchCondition,
  password: "123456",
  protectionType: "All",
});

client
  .postBatchProtect(request)
  .then((res) => console.log(`Status: ${res.code}`))
  .catch((err) => console.error(err));
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

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}
{{</tab>}}
{{< /tabs >}}
