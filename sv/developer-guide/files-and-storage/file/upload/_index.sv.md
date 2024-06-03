---
title: Ladda upp Fil
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/file/upload/
keywords: Learn how to upload file with Aspose Cells Cloud REST API
description: Lär dig hur du laddar upp filer med Aspose Cells Cloud REST API SDK-stöd för olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Ladda upp fil
---
Denna REST API indikerar `upload file`.

## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Sökväg dit du ska ladda upp inklusive filnamn och filtillägg t.ex. /file.ext eller /Folder 1/file.ext Om innehållet är flerdelat och sökvägen inte innehåller filnamnet försöker den hämta dem från filnamnsparametern från Content-Disposition-huvudet.|
| fil| Fil| formData| Fil att ladda upp|
| lagringsnamn| sträng| fråga| Lagringsnamn|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/File/UploadFile) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
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
 
## Cloud SDK-familj
 
 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
 
 {{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

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
 

