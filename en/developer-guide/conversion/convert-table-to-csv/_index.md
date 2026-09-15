---
title: "Convert Excel Table to CSV via Aspose.Cells Cloud API"
second title: "Document"
ArticleTitle: "Convert Excel Table to CSV via Aspose.Cells Cloud API"
linktype: "docs"
url: /convert-table-to-csv/
keywords: "excel to csv, table conversion, aspose.cells cloud, rest api"
description: "Step-by-step guide to convert Excel table data to CSV using Aspose.Cells Cloud REST API, with cURL and SDK examples."
weight: 100
date: 2024-05-20
---

Export table data from a local Excel file to a CSV file using the Cloud API.

## **Convert Table to CSV API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/quickstart/" rel="noopener noreferrer">JWT token-based authentication</a>.

> ⚠️ Replace `{YOUR_ACCESS_TOKEN}` with a valid JWT token obtained from [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).

```bash
-H "Authorization: Bearer {YOUR_ACCESS_TOKEN}"
```

### **Request Parameters:**

| Parameter Name | Type   | Path/Query String/HTTP Body | Description                                                                                                                             |
| -------------- | ------ | --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | FormData                    | Upload the spreadsheet file.                                                                                                            |
| worksheet      | String | Query                       | Name of the worksheet in the spreadsheet.                                                                                               |
| tableName      | String | Query                       | Name of the table to be converted.                                                                                                      |
| outPath        | String | Query                       | (Optional) Folder path where the workbook is stored; defaults to null.                                                                  |
| outStorageName | String | Query                       | Name of the storage for the output file.                                                                                                |
| fontsLocation  | String | Query                       | Path for using custom fonts.                                                                                                            |
| region         | String | Query                       | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale-specific behavior. |
| password       | String | Query                       | Password for opening the spreadsheet file.                                                                                              |

### **Response**

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

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## **Where Should You Use the Convert Table to CSV API?**

This API is ideal for scenarios requiring structured, lightweight data extraction from Excel tables:

- **Database Migration**: Convert Excel tables to CSV for bulk import into SQL databases (MySQL, PostgreSQL, SQL Server).
- **Data Warehouse Loading**: Transform Excel-based reporting tables to CSV for loading into Snowflake, Redshift, or BigQuery.
- **Batch API Payloads**: Convert Excel table data to CSV for bulk API uploads to REST services.
- **Service-to-Service Communication**: Use CSV as a lightweight data-exchange format between microservices.
- **Machine Learning Data Prep**: Convert feature tables from Excel to CSV for Python/R machine-learning libraries.
- **Statistical Analysis**: Transform research data tables to CSV for SPSS, SAS, or Stata import.
- **Content Migration**: Move structured content from Excel to CMS systems via CSV.

## Why should you use the Convert Table to CSV API?

- **Developer-Friendly**: Aspose.Cells Cloud offers SDK libraries in multiple languages, enabling quick development and comes with comprehensive documentation. Compared with building custom solutions, this significantly reduces development workload.
- **Cost-Effective**: You can convert table data without first uploading the workbook, which saves storage space and reduces costs.
- **Pure data extraction without formatting**.
- **CSV is supported by virtually every system**:
  - Databases (all major RDBMS)
  - Programming languages (native parsers in all)
  - Business intelligence tools (Tableau, Power BI, Looker)
  - Spreadsheet software (Excel, Google Sheets, LibreOffice)
  - Command-line tools (awk, sed, grep)

## How to Use the Convert Table to CSV API with SDKs?

### Prerequisites

- A valid Aspose.Cells Cloud API key and app SID.
- An Excel file containing a named table.
- A working environment for your preferred programming language (with SDK installed).

### Convert Table to CSV API Specification

The [Convert Table to CSV API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) provides a publicly accessible programming interface, allowing REST interactions directly from a web browser.
You can use the cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {YOUR_ACCESS_TOKEN}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
```

> *Tip: Add `-v` for verbose output to troubleshoot authentication or payload issues.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low-level details, allowing you to convert spreadsheet table data to a CSV file with minimal code. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples illustrate how to make calls to Aspose.Cells web services using various SDKs:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<highlight csharp>}}
// Example: Aspose.Cells.Cloud SDK for .NET
// Ensure you have set up your App SID and API Key
var configuration = new Configuration
{
    AppSid = "your_app_sid",
    AppKey = "your_api_key"
};
var cellsApi = new CellsApi(configuration.AppSid, configuration.AppKey);

var result = cellsApi.CellsTableGetTable("input.xlsx", "Sheet1", "Table1", outPath: null, storage: null);
// Save result as CSV
var fileStream = new MemoryStream(Convert.FromBase64String(result.FileContents));
File.WriteAllBytes("output.csv", fileStream.ToArray());
{{</highlight>}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<highlight java>}}
// Example: Aspose.Cells.Cloud SDK for Java
Configuration configuration = new Configuration();
configuration.setAppSid("your_app_sid");
configuration.setAppKey("your_api_key");

CellsApi cellsApi = new CellsApi(configuration);

File response = cellsApi.cellsTableGetTable("input.xlsx", "Sheet1", "Table1", null, null);
// Save to CSV
{{</highlight>}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<highlight php>}}
// Example: Aspose.Cells.Cloud SDK for PHP
$config = [
    'appId' => 'your_app_sid',
    'appKey' => 'your_api_key'
];
$cellsApi = new \Aspose\Cells\CellsApi(null, null, null, null, $config);

$response = $cellsApi->CellsTableGetTable("input.xlsx", "Sheet1", "Table1");
// Handle response
{{</highlight>}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<highlight ruby>}}
# Example: Aspose.Cells.Cloud SDK for Ruby
require 'aspose_cells_cloud'

configuration = AsposeCellsCloud::Configuration.new
configuration.app_sid = 'your_app_sid'
configuration.app_key = 'your_api_key'

api_instance = AsposeCellsCloud::CellsApi.new(configuration)

response = api_instance.cells_table_get_table('input.xlsx', 'Sheet1', 'Table1')
# Process response
{{</highlight>}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<highlight javascript>}}
// Example: Aspose.Cells.Cloud SDK for Node.js
const { CellsApi } = require("@aspose/cells-cloud");

const configuration = new configuration.Configuration();
configuration.appSid = "your_app_sid";
configuration.appKey = "your_api_key";

const cellsApi = new CellsApi(configuration);

cellsApi.cellsTableGetTable("input.xlsx", "Sheet1", "Table1").then((response) => {
    // Save response
});
{{</highlight>}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<highlight python>}}
# Example: Aspose.Cells.Cloud SDK for Python
from asposecellscloud.configuration import Configuration
from asposecellscloud.cells_api import CellsApi

config = Configuration()
config.app_sid = "your_app_sid"
config.app_key = "your_api_key"

api = CellsApi(None, None, None, None, config)
response = api.cells_table_get_table("input.xlsx", "Sheet1", "Table1")
# Save result
{{</highlight>}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<highlight perl>}}
# Example: Aspose.Cells.Cloud SDK for Perl
use Aspose::Cells::Cloud::CellsApi;
my $config = {
    'appSid' => 'your_app_sid',
    'appKey' => 'your_api_key',
};
my $cells_api = Aspose::Cells::Cloud::CellsApi->new($config);
my $response = $cells_api->cells_table_get_table("input.xlsx", "Sheet1", "Table1");
# Handle response
{{</highlight>}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<highlight go>}}
// Example: Aspose.Cells.Cloud SDK for Go
import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22/config"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22/api"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AppSid = "your_app_sid"
    cfg.AppKey = "your_api_key"

    cellsApi := api.NewCellsApiWithConfiguration(cfg)
    resp, _, err := cellsApi.CellsTableGetTable(context.Background(), "input.xlsx", "Sheet1", "Table1")
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    // Process resp
}
{{</highlight>}}
{{</tab>}}
{{< /tabs >}}

> *If you receive HTTP 401, check your JWT token validity. If 413, reduce file size or enable chunked upload.*