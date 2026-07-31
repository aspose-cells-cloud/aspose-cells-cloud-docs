---
title: "Aspose.Cells Cloud Replace Web API – Update Text in Remote Spreadsheet Range"
second_title: "Document"
ArticleTitle: "Bulk Range Text Replacement in Cloud Excel Files – Find & Replace API"
linktitle: "Replace Remote Range Content"
type: docs
url: /replace-content-in-remote-range/
keywords: "replace content remote range, Aspose.Cells Cloud replace content, Excel find replace API, cloud spreadsheet range replace, remote Excel file update"
description: "Learn how to replace content in a remote range of an Excel workbook using Aspose.Cells Cloud API. This guide covers request parameters, response handling, error codes, and SDK examples for multiple programming languages."
weight: 100
---

Perform bulk text replacement across remote Excel files stored in the cloud. Find and update specific text strings within selected ranges efficiently using Aspose.Cells Find and Replace API.

## **Replace Content in Remote Range API**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
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

The [OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the best way to accelerate development. The SDK handles the underlying details, allowing you to simply implement replace content in spreadsheets for cells with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_ACCESS_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.ReplaceContentInRemoteRange(
            name: "report.xlsx",
            worksheet: "Sheet1",
            cellArea: "A1:D20",
            searchText: "OldText",
            replaceText: "NewText",
            folder: "MyFolder",
            storageName: null,
            region: null,
            password: null);

        Console.WriteLine($"Code: {response.Code}, Status: {response.Status}");
    }
}
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class ReplaceRangeExample {
    public static void main(String[] args) {
        Configuration config = new Configuration();
        config.setAccessToken("YOUR_ACCESS_TOKEN");
        config.setBaseUrl("https://api.aspose.cloud");

        CellsApi api = new CellsApi(config);

        CellsCloudResponse response = api.replaceContentInRemoteRange(
                "report.xlsx",
                "Sheet1",
                "A1:D20",
                "OldText",
                "NewText",
                "MyFolder",
                null,
                null,
                null,
                null);

        System.out.println("Code: " + response.getCode() + ", Status: " + response.getStatus());
    }
}
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Configuration;
use Aspose\Cells\Api\CellsApi;

$config = new Configuration();
$config->setAccessToken('YOUR_ACCESS_TOKEN');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new CellsApi($config);

try {
    $response = $apiInstance->replaceContentInRemoteRange(
        'report.xlsx',
        'Sheet1',
        'A1:D20',
        'OldText',
        'NewText',
        'MyFolder',
        null,
        null,
        null,
        null,
        null
    );
    echo "Code: {$response->getCode()}, Status: {$response->getStatus()}";
} catch (Exception $e) {
    echo 'Exception when calling CellsApi->replaceContentInRemoteRange: ', $e->getMessage();
}
?>
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = 'YOUR_ACCESS_TOKEN'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::CellsApi.new

begin
  response = api_instance.replace_content_in_remote_range(
    'report.xlsx',
    'Sheet1',
    'A1:D20',
    'OldText',
    'NewText',
    'MyFolder',
    nil,
    nil,
    nil,
    nil,
    nil
  )
  puts "Code: #{response.code}, Status: #{response.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling CellsApi->replace_content_in_remote_range: #{e}"
end
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration();
config.accessToken = 'YOUR_ACCESS_TOKEN';
config.baseUrl = 'https://api.aspose.cloud';

const apiInstance = new CellsApi(config);

apiInstance.replaceContentInRemoteRange(
    'report.xlsx',
    'Sheet1',
    'A1:D20',
    'OldText',
    'NewText',
    'MyFolder',
    null,
    null,
    null,
    null,
    null,
    (error, data, response) => {
        if (error) {
            console.error('Error:', error);
        } else {
            console.log(`Code: ${data.code}, Status: ${data.status}`);
        }
    }
);
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = 'YOUR_ACCESS_TOKEN'
config.host = 'https://api.aspose.cloud'

api_instance = CellsApi(config)

try:
    response = api_instance.replace_content_in_remote_range(
        name='report.xlsx',
        worksheet='Sheet1',
        cell_area='A1:D20',
        search_text='OldText',
        replace_text='NewText',
        folder='MyFolder',
        storage_name=None,
        region=None,
        password=None
    )
    print(f"Code: {response.code}, Status: {response.status}")
except Exception as e:
    print("Exception when calling CellsApi->replace_content_in_remote_range:", e)
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
use Aspose::Cells::API::CellsApi;
use Aspose::Cells::Configuration;

my $config = Aspose::Cells::Configuration->new(
    access_token => 'YOUR_ACCESS_TOKEN',
    host => 'https://api.aspose.cloud'
);
my $api_instance = Aspose::Cells::API::CellsApi->new($config);

eval {
    my $response = $api_instance->replace_content_in_remote_range(
        name => 'report.xlsx',
        worksheet => 'Sheet1',
        cell_area => 'A1:D20',
        search_text => 'OldText',
        replace_text => 'NewText',
        folder => 'MyFolder'
    );
    print "Code: $response->{code}, Status: $response->{status}\n";
};
if ($@) {
    warn "Exception when calling CellsApi->replace_content_in_remote_range: $@";
}
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.AccessToken = "YOUR_ACCESS_TOKEN"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi

    resp, _, err := api.ReplaceContentInRemoteRange(
        "report.xlsx",
        "Sheet1",
        "A1:D20",
        "OldText",
        "NewText",
        "MyFolder",
        nil, nil, nil, nil,
    )
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("Code: %d, Status: %s\n", resp.Code, resp.Status)
}
```

{{</tab>}}
{{< /tabs >}}