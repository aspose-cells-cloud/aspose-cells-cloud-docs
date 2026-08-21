---
---
title: "Come creare un foglio di calcolo Excel con un file modello"
second_title: "Documento"
linktitle: "File modello"
type: docs
url: /create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, modello, API, Aspose.Cells, foglio di calcolo, REST, Cloud"
description: "Scopri come generare fogli di calcolo Excel partendo da file modello utilizzando l'API REST di Aspose.Cells Cloud. Include prerequisiti, passaggi di autenticazione, esempi cURL, dettagli sulla gestione degli errori e frammenti di codice SDK."
weight: 30
---

# Come creare un foglio di calcolo Excel con un file modello

Crea un nuovo foglio di calcolo Excel utilizzando un file modello esistente e, opzionalmente, un file di dati che fornisce i valori per i marcatori intelligenti (*Smart‑Marker*). L'operazione viene eseguita tramite l'endpoint **PUT** `/cells/{name}` di Aspose.Cells Cloud.

---

## Prerequisiti

| Requisito | Descrizione |
|-----------|-------------|
| **Account Aspose.Cells Cloud** | Registrati su https://dashboard.aspose.cloud/ e ottieni un **Client Id** / **Client Secret**. |
| **Token di accesso JWT** | Genera un token JWT come descritto nella [guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **File modello** | Carica il file Excel modello (ad esempio, `Calendar.xlsx`) nello storage scelto utilizzando l'API **Upload File** o l'interfaccia utente. |
| **File di dati (opzionale)** | Un file JSON o XML contenente i valori per i marcatori intelligenti (ad esempio, `Sample_Data.xml`). |
| **Storage supportato** | Storage predefinito (`Default`) oppure uno storage personalizzato configurato nel tuo account Aspose. |

---

## Autenticazione

Tutte le richieste a Aspose.Cells Cloud richiedono un **token JWT Bearer** passato nell'intestazione `Authorization`:

```http
Authorization: Bearer {access_token}
```

Il token deve essere ottenuto in anticipo e ha una validità predefinita di un'ora.

---

## Richiesta

### Richiesta HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Componente | Valore |
|------------|--------|
| **Metodo** | `PUT` |
| **Percorso** | `/cells/{name}` – `name` è il nome desiderato del nuovo foglio di calcolo creato (inclusa l'estensione, ad esempio `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (quando un file di dati viene inviato nel corpo della richiesta). |
| **Accept** | `application/json` |

### Parametro di percorso

| Nome | Tipo | Obbligatorio | Descrizione |
|------|------|--------------|-------------|
| `name` | stringa | **Sì** | Nome del foglio di calcolo da creare (ad esempio, `newworkbook.xlsx`). |

### Parametri di query

| Parametro | Tipo | Obbligatorio | Default | Descrizione |
|-----------|------|--------------|---------|-------------|
| `templateFile` | stringa | No | — | Nome del file modello memorizzato nel cloud. |
| `dataFile` | stringa | No | — | Nome del file di dati (XML o JSON) memorizzato nel cloud. |
| `isWriteOver` | booleano | No | `false` | Sovrascrivi il file di destinazione se esiste già. Passa `true` o `false` **senza** virgolette. |
| `folder` | stringa | No | — | Percorso della cartella in cui risiede il modello (e facoltativamente il file di dati). |
| `storageName` | stringa | No | — | Nome del servizio di storage che contiene i file. |
| `checkExcelRestriction` | booleano | No | `true` | Convalida il foglio di calcolo contro le restrizioni di Excel prima della creazione. |

### Corpo della richiesta (opzionale)

Quando i dati per i segnaposto dei marcatori intelligenti vengono inviati direttamente nella richiesta, includili come parte di un file multipart denominata **`data`**.

| Nome parte | Tipo | Descrizione |
|------------|------|-------------|
| `data` | file | File XML o JSON contenente i valori per i marcatori intelligenti. |

#### Esempio cURL con corpo della richiesta

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*Se viene utilizzato invece il parametro di query `dataFile`, ometti il flag `-F`.*

---

## Risposta

Una chiamata riuscita restituisce un codice **`200 OK`** (o **`201 Created`** quando viene generato un nuovo file) insieme a un payload JSON che descrive il foglio di calcolo creato.

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

### Tipi di dati della risposta

| Proprietà | Tipo | Descrizione |
|-----------|------|-------------|
| `Code` | intero | Codice di stato simile all'HTTP restituito dall'API. |
| `Status` | stringa | Descrizione testuale dello stato. |
| `File` | oggetto | Dettagli del foglio di calcolo generato. |
| `File.Name` | stringa | Nome del file del foglio di calcolo creato. |
| `File.Size` | intero | Dimensione in byte. |
| `File.Path` | stringa | Percorso relativo nello storage. |
| `File.Url` | stringa | URL di download diretto (richiede lo stesso token JWT). |

---

**Codici di stato HTTP**

| Codice | Significato                     | Descrizione                                      |
|--------|---------------------------------|--------------------------------------------------|
| 200    | OK                              | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida            | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato                 | Token JWT non valido o mancante. |
| 413    | Payload troppo grande           | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server       | Errore imprevisto sul server. |
---

## Esempi SDK

I frammenti seguenti mostrano come richiamare **PutWorkbookCreate** utilizzando gli SDK ufficiali di Aspose.Cells Cloud.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | Nome del nuovo documento.
var templateFile = "Calendar.xlsx"; // string | Nome del file modello.
var dataFile = "Sample_Data.xml"; // string | Nome del file di dati (opzionale).
var isWriteOver = true; // bool? | Sovrascrivi se esiste.
var folder = "templates"; // string | Cartella in cui risiedono i file.
var storageName = "MyStorage"; // string | Nome dello storage.

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

## Gestione degli errori

| Codice di stato | Situazione | Azione consigliata |
|-----------------|------------|--------------------|
| **400** | Parametri obbligatori mancanti o tipo di file non valido. | Verifica i parametri di query, assicurati che i file modello e di dati esistano e siano supportati (`.xlsx`, `.xml`, `.json`). |
| **401** | Token JWT mancante, scaduto o non corretto. | Rigenera un nuovo token di accesso utilizzando il tuo Client Id/Secret. |
| **413** | File caricato supera il limite di dimensione del servizio (50 MB in modo predefinito). | Riduci le dimensioni del file o suddividi il foglio di calcolo in parti più piccole. |
| **500** | Errore imprevisto del server. | Riprova dopo un breve intervallo; se il problema persiste, contatta il supporto Aspose fornendo il valore dell'intestazione `Request‑Id`. |

---

## Vedi anche

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Salva un foglio di calcolo esistente in un formato specificato.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Recupera le informazioni del foglio di calcolo o scarica il file.  
- **[API Upload File](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Carica file modello o di dati nello storage cloud.  

---