---
title: "Aspose.Cells Cloud – Convert Table to HTML (API v4.0)"
description: "Convert Excel tables to HTML quickly with Aspose.Cells Cloud API – secure, format‑preserving, and easy to integrate."
keywords: "Aspose.Cells, Excel to HTML, convert table to HTML, cloud API, spreadsheet conversion"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /convert-table-to-html/
type: docs
---

# Convert Table to HTML API (v4.0)

> **Quick summary** – This endpoint reads a local Excel workbook, extracts the specified **table**, converts it to an **HTML** file, and returns the result as a downloadable stream. No intermediate upload to Aspose Cloud storage is required.

---

## Table of Contents
1. [When to Use This API](#when-to-use-this-api)  
2. [Key Benefits](#key-benefits)  
3. [Endpoint Overview](#endpoint-overview)  
4. [Authentication](#authentication)  
5. [Request Parameters](#request-parameters)  
6. [Request Example (cURL)](#request-example-curl)  
7. [Success Response](#success-response)  
8. [Error Codes](#error-codes)  
9. [SDK Code Samples](#sdk-code-samples)  
10. [Additional Options](#additional-options)  
11. [Version & Change Log](#version--change-log)

---

## When to Use This API
- **Dynamic web content** – Embed pricing tables, schedules, or product lists directly into web pages or CMSes.  
- **Email templates** – Generate HTML snippets for order summaries or reports that render consistently across email clients.  
- **Dashboards & reporting tools** – Show live spreadsheet data without loading the full workbook or using heavy grid components.  
- **Document previews** – Provide quick, format‑preserving previews of specific spreadsheet sections.

---

## Key Benefits
- **Rich formatting retained** – Cell styles, fonts, colors, borders, alignment, and number formats are preserved in the HTML output.  
- **Selective export** – Convert only the required table, saving bandwidth and processing time for large workbooks.  
- **No Excel dependency** – Purely cloud‑based; works from any environment that can make HTTP calls.  
- **Developer‑friendly SDKs** – Available for C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, etc.  
- **Cost‑effective** – No need to upload the whole workbook to cloud storage; conversion occurs directly from the supplied file stream.

---

## Endpoint Overview
| Item | Details |
|------|---------|
| **HTTP Method** | `PUT` |
| **URL** | `https://api.aspose.cloud/v4.0/cells/convert/table/html` |
| **Content‑Type** | `multipart/form-data` (for file upload) |
| **Response Content‑Type** | `application/octet-stream` (HTML file stream) |
| **API Version** | `v4.0` |
| **Operation ID** | `ConvertTableToHtml` |

---

## Authentication
The API uses **JWT token‑based authentication**. Include the access token in the `Authorization` header:

```http
Authorization: Bearer {access_token}
```

> **How to obtain a token** – See the [Aspose Cloud authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

## Request Parameters

| Name | Location | Type | Required | Description |
|------|----------|------|----------|-------------|
| **Spreadsheet** | Form‑Data | `File` | **Yes** | The Excel workbook containing the table to convert. |
| **worksheet** | Query | `String` | **Yes** | Name of the worksheet that holds the table. |
| **tableName** | Query | `String` | **Yes** | Exact name of the table to be converted. |
| **outPath** | Query | `String` | No | Folder path in Aspose Cloud storage where the HTML file will be saved (optional). |
| **outStorageName** | Query | `String` | No | Storage name for the output file (optional). |
| **fontsLocation** | Query | `String` | No | Path to a folder containing custom fonts required for the conversion. |
| **region** | Query | `String` | No | Locale identifier (e.g., `en-US`, `fr-FR`). Affects number/date formatting. |
| **password** | Query | `String` | No | Password to open a protected workbook. |
| **AutoRowsFit** | Query | `Boolean` | No | Auto‑fit all rows in the worksheet (`true`/`false`). |
| **AutoColumnsFit** | Query | `Boolean` | No | Auto‑fit all columns in the worksheet (`true`/`false`). |

> **Note** – All query parameters are appended to the URL. Example: `?worksheet=Sheet1&tableName=SalesData&region=en-US`.

---

## Request Example (cURL)

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=SalesData&region=en-US" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/Workbook.xlsx" \
     -F "fontsLocation=/fonts" \
     -F "AutoRowsFit=true" \
     -F "AutoColumnsFit=true"
```

*The `-F` flag automatically sets `multipart/form-data` and streams the file.*

---

## Success Response

| Code | Description | Headers | Body |
|------|-------------|---------|------|
| **200 OK** | HTML file returned as a binary stream. | `Content-Type: application/octet-stream`<br>`Content-Disposition: attachment; filename="{TableName}.html"` | Binary HTML file (downloadable). |

**Example (partial) header output**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="SalesData.html"
Content-Length: 12458
```

The response body contains the full HTML markup of the requested table.

---

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |

Error responses are returned in JSON format:

```json
{
  "code": "ErrorCode",
  "message": "Human‑readable description of the problem."
}
```

---

## SDK Code Samples

The Aspose.Cells Cloud SDKs wrap the low‑level HTTP call, letting you convert a table with just a few lines of code. Below are ready‑to‑run snippets for the eight officially supported languages.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new ConversionApi(config);
var file = File.ReadAllBytes("Workbook.xlsx"); // local file
var response = apiInstance.ConvertTableToHtml(
    spreadsheet: file,
    worksheet: "Sheet1",
    tableName: "SalesData",
    region: "en-US",
    fontsLocation: "/fonts",
    autoRowsFit: true,
    autoColumnsFit: true
);

// `response` is a Stream containing the HTML file.
File.WriteAllBytes("SalesData.html", response.ToArray());
```
{{</tab>}}
{{<tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.sdk.ApiClient;
import com.aspose.cells.cloud.sdk.ApiException;
import com.aspose.cells.cloud.sdk.Configuration;
import com.aspose.cells.cloud.sdk.api.ConversionApi;
import java.io.File;
import java.io.FileOutputStream;
import java.io.InputStream;

Configuration config = new Configuration();
config.setAccessToken("{access_token}");
ConversionApi api = new ConversionApi(config);

File file = new File("Workbook.xlsx");
InputStream htmlStream = api.convertTableToHtml(
        file,
        "Sheet1",
        "SalesData",
        "en-US",
        "/fonts",
        true,
        true
);

try (FileOutputStream out = new FileOutputStream("SalesData.html")) {
    htmlStream.transferTo(out);
}
```
{{</tab>}}
{{<tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ConversionApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$apiInstance = new ConversionApi($config);

$file = fopen('Workbook.xlsx', 'r');
$response = $apiInstance->convertTableToHtml(
    $file,
    'Sheet1',
    'SalesData',
    'en-US',
    '/fonts',
    true,
    true
);

file_put_contents('SalesData.html', $response);
?>
```
{{</tab>}}
{{<tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
api = AsposeCellsCloud::ConversionApi.new

File.open('Workbook.xlsx', 'rb') do |file|
  result = api.convert_table_to_html(
    spreadsheet: file,
    worksheet: 'Sheet1',
    table_name: 'SalesData',
    region: 'en-US',
    fonts_location: '/fonts',
    auto_rows_fit: true,
    auto_columns_fit: true
  )
  File.write('SalesData.html', result)
end
```
{{</tab>}}
{{<tab tabNum="5" >}}
```javascript
// Node.js – using the official SDK
const { ConversionApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

const config = new Configuration({
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
});
const api = new ConversionApi(config);

const fileStream = fs.createReadStream('Workbook.xlsx');

api.convertTableToHtml(
    fileStream,
    'Sheet1',
    'SalesData',
    'en-US',
    '/fonts',
    true,
    true
).then((htmlStream) => {
    const writeStream = fs.createWriteStream('SalesData.html');
    htmlStream.pipe(writeStream);
}).catch(console.error);
```
{{</tab>}}
{{<tab tabNum="6" >}}
```python
import asposecellscloud
from asposecellscloud.rest import ApiException

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
api_instance = asposecellscloud.ConversionApi(asposecellscloud.ApiClient(config))

with open('Workbook.xlsx', 'rb') as file:
    html_stream = api_instance.convert_table_to_html(
        spreadsheet=file,
        worksheet='Sheet1',
        table_name='SalesData',
        region='en-US',
        fonts_location='/fonts',
        auto_rows_fit=True,
        auto_columns_fit=True
    )
    with open('SalesData.html', 'wb') as out_file:
        out_file.write(html_stream.read())
```
{{</tab>}}
{{<tab tabNum="7" >}}
```perl
use AsposeCellsCloud::Api::ConversionApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
my $api = AsposeCellsCloud::Api::ConversionApi->new($config);

open my $fh, '<:raw', 'Workbook.xlsx' or die $!;
my $html_stream = $api->convert_table_to_html(
    spreadsheet   => $fh,
    worksheet     => 'Sheet1',
    table_name    => 'SalesData',
    region        => 'en-US',
    fonts_location=> '/fonts',
    auto_rows_fit => 1,
    auto_columns_fit => 1
);
open my $out, '>:raw', 'SalesData.html' or die $!;
print $out $_ while <$html_stream>;
close $out;
close $fh;
```
{{</tab>}}
{{<tab tabNum="8" >}}
```go
package main

import (
    "io"
    "log"
    "os"

    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    api := asposecellscloud.NewConversionApi(cfg)

    file, err := os.Open("Workbook.xlsx")
    if err != nil {
        log.Fatalf("cannot open file: %v", err)
    }
    defer file.Close()

    htmlStream, _, err := api.ConvertTableToHtml(
        file,
        "Sheet1",
        "SalesData",
        "en-US",
        "/fonts",
        true,
        true,
    )
    if err != nil {
        log.Fatalf("API error: %v", err)
    }
    out, _ := os.Create("SalesData.html")
    defer out.Close()
    io.Copy(out, htmlStream)
}
```
{{</tab>}}
{{< /tabs >}}

---

## Additional Options

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| **AutoRowsFit** | Boolean | `false` | When `true`, rows are auto‑fitted to content after conversion. |
| **AutoColumnsFit** | Boolean | `false` | When `true`, columns are auto‑fitted to content after conversion. |
| **fontsLocation** | String | – | Path to a custom fonts folder; useful for non‑standard typefaces. |
| **region** | String | `en-US` | Controls locale‑specific number and date formatting. |
| **password** | String | – | Required only for password‑protected workbooks. |

---

## Version & Change Log

| Version | Date | Changes |
|---------|------|---------|
| **v4.0** | 2026‑07‑30 | Added `AutoRowsFit` / `AutoColumnsFit` parameters, enhanced success‑response description, included cURL example, fixed encoding artifacts, consolidated meta tags, and added SRI recommendation for external scripts. |
| **v3.2** | 2025‑11‑12 | Introduced `region` and `fontsLocation` support. |
| **v3.0** | 2024‑05‑08 | Initial public release. |

---

### Related Documentation
- [Convert Range to HTML](/convert-range-to-html/)  
- [Convert Worksheet to HTML](/convert-worksheet-to-html/)  

--- 

*Last updated: 2026‑07‑30*