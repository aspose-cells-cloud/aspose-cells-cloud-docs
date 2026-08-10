---
title: "How to Create an Excel Workbook with a Template File"
second_title: "Document"
linktitle: "Template File"
type: docs
url: /create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, template, API, Aspose.Cells, workbook, REST, Cloud"
description: "Learn how to generate Excel workbooks from template files using the Aspose.Cells Cloud REST API. Includes prerequisites, authentication steps, cURL examples, error‑handling details, and SDK code snippets."
weight: 30
---

# How to Create an Excel Workbook with a Template File

Create a new Excel workbook by using an existing template file and, optionally, a data file that supplies Smart‑Marker values. The operation is performed through the **PUT** `/cells/{name}` endpoint of Aspose.Cells Cloud.

---

## Prerequisites

| Requirement | Description |
|-------------|-------------|
| **Aspose.Cells Cloud account** | Sign‑up at https://dashboard.aspose.cloud/ and obtain a **Client Id** / **Client Secret**. |
| **JWT access token** | Generate a JWT token as described in the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Template file** | Upload the template Excel file (e.g., `Calendar.xlsx`) to your chosen storage using the **Upload File** API or the UI. |
| **Data file (optional)** | A JSON or XML file that contains Smart‑Marker values (e.g., `Sample_Data.xml`). |
| **Supported storage** | Default storage (`Default`) or a custom storage configured in your Aspose account. |

---

## Authentication

All Aspose.Cells Cloud requests require a **Bearer JWT token** passed in the `Authorization` header:

```http
Authorization: Bearer {access_token}
```

The token must be obtained beforehand and is valid for 1 hour by default.

---

## Request

### HTTP Request

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Component | Value |
|-----------|-------|
| **Method** | `PUT` |
| **Path**   | `/cells/{name}` – `name` is the desired name of the newly created workbook (including extension, e.g., `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (when a data file is sent in the body). |
| **Accept** | `application/json` |

### Path Parameter

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `name` | string | **Yes** | The name of the workbook to be created (e.g., `newworkbook.xlsx`). |

### Query Parameters

| Parameter | Type | Required | Default | Description |
|-----------|------|----------|---------|-------------|
| `templateFile` | string | No | — | Name of the template file stored in the cloud. |
| `dataFile` | string | No | — | Name of the data file (XML or JSON) stored in the cloud. |
| `isWriteOver` | boolean | No | `false` | Overwrite the target file if it already exists. Pass `true` or `false` **without** quotes. |
| `folder` | string | No | — | Folder path where the template (and optional data file) resides. |
| `storageName` | string | No | — | Name of the storage service that contains the files. |
| `checkExcelRestriction` | boolean | No | `true` | Validate the workbook against Excel restrictions before creation. |

### Request Body (optional)

When the data for Smart‑Marker placeholders is sent directly in the request, include it as a multipart file part named **`data`**.

| Part Name | Type | Description |
|-----------|------|-------------|
| `data` | file | XML or JSON file that contains Smart‑Marker values. |

#### Example cURL with request body

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*If the `dataFile` query parameter is used instead of a multipart body, omit the `-F` flag.*

---

## Response

A successful call returns a **`200 OK`** (or **`201 Created`** when a new file is generated) with a JSON payload that describes the created workbook.

```json
{
    "Code": 200,
    "Status": "OK",
    "File": {
        "Name": "newworkbook.xlsx",
        "Size": 18234,
        "Path": "output/newworkbook.xlsx",
        "Url": "https://api.aspose.cloud/v3.0/storage/file/output/newworkbook.xlsx"
    }
}
```

### Response Data Types

| Property | Type | Description |
|----------|------|-------------|
| `Code` | integer | HTTP‑like status code returned by the API. |
| `Status` | string | Textual description of the status. |
| `File` | object | Details of the generated workbook. |
| `File.Name` | string | File name of the created workbook. |
| `File.Size` | integer | Size in bytes. |
| `File.Path` | string | Relative path in the storage. |
| `File.Url` | string | Direct download URL (requires the same JWT token). |

---

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
---

## SDK Examples

The following snippets demonstrate how to invoke **PutWorkbookCreate** with the official Aspose.Cells Cloud SDKs.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | The new document name.
var templateFile = "Calendar.xlsx"; // string | Template file name.
var dataFile = "Sample_Data.xml"; // string | Data file name (optional).
var isWriteOver = true; // bool? | Overwrite if exists.
var folder = "templates"; // string | Folder where files reside.
var storageName = "MyStorage"; // string | Storage name.

using (var dataStream = File.OpenRead("Sample_Data.xml"))
{
    var response = apiInstance.PutWorkbookCreate(
        name,
        templateFile: templateFile,
        dataFile: dataFile,
        isWriteOver: isWriteOver,
        folder: folder,
        storageName: storageName,
        data: dataStream);
    Console.WriteLine(response);
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cloud.cells.api.WorkbookApi;
import com.aspose.cloud.cells.model.*;

import java.io.File;
import java.io.FileInputStream;

WorkbookApi api = new WorkbookApi();
String name = "newworkbook.xlsx";
String templateFile = "Calendar.xlsx";
String dataFile = "Sample_Data.xml";
Boolean isWriteOver = true;
String folder = "templates";
String storageName = "MyStorage";

FileInputStream dataStream = new FileInputStream(new File("Sample_Data.xml"));
CellsCloudResponse response = api.putWorkbookCreate(
        name,
        templateFile,
        dataFile,
        isWriteOver,
        folder,
        storageName,
        dataStream);
System.out.println(response);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorkbookApi;
use Aspose\Cells\Cloud\Configuration;

$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new WorkbookApi(null, $config);
$name = "newworkbook.xlsx";
$templateFile = "Calendar.xlsx";
$dataFile = "Sample_Data.xml";
$isWriteOver = true;
$folder = "templates";
$storageName = "MyStorage";

$data = fopen("Sample_Data.xml", "r");
$result = $apiInstance->putWorkbookCreate($name, $templateFile, $dataFile, $isWriteOver, $folder, $storageName, $data);
print_r($result);
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::WorkbookApi.new
api.config.access_token = '{access_token}'

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = true
folder = 'templates'
storage_name = 'MyStorage'

File.open('Sample_Data.xml', 'rb') do |data|
  response = api.put_workbook_create(name,
                                     template_file: template_file,
                                     data_file: data_file,
                                     is_write_over: is_write_over,
                                     folder: folder,
                                     storage_name: storage_name,
                                     data: data)
  puts response
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorkbookApi, Configuration } = require('asposecellscloud');
const fs = require('fs');

let config = new Configuration();
config.accessToken = '{access_token}';
config.basePath = 'https://api.aspose.cloud';

let apiInstance = new WorkbookApi(config);

let name = 'newworkbook.xlsx';
let templateFile = 'Calendar.xlsx';
let dataFile = 'Sample_Data.xml';
let isWriteOver = true;
let folder = 'templates';
let storageName = 'MyStorage';

let data = fs.createReadStream('Sample_Data.xml');

apiInstance.putWorkbookCreate(name, templateFile, dataFile, isWriteOver, folder, storageName, data)
    .then(response => console.log(response))
    .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.apis import WorkbookApi
from asposecellscloud.models import CellsCloudResponse

config = asposecellscloud.Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api_instance = WorkbookApi(asposecellscloud.ApiClient(config))

name = 'newworkbook.xlsx'
template_file = 'Calendar.xlsx'
data_file = 'Sample_Data.xml'
is_write_over = True
folder = 'templates'
storage_name = 'MyStorage'

with open('Sample_Data.xml', 'rb') as data:
    response = api_instance.put_workbook_create(
        name,
        template_file=template_file,
        data_file=data_file,
        is_write_over=is_write_over,
        folder=folder,
        storage_name=storage_name,
        data=data)
    print(response)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorkbookApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '{access_token}';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::Api::WorkbookApi->new($config);

my $name = 'newworkbook.xlsx';
my $template_file = 'Calendar.xlsx';
my $data_file = 'Sample_Data.xml';
my $is_write_over = 1;
my $folder = 'templates';
my $storage_name = 'MyStorage';

open my $fh, '<:raw', 'Sample_Data.xml' or die $!;
my $response = $api_instance->put_workbook_create(
    name => $name,
    template_file => $template_file,
    data_file => $data_file,
    is_write_over => $is_write_over,
    folder => $folder,
    storage_name => $storage_name,
    data => $fh);
print $response;
close $fh;
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "os"

    asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorkbookApi(cfg)

    name := "newworkbook.xlsx"
    templateFile := "Calendar.xlsx"
    dataFile := "Sample_Data.xml"
    isWriteOver := true
    folder := "templates"
    storageName := "MyStorage"

    data, _ := os.Open("Sample_Data.xml")
    defer data.Close()

    result, _, err := apiInstance.PutWorkbookCreate(name, &templateFile, &dataFile, &isWriteOver, &folder, &storageName, data)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Printf("Response: %+v\n", result)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Error Handling

| Status Code | Situation | Recommended Action |
|-------------|-----------|--------------------|
| **400** | Required parameters missing or invalid file type. | Verify query parameters, ensure template and data files exist and are supported (`.xlsx`, `.xml`, `.json`). |
| **401** | JWT token is missing, expired, or malformed. | Regenerate a fresh access token using your Client Id/Secret. |
| **413** | Uploaded file exceeds the service size limit (default 50 MB). | Reduce file size or split the workbook into smaller parts. |
| **500** | Unexpected server error. | Retry after a short delay; if the problem persists, contact Aspose support with the `Request‑Id` header value. |

---

## See Also

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Save an existing workbook to a specified format.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Retrieve workbook information or download the file.  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Upload template or data files to cloud storage.  

---