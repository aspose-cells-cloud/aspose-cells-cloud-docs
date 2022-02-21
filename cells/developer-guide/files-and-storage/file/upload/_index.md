---
title: "Upload File"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /file/upload/
keywords: "REST API, upload, download, delelte, spreadsheets, excel"
description: "Cells.Cloud API for Excel operate: upload, download and delete excel file to storage."
weight: 100
---

This REST API indicates `upload file`.

## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
The request parameters are: 
 
| Parameter Name | Type | Path/Query String/HTTPBody | Description| 
| :- | :- | :- |:- | 
| path | string | path | Path where to upload including filename and extension e.g. /file.ext or /Folder 1/file.ext If the content is multipart and path does not contains the file name it tries to get them from filename parameter from Content-Disposition header. |
| file | File | formData | File to upload |
| storageName | string | query | Storage name |
 
The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/File/UploadFile) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.
 
You can use cURL command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK Family
 
Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
 
The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:
 
 {{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python">}}

{{< tab tabNum="1" >}}

```csharp

CellsApi cellsApi = new CellsApi(ClientId, ClientSecret);
cellsApi.UploadFile("DotNetSDK/OutResult/Upload_Book1.xlsx", File.OpenRead(filePath), null);

```

{{< /tab >}}

{{< tab tabNum="2" >}}
```java

    public static void main(String[] args) {
        try{
            CellsApi  cellsApi = new CellsApi(System.getenv("ProductClientId"),System.getenv("ProductClientSecret"));
            File file = new File("TestImportData.xlsx");
            cellsApi.uploadFile("JavaSDK/OutResult/Book1.xlsx", file, null);
        }
        catch( Exception e) 
        {
            System.out.print(e.getMessage());
        }
    }
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
$cells = new CellsApi( getenv("ProductClientId"),getenv("ProductClientSecret") );
$cells->uploadFile("PHPSDK/OutResult/UploadFile_Book1.xlsx","D:/projects/aspose/examples/testdata/source/Book1.xlsx",null );


```
{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}
```java

    public static void main(String[] args) {
        try{
            CellsApi  cellsApi = new CellsApi(System.getenv("ProductClientId"),System.getenv("ProductClientSecret"));
            File file = new File("TestImportData.xlsx");
            cellsApi.uploadFile("JavaSDK/OutResult/Book1.xlsx", file, null);
        }
        catch( Exception e) 
        {
            System.out.print(e.getMessage());
        }
    }
```

{{< /tab >}}

{{< tab tabNum="7" >}}
 ```perl
use strict;
use warnings;
use utf8; 
use File::Slurp;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new( client_id => $ENV{'ProductClientId'}, client_secret => $ENV{'ProductClientSecret'});
my $instance = AsposeCellsCloud::CellsApi->new(AsposeCellsCloud::ApiClient->new( $config));

my $upload_file_data = read_file( 'C:/data/CellsTests/Book1.xlsx' , binmode => ':raw' );
$instance->upload_file(path=>'PerlSDK/OutResult/UplaodFile_Book1.xlsx' ,file => $upload_file_data);

 ```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go

package main

import (
	"os"
	"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v22"
)

func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))

	file, err := os.Open("D:/projects/aspose/examples/testdata/source/Book1.xlsx")	
	if err != nil {
	   println( err)
	}


	uploadFileOpts := new(asposecellscloud.UploadFileOpts)
	uploadFileOpts.Path = "GoSDK/OutResult/UploadFile_Book1.xlsx"
	_, _, err1  := instance.UploadFile(file, uploadFileOpts)
	if err1 != nil {
	   println( err1)
	}

}

```

{{< /tab >}}
{{< tab tabNum="9" >}}
```python

import os
from asposecellscloud.apis.cells_api import CellsApi

cells_api = CellsApi(os.getenv('ProductClientId'),os.getenv('ProductClientSecret'))
cells_api.upload_file("PythonSDK/OutResult/UploadFile_Book1.xlsx", "D:/projects/aspose/examples/testdata/source/Book1.xlsx")

```
{{< /tab >}}
{{< /tabs >}}
 

