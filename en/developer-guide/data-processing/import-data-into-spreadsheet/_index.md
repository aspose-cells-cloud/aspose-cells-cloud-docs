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

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> Data Import**: Supports various delimiters and automatically detects encoding.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> Data Handling**: Flattens complex JSON structures into Excel tables.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> File Conversion**: Maps node data to Excel row and column structure.

## **Import Data into Spreadsheet API Description**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

**cURL example**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

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

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## Why You Should Use This API

- **Efficient data loading** – Enables bulk import of large datasets directly into a workbook without creating intermediate files.  
- **Broad SDK support** – Provides client libraries for .NET, Java, PHP, Ruby, Node.js, Python, Go, and Perl, simplifying integration.  
- **In‑memory processing** – Performs transformations in memory, which reduces temporary storage requirements.  

## How to Use the Import Data into Spreadsheet API with SDKs

**Prerequisites:** To use this API you must have a valid Aspose Cloud account, the latest version of the Aspose.Cells Cloud SDK (v4.0 or newer), and an OAuth2 access token with the `Cells.ReadWrite` scope. The data files must not exceed the service‑specific size limits (typically 100 MB per file).

**Notes / Limitations:** The API supports up to 1 000 000 rows per import. Only comma is the default CSV delimiter; other single‑character delimiters can be specified via the `splitter` parameter. Large XML files may increase processing time.

For related operations such as exporting data or converting workbook formats, see the **Export Data** and **Convert Workbook** documentation.

### Import Data into Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">Import Data into Spreadsheet API Specification</a> provides a publicly accessible programming interface, allowing REST interactions directly from your web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to import data into a spreadsheet worksheet with short code. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to invoke Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("clientId", "clientSecret");
var response = api.ImportDataIntoSpreadsheet(
    dataFile: "data.csv",
    spreadsheet: "book.xlsx",
    worksheet: "Sheet1",
    startCell: "A1",
    insert: true);
Console.WriteLine($"Imported file: {response.Name}");
```

{{</tab>}}
{{<tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ResponseFile;

CellsApi api = new CellsApi("clientId", "clientSecret");
ResponseFile response = api.importDataIntoSpreadsheet(
    "data.csv",
    "book.xlsx",
    "Sheet1",
    "A1",
    true);
System.out.println("Imported file: " + response.getName());
```

{{</tab>}}
{{<tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;

$api = new CellsApi('clientId', 'clientSecret');
$response = $api->importDataIntoSpreadsheet(
    'data.csv',
    'book.xlsx',
    'Sheet1',
    'A1',
    true
);
echo "Imported file: " . $response->getName();
?>
```

{{</tab>}}
{{<tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('clientId', 'clientSecret')
response = api.import_data_into_spreadsheet(
  'data.csv',
  'book.xlsx',
  'Sheet1',
  'A1',
  true
)
puts "Imported file: #{response.name}"
```

{{</tab>}}
{{<tab tabNum="5" >}}

```javascript
const { CellsApi } = require('asposecellscloud');

const api = new CellsApi('clientId', 'clientSecret');
api.importDataIntoSpreadsheet(
    'data.csv',
    'book.xlsx',
    'Sheet1',
    'A1',
    true
).then(response => {
    console.log(`Imported file: ${response.name}`);
});
```

{{</tab>}}
{{<tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi

api = CellsApi('clientId', 'clientSecret')
response = api.import_data_into_spreadsheet(
    data_file='data.csv',
    spreadsheet='book.xlsx',
    worksheet='Sheet1',
    start_cell='A1',
    insert=True
)
print(f"Imported file: {response.name}")
```

{{</tab>}}
{{<tab tabNum="7" >}}

```perl
use Aspose::Cells::Cloud::Api::CellsApi;

my $api = Aspose::Cells::Cloud::Api::CellsApi->new('clientId', 'clientSecret');
my $response = $api->importDataIntoSpreadsheet(
    'data.csv',
    'book.xlsx',
    'Sheet1',
    'A1',
    1
);
print "Imported file: " . $response->{Name} . "\n";
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
    api := asposecellscloud.NewCellsApi("clientId", "clientSecret")
    response, err := api.ImportDataIntoSpreadsheet(
        "data.csv",
        "book.xlsx",
        "Sheet1",
        "A1",
        true,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Imported file: %s\n", response.Name)
}
```

{{</tab>}}
{{< /tabs >}}