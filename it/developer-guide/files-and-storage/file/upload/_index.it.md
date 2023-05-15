---
title: Carica file
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/file/upload/
keywords: Learn how to upload file with Aspose Cells Cloud REST API
description: Scopri come caricare file con Aspose Cells Cloud REST API SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 100
---
Questo REST API indica `upload file`.

## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
 I parametri della richiesta sono:
 
| Nome parametro| Tipo| Percorso/Stringa di query/HTTPBody|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso dove caricare includendo il nome file e l'estensione, ad esempio /file.ext o /Folder 1/file.ext Se il contenuto è multipart e il percorso non contiene il nome del file, tenta di ottenerli dal parametro filename dall'intestazione Content-Disposition.|
| file| File| formData| File da caricare|
| storageName| corda| domanda| Nome di archiviazione|
 
 IL[Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.
 
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
 
## Famiglia di SDK cloud
 
 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
 
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
 

