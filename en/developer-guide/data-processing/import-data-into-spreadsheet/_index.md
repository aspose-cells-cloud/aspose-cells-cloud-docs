---
title: "Aspose.Cells Cloud Data Import API – A cloud solution for automatically importing CSV, JSON, and XML data into Excel spreadsheets."
second_title: "Document"
ArticleTitle: "Multi‑Source Data Integration Excel Platform – Aspose.Cells Cloud Automated Data Import and Transformation API."
linktitle: "Import Data into Spreadsheet"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Aspose Cells, data import API, CSV to Excel, JSON to Excel, XML to Excel, cloud spreadsheet, REST API"
description: "Import CSV, JSON, or XML data into Excel spreadsheets with Aspose.Cells Cloud REST API. Learn request format, parameters, sample SDK code, and error handling."
weight: 100
---

## Core Features

### Multi-Format Data Support

- **[CSV](https://docs.fileformat.com/spreadsheet/csv/) Data Import**: Supports various delimiters and automatically detects encoding.
- **[JSON](https://docs.fileformat.com/web/json/) Data Handling**: Flattens complex JSON structures into Excel tables.
- **[XML](https://docs.fileformat.com/web/xml/) File Conversion**: Maps node data to Excel row and column structure.

### Advanced Data Processing Capabilities

- **Intelligent Field Mapping**: Automatically matches source fields to target columns.
- **Data Transformation Rules**: Supports data‑type conversion and formatting.
- **Batch Processing Support**: Allows importing multiple data files simultaneously.

## **Import Data into Spreadsheet API Description**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### Request Parameters

| Parameter Name     | Type   | Location         | Description                                                              |
| ------------------ | ------ | ---------------- | ------------------------------------------------------------------------ |
| datafile           | File   | FormData         | The data file (CSV, JSON, or XML) to be imported.                        |
| spreadsheet        | File   | FormData         | The target workbook that will receive the imported data.                 |
| worksheet          | string | Query            | Name of the worksheet where data will be placed.                         |
| startCell          | string | Query            | Top‑left cell (e.g., `A1`) that marks the start position for the import. |
| insert             | bool   | Query            | `true` to insert rows; `false` to overwrite existing data.               |
| convertNumericData | bool   | Query            | `true` to convert numeric strings to numbers during import.              |
| splitter           | string | Query            | Single‑character CSV delimiter (default is `,`).                         |
| outPath            | string | Query (optional) | Folder path where the updated workbook will be stored.                   |
| outStorageName     | string | Query (optional) | Name of the storage location for the output file.                        |
| fontsLocation      | string | Query (optional) | Path to a custom fonts folder, if required.                              |
| region             | string | Query (optional) | Spreadsheet region configuration (e.g., `en-US`).                        |
| password           | string | Query (optional) | Password for opening a protected workbook.                               |

### Response

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Error Codes

| Code | Message               | When It Occurs                                      |
| ---- | --------------------- | --------------------------------------------------- |
| 400  | Bad Request           | Invalid API URI or malformed request parameters.    |
| 401  | Unauthorized          | Missing/invalid access token or client credentials. |
| 404  | Not Found             | The specified spreadsheet cannot be accessed.       |
| 500  | Internal Server Error | An unexpected server‑side problem while processing. |

## Why You Should Use This API

- **Efficient Data Loading** – Import large volumes of data without first creating intermediate files.
- **Developer‑Friendly** – SDKs are available for many languages, reducing development effort and ensuring consistent implementations.
- **Cost‑Effective** – The API processes data in‑memory, minimizing storage usage and associated costs.

## How to Use the Import Data into Spreadsheet API with SDKs

### Import Data into Spreadsheet API Specification

The [Import Data into Spreadsheet API Specification](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) provides a publicly accessible programming interface, allowing REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to import data into a spreadsheet worksheet with short code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
// C# example – Import CSV into a workbook
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new CellsApi(config);
var token = apiInstance.OAuth2GetToken(); // obtain OAuth2 token
apiInstance.Authorization = $"Bearer {token.AccessToken}";

using var dataStream = File.OpenRead("data.csv");
using var workbookStream = File.OpenRead("template.xlsx");
var result = apiInstance.ImportDataIntoSpreadsheet(
    datafile: dataStream,
    spreadsheet: workbookStream,
    worksheet: "Sheet1",
    startCell: "A1",
    insert: true,
    convertNumericData: true,
    splitter: ","
);
Console.WriteLine($"File saved to: {result[0].Name}");
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
// Java example – Import JSON into a workbook
CellsApi api = new CellsApi("<client_id>", "<client_secret>");
String token = api.getAccessToken(); // OAuth2
api.setAccessToken(token);

File dataFile = new File("data.json");
File workbook = new File("template.xlsx");

ImportResponse response = api.importDataIntoSpreadsheet(
    dataFile,
    workbook,
    "Sheet1",
    "A1",
    true,
    true,
    null
);
System.out.println("Output file: " + response.getName());
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
<?php
// PHP example – Import XML into a workbook
use Aspose\Cells\Configuration;
use Aspose\Cells\Api\CellsApi;

$config = new Configuration();
$config->setClientId('<client_id>');
$config->setClientSecret('<client_secret>');

$api = new CellsApi($config);
$token = $api->oAuth2GetToken();
$api->setAccessToken($token->getAccessToken());

$dataFile = fopen('data.xml', 'r');
$workbook = fopen('template.xlsx', 'r');

$response = $api->importDataIntoSpreadsheet(
    $dataFile,
    $workbook,
    'Sheet1',
    'A1',
    true,
    true,
    null
);
echo "Result file: " . $response[0]->getName();
?>
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
# Ruby example – Import CSV into a workbook
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<client_id>'
config.client_secret = '<client_secret>'

api_instance = AsposeCellsCloud::CellsApi.new
token = api_instance.oauth2_get_token
api_instance.access_token = token.access_token

data = File.open('data.csv')
workbook = File.open('template.xlsx')

result = api_instance.import_data_into_spreadsheet(
  datafile: data,
  spreadsheet: workbook,
  worksheet: 'Sheet1',
  startcell: 'A1',
  insert: true,
  convert_numeric_data: true,
  splitter: ','
)
puts "Saved as #{result[0].name}"
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
// Node.js example – Import CSV into a workbook
const { CellsApi, Configuration } = require("asposecellscloud");
const fs = require("fs");

let config = new Configuration({
  clientId: "<client_id>",
  clientSecret: "<client_secret>",
});
let api = new CellsApi(config);

api
  .oAuth2GetToken()
  .then((token) => {
    api.accessToken = token.access_token;

    const dataFile = fs.createReadStream("data.csv");
    const workbookFile = fs.createReadStream("template.xlsx");

    return api.importDataIntoSpreadsheet(
      dataFile,
      workbookFile,
      "Sheet1",
      "A1",
      true,
      true,
      null,
    );
  })
  .then((result) => {
    console.log("Result file:", result[0].name);
  })
  .catch((err) => console.error(err));
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
# Python example – Import JSON into a workbook
from asposecellscloud import CellsApi, Configuration

config = Configuration(client_id='<client_id>', client_secret='<client_secret>')
api = CellsApi(config)

token = api.oauth2_get_token()
api.access_token = token.access_token

with open('data.json', 'rb') as data_file, open('template.xlsx', 'rb') as workbook_file:
    result = api.import_data_into_spreadsheet(
        datafile=data_file,
        spreadsheet=workbook_file,
        worksheet='Sheet1',
        startcell='A1',
        insert=True,
        convert_numeric_data=True,
        splitter=None
    )
print('Output file:', result[0].name)
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
# Perl example – Import CSV into a workbook
use Aspose::Cells::Api::CellsApi;
use Aspose::Cells::Configuration;

my $config = Aspose::Cells::Configuration->new(
    client_id     => '<client_id>',
    client_secret => '<client_secret>'
);
my $api = Aspose::Cells::Api::CellsApi->new($config);
my $token = $api->o_auth2_get_token;
$api->access_token($token->{access_token});

open my $data_fh, '<', 'data.csv' or die $!;
open my $work_fh, '<', 'template.xlsx' or die $!;

my $result = $api->import_data_into_spreadsheet(
    datafile          => $data_fh,
    spreadsheet       => $work_fh,
    worksheet         => 'Sheet1',
    startcell         => 'A1',
    insert            => JSON::true,
    convert_numeric_data => JSON::true,
    splitter          => ','
);
print "Result file: $result->[0]{name}\n";
```

{{</tab>}}
{{<tab tabNum="8" >}}

```go
// Go example – Import XML into a workbook
package main

import (
    "fmt"
    "os"

    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    config := cells.NewConfiguration()
    config.ClientId = "<client_id>"
    config.ClientSecret = "<client_secret>"

    api := cells.NewAPIClient(config)

    // Obtain token
    token, _, err := api.OAuth2Api.ConnectToken(config.ClientId, config.ClientSecret, nil)
    if err != nil {
        panic(err)
    }
    config.AccessToken = token.AccessToken

    dataFile, _ := os.Open("data.xml")
    workbookFile, _ := os.Open("template.xlsx")

    result, _, err := api.DataProcessingApi.ImportDataIntoSpreadsheet(
        dataFile,
        workbookFile,
        "Sheet1",
        "A1",
        true,
        true,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Println("Result file:", result[0].Name)
}
```

{{</tab>}}
{{< /tabs >}}
