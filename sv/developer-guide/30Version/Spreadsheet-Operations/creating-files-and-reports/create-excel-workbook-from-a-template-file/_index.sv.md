---
title: "Så här skapar du en Excel-arbetsbok med en mallfil"
second_title: "Dokument"
linktitle: "Mallfil"
type: docs
url: /create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, mall, API, Aspose.Cells, arbetsbok, REST, moln"
description: "Lär dig hur du genererar Excel-arbetsböcker från mallfiler med Aspose.Cells Cloud REST API. Innehåller förutsättningar, autentiseringssteg, cURL-exempel, felhanteringsinformation och SDK-kodfragment."
weight: 30
---

# Så här skapar du en Excel-arbetsbok med en mallfil

Skapa en ny Excel-arbetsbok genom att använda en befintlig mallfil och valfritt en datafil som innehåller värden för Smart‑Marker. Åtgärden utförs via slutpunkten **PUT** `/cells/{name}` i Aspose.Cells Cloud.

---

## Förutsättningar

| Krav | Beskrivning |
|------|-------------|
| **Aspose.Cells Cloud-konto** | Registrera dig på https://dashboard.aspose.cloud/ och skaffa ett **Client Id** / **Client Secret**. |
| **JWT-åtkomsttoken** | Generera en JWT-token enligt beskrivningen i [autentiseringsguide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Mallfil** | Ladda upp Excel-mallfilen (t.ex. `Calendar.xlsx`) till valfri lagring med API:t **Upload File** eller via användargränssnittet. |
| **Datafil (valfritt)** | En JSON- eller XML-fil som innehåller värden för Smart‑Marker (t.ex. `Sample_Data.xml`). |
| **Stödd lagring** | Standardlagring (`Default`) eller en anpassad lagring som konfigurerats i ditt Aspose-konto. |

---

## Autentisering

Alla förfrågningar till Aspose.Cells Cloud kräver en **Bearer JWT-token** som skickas i `Authorization`-headern:

```http
Authorization: Bearer {access_token}
```

Token måste ha skapats på förhand och är standard giltig i en timme.

---

## Förfrågan

### HTTP-förfrågan

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Komponent | Värde |
|-----------|-------|
| **Metod** | `PUT` |
| **Sökväg** | `/cells/{name}` – `name` är önskat namn på den nyskapade arbetsboken (inklusive filändelse, t.ex. `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (vid skickande av datafil i meddelandekroppen). |
| **Accept** | `application/json` |

### Sökvägsparameter

| Namn | Typ | Obligatoriskt | Beskrivning |
|------|-----|---------------|-------------|
| `name` | sträng | **Ja** | Namnet på den arbetsbok som ska skapas (t.ex. `newworkbook.xlsx`). |

### Frågeparametrar

| Parameter | Typ | Obligatoriskt | Standard | Beskrivning |
|-----------|-----|---------------|----------|-------------|
| `templateFile` | sträng | Nej | — | Namnet på mallfilen som finns i molnet. |
| `dataFile` | sträng | Nej | — | Namnet på datafil (XML eller JSON) som finns i molnet. |
| `isWriteOver` | boolean | Nej | `false` | Skriv över målfilen om den redan finns. Skicka `true` eller `false` **utan** citationstecken. |
| `folder` | sträng | Nej | — | Mapp Sökväg där mallen (och valfri datafil) finns. |
| `storageName` | sträng | Nej | — | Namn på lagringstjänsten som innehåller filerna. |
| `checkExcelRestriction` | boolean | Nej | `true` | Validera arbetsboken mot Excel-begränsningar före skapande. |

### Meddelandekropp (valfritt)

När data för Smart‑Marker-platshållare skickas direkt i förfrågan inkluderas den som en multipart-fildel med namnet **`data`**.

| Delnamn | Typ | Beskrivning |
|---------|-----|-------------|
| `data` | fil | XML- eller JSON-fil som innehåller värden för Smart‑Marker. |

#### Exempel på cURL med meddelandekropp

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*Om frågeparametern `dataFile` används istället för multipart-meddelandekroppen utelämnas flaggan `-F`.*

---

## Svar

Ett lyckat anrop returnerar **`200 OK`** (eller **`201 Created`** när en ny fil genereras) med en JSON-struktur som beskriver den skapade arbetsboken.

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

### Datatyper för svar

| Egenskap | Typ | Beskrivning |
|----------|-----|-------------|
| `Code` | heltal | HTTP-liknande statuskod returnerad av API:et. |
| `Status` | sträng | Textuell beskrivning av statusen. |
| `File` | objekt | Detaljerad information om den genererade arbetsboken. |
| `File.Name` | sträng | Filnamn för den skapade arbetsboken. |
| `File.Size` | heltal | Storlek i byte. |
| `File.Path` | sträng | Relativ sökväg i lagringen. |
| `File.Url` | sträng | Direkt nedladdnings-URL (kräver samma JWT-token). |

---

**HTTP-statuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad | Ogiltig eller saknad JWT-token. |
| 413 | Meddelandekroppen är för stor | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel | Oväntat serverfel. |

---

## SDK-exempel

Följande kodfragment visar hur du anropar **PutWorkbookCreate** med de officiella Aspose.Cells Cloud SDK:erna.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | Det nya dokumentets namn.
var templateFile = "Calendar.xlsx"; // string | Mallfilens namn.
var dataFile = "Sample_Data.xml"; // string | Datafilens namn (valfritt).
var isWriteOver = true; // bool? | Skriv över om den redan finns.
var folder = "templates"; // string | Mapp där filerna finns.
var storageName = "MyStorage"; // string | Lagringsnamn.

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

## Felhantering

| Statuskod | Situation | Rekommenderad åtgärd |
|-----------|-----------|----------------------|
| **400** | Obligatoriska parametrar saknas eller ogiltig filtyp. | Kontrollera frågeparametrar, se till att mall- och datafiler finns och är av stödda typer (`.xlsx`, `.xml`, `.json`). |
| **401** | JWT-token saknas, har gått ut eller är felaktig. | Generera en ny åtkomsttoken med ditt Client Id/Secret. |
| **413** | Den uppladdade filen överskrider gränsen för tjänstens storlek (standard 50 MB). | Minska filens storlek eller dela upp arbetsboken i mindre delar. |
| **500** | Oväntat serverfel. | Försök igen efter en kort fördröjning; om problemet kvarstår, kontakta Aspose-supporten med värdet från `Request‑Id`-headern. |

---

## Se även

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Spara en befintlig arbetsbok i ett angivet format.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Hämta information om arbetsboken eller ladda ner filen.  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Ladda upp mall- eller datafiler till molnlagring.  

---