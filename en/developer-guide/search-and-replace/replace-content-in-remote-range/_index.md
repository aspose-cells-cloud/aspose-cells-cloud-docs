---
title: "Aspose.Cells Cloud Replace Web API – Update Text in Remote Spreadsheet Range"
second_title: "Document"
ArticleTitle: "Bulk Range Text Replacement in Cloud Excel Files – Find & Replace API"
linktitle: "Replace Remote Range Content"
type: docs
url: /replace-content-in-remote-range/
keywords: "replace text remote excel range, Aspose.Cells Cloud API, find and replace Excel, cloud spreadsheet edit, remote Excel file update"
description: "Use Aspose.Cells Cloud to find and replace text in a specific range of a remote Excel file. Supports authentication, error handling, and multi‑language SDKs."
weight: 100
---

Perform bulk text replacement across remote Excel files stored in the cloud. Find and update specific text strings within selected ranges efficiently using Aspose.Cells Find and Replace API.

## Security and Authentication
The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## **Replace Content in Remote Range API**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Request Parameters**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                                                                                                                 |
| :------------- | :----- | :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | The name of the workbook file stored in cloud storage to be modified (e.g., `"report.xlsx"`).                                                               |
| searchText     | String | Query                       | The text string to search for within the specified worksheet and cell area. Supports exact text matching.                                                   |
| replaceText    | String | Query                       | The text string that will replace all occurrences of the `searchText` within the specified range.                                                           |
| worksheet      | String | Path                        | The name of the worksheet where the find‑and‑replace operation will be performed.                                                                           |
| cellArea       | String | Path                        | The specific cell range (e.g., `"A1:D20"`) where the text search and replacement will occur.                                                                |
| folder         | String | Query                       | The cloud storage folder path where the source workbook is located.                                                                                         |
| storageName    | String | Query                       | _(Optional)_ The name of the cloud storage where the workbook resides. If omitted, the default cloud storage is used.                                       |
| region         | String | Query                       | _(Optional)_ Sets the locale for text handling, which may affect case sensitivity and character encoding in search operations (e.g., `"en-US"`, `"tr-TR"`). |
| password       | String | Query                       | _(Optional)_ If the workbook is password‑protected, provide the password to open and modify the file.                                                       |

### **Response**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

A successful call returns the following concrete JSON payload:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Rate Limits & Throttling

The API allows **60 calls per minute** per account. If the limit is exceeded, the service returns HTTP 429. Implement exponential back‑off and retry after the `Retry-After` header value.

### Error Codes

| Code | Message      | When it occurs                                          |
| ---- | ------------ | ------------------------------------------------------- |
| 400  | Bad Request  | The request URI or parameters are malformed.            |
| 401  | Unauthorized | Missing or invalid authentication token.                |
| 404  | Not Found    | The specified workbook cannot be found or accessed.     |
| 500  | Server Error | An internal server error while processing the workbook. |

## Where should we use the Replace content of Range in Remote Spreadsheet API?

- **Batch Cloud File Update**: Modify the contents of multiple Excel files stored in cloud storage such as AWS S3 and Azure Blob.
- **Dynamic population of cloud templates**: Batch‑populate dynamic data for report templates stored in the cloud.
- **Cross‑region file synchronization**: Synchronize the content consistency of Excel files in cloud storage across different geographical regions.

## Why should you use the Replace content of Range in Remote Spreadsheet API?

- **Developer‑Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.
- **Reduced Labor Costs**: Decreases the need for dedicated positions handling document consolidation.
- **Pay‑per‑use**: No upfront investment; you only pay for API calls actually used.
- **Zero Maintenance Costs**: No need to maintain servers, update software, or deal with compatibility issues.
- **Preserves complex Excel formatting** in a universally accessible PDF format.

## How to Use the Replace content of Range in Remote Spreadsheet API with SDKs

### OpenAPI Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content in spreadsheets for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
// C# example – Replace text in a remote range
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var config = new Configuration
{
    ClientId = "YOUR_CLIENT_ID",
    ClientSecret = "YOUR_CLIENT_SECRET"
};
var api = new CellsApi(config);
var request = new PutReplaceContentRequest(
    name: "report.xlsx",
    worksheet: "Sheet1",
    cellArea: "A1:D20",
    searchText: "OldText",
    replaceText: "NewText",
    folder: "input",
    storageName: null);
api.PutReplaceContent(request);
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
// Java example – Replace text in a remote range
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
PutReplaceContentRequest request = new PutReplaceContentRequest()
        .name("report.xlsx")
        .worksheet("Sheet1")
        .cellArea("A1:D20")
        .searchText("OldText")
        .replaceText("NewText")
        .folder("input");
api.putReplaceContent(request);
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
// PHP example – Replace text in a remote range
require_once 'vendor/autoload.php';

$config = new Aspose\Cells\Configuration();
$config->setClientId('YOUR_CLIENT_ID');
$config->setClientSecret('YOUR_CLIENT_SECRET');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$request = new Aspose\Cells\Model\Requests\PutReplaceContentRequest(
    "report.xlsx", "Sheet1", "A1:D20", "OldText", "NewText", "input"
);
$apiInstance->putReplaceContent($request);
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
# Ruby example – Replace text in a remote range
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = 'YOUR_CLIENT_ID'
config.client_secret = 'YOUR_CLIENT_SECRET'

api_instance = AsposeCellsCloud::CellsApi.new
request = AsposeCellsCloud::PutReplaceContentRequest.new(
  name: 'report.xlsx',
  worksheet: 'Sheet1',
  cell_area: 'A1:D20',
  search_text: 'OldText',
  replace_text: 'NewText',
  folder: 'input'
)
api_instance.put_replace_content(request)
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
// Node.js example – Replace text in a remote range
const { CellsApi, PutReplaceContentRequest } = require('asposecellscloud');

const config = {
    clientId: 'YOUR_CLIENT_ID',
    clientSecret: 'YOUR_CLIENT_SECRET'
};

const api = new CellsApi(config);
const request = new PutReplaceContentRequest({
    name: 'report.xlsx',
    worksheet: 'Sheet1',
    cellArea: 'A1:D20',
    searchText: 'OldText',
    replaceText: 'NewText',
    folder: 'input'
});

api.putReplaceContent(request).then(() => {
    console.log('Content replaced successfully.');
}).catch(err => {
    console.error(err);
});
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
# Python example – Replace text in a remote range
from asposecellscloud import CellsApi, PutReplaceContentRequest, Configuration

configuration = Configuration()
configuration.client_id = 'YOUR_CLIENT_ID'
configuration.client_secret = 'YOUR_CLIENT_SECRET'

api_instance = CellsApi(configuration)

request = PutReplaceContentRequest(
    name='report.xlsx',
    worksheet='Sheet1',
    cell_area='A1:D20',
    search_text='OldText',
    replace_text='NewText',
    folder='input'
)

api_instance.put_replace_content(request)
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
# Perl example – Replace text in a remote range
use AsposeCellsCloud::Api::CellsApi;
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::Object::PutReplaceContentRequest;

my $config = AsposeCellsCloud::Configuration->new(
    client_id => 'YOUR_CLIENT_ID',
    client_secret => 'YOUR_CLIENT_SECRET'
);
my $api = AsposeCellsCloud::Api::CellsApi->new($config);

my $request = AsposeCellsCloud::Object::PutReplaceContentRequest->new(
    name => 'report.xlsx',
    worksheet => 'Sheet1',
    cell_area => 'A1:D20',
    search_text => 'OldText',
    replace_text => 'NewText',
    folder => 'input'
);
$api->put_replace_content(request => $request);
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
// Go example – Replace text in a remote range
package main

import (
    "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v4/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v4/model"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.ClientId = "YOUR_CLIENT_ID"
    cfg.ClientSecret = "YOUR_CLIENT_SECRET"

    apiInstance := api.NewCellsApi(cfg)

    request := model.PutReplaceContentRequest{
        Name:        "report.xlsx",
        Worksheet:   "Sheet1",
        CellArea:    "A1:D20",
        SearchText:  "OldText",
        ReplaceText: "NewText",
        Folder:      "input",
    }

    _, err := apiInstance.PutReplaceContent(request)
    if err != nil {
        panic(err)
    }
    fmt.Println("Content replaced successfully.")
}
```

{{</tab>}}
{{< /tabs >}}

For related operations, see the **Replace Content in Remote Worksheet** API.

## Frequently Asked Questions

<details>
<summary>How do I authenticate when calling the Replace Content in Remote Range API?</summary>
First obtain an access token by POSTing your **client_id** and **client_secret** to `https://api.aspose.cloud/connect/token`. Then include the header `Authorization: Bearer <access_token>` in every request, including the Replace Content call.
</details>

<details>
<summary>What is the required format for the <code>cellArea</code> parameter?</summary>
`cellArea` must be a valid Excel range string like `"A1:D20"` (uppercase column letters, colon, row numbers). Partial ranges such as `"A:C"` or `"1:10"` are also accepted.
</details>

<details>
<summary>What response indicates a successful replace operation?</summary>
A successful call returns HTTP 200 with JSON `{ "Code": 200, "Status": "OK" }`. The `Code` field mirrors the HTTP status, while `Status` provides a human‑readable message.
</details>