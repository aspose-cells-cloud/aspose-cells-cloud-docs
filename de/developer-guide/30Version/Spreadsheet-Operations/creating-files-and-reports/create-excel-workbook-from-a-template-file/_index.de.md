---
title: "So erstellen Sie eine Excel-Arbeitsmappe mit einer Vorlagendatei"
second_title: "Dokument"
linktitle: "Vorlagendatei"
type: docs
url: /create-an-excel-file-with-template-file/
aliases:
  - /create-excel-workbook-from-a-template-file/
  - /workbook/new-from-a-template-file/
  - /workbook/create/template-file/
keywords: "Excel, Vorlage, API, Aspose.Cells, Arbeitsmappe, REST, Cloud"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mithilfe von Vorlagendateien über die Aspose.Cells Cloud REST API generieren. Enthält Voraussetzungen, Authentifizierungsschritte, cURL-Beispiele, Details zur Fehlerbehandlung sowie SDK-Code-Snippets."
weight: 30
---

# So erstellen Sie eine Excel-Arbeitsmappe mit einer Vorlagendatei

Erstellen Sie eine neue Excel-Arbeitsmappe mithilfe einer vorhandenen Vorlagendatei und optional einer Datendatei, die Smart‑Marker‑Werte bereitstellt. Der Vorgang wird über den **PUT**-Endpunkt `/cells/{name}` von Aspose.Cells Cloud durchgeführt.

---

## Voraussetzungen

| Anforderung | Beschreibung |
|-------------|-------------|
| **Aspose.Cells Cloud-Konto** | Registrieren Sie sich unter https://dashboard.aspose.cloud/ und erhalten Sie eine **Client‑Id** / **Client‑Secret**. |
| **JWT-Zugriffstoken** | Generieren Sie ein JWT-Token gemäß der [Authentifizierungsanleitung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Vorlagendatei** | Laden Sie die Vorlagendatei (z. B. `Calendar.xlsx`) mithilfe der **Upload File**-API oder der Benutzeroberfläche in den gewählten Speicher hoch. |
| **Datendatei (optional)** | Eine JSON- oder XML-Datei, die Smart‑Marker‑Werte enthält (z. B. `Sample_Data.xml`). |
| **Unterstützter Speicher** | Standardspeicher (`Default`) oder ein benutzerdefinierter Speicher, der in Ihrem Aspose-Konto konfiguriert ist. |

---

## Authentifizierung

Alle Anforderungen an Aspose.Cells Cloud erfordern ein **Bearer JWT-Token**, das im `Authorization`-Header übergeben wird:

```http
Authorization: Bearer {access_token}
```

Das Token muss zuvor abgerufen werden und ist standardmäßig eine Stunde lang gültig.

---

## Anforderung

### HTTP-Anforderung

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

| Komponente | Wert |
|-----------|-------|
| **Methode** | `PUT` |
| **Pfad**   | `/cells/{name}` – `name` ist der gewünschte Name der neu erstellten Arbeitsmappe (einschließlich Erweiterung, z. B. `newworkbook.xlsx`). |
| **Content‑Type** | `multipart/form-data` (falls eine Datendatei im Körper gesendet wird). |
| **Accept** | `application/json` |

### Pfadparameter

| Name | Typ | Erforderlich | Beschreibung |
|------|-----|--------------|-------------|
| `name` | Zeichenkette | **Ja** | Der Name der zu erstellenden Arbeitsmappe (z. B. `newworkbook.xlsx`). |

### Abfrageparameter

| Parameter | Typ | Erforderlich | Standardwert | Beschreibung |
|-----------|-----|--------------|--------------|-------------|
| `templateFile` | Zeichenkette | Nein | — | Name der Vorlagendatei im Cloud-Speicher. |
| `dataFile` | Zeichenkette | Nein | — | Name der Datendatei (XML oder JSON) im Cloud-Speicher. |
| `isWriteOver` | Boolean | Nein | `false` | Überschreiben der Zieldatei, falls sie bereits vorhanden ist. Übergeben Sie `true` oder `false` **ohne** Anführungszeichen. |
| `folder` | Zeichenkette | Nein | — | Ordnerpfad, in dem sich die Vorlage (und optional die Datendatei) befindet. |
| `storageName` | Zeichenkette | Nein | — | Name des Speicherdiensts, der die Dateien enthält. |
| `checkExcelRestriction` | Boolean | Nein | `true` | Überprüfen Sie die Arbeitsmappe vor der Erstellung auf Excel-Beschränkungen. |

### Anforderungstext (optional)

Wenn die Daten für Smart‑Marker-Platzhalter direkt in der Anforderung gesendet werden, fügen Sie sie als Multipart-Dateiteil mit dem Namen **`data`** ein.

| Teilname | Typ | Beschreibung |
|----------|-----|-------------|
| `data` | Datei | XML- oder JSON-Datei, die Smart‑Marker‑Werte enthält. |

#### Beispiel-cURL mit Anforderungstext

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&isWriteOver=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "data=@Sample_Data.xml"
```

*Falls stattdessen der Abfrageparameter `dataFile` verwendet wird, lassen Sie das `-F`-Flag weg.*

---

## Antwort

Ein erfolgreicher Aufruf gibt einen **`200 OK`**- (oder **`201 Created`**-Status bei Erstellung einer neuen Datei) mit einer JSON-Antwort zurück, die die erstellte Arbeitsmappe beschreibt.

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

### Antwortdatentypen

| Eigenschaft | Typ | Beschreibung |
|-------------|-----|-------------|
| `Code` | Ganzzahl | HTTP-ähnlicher Statuscode, der von der API zurückgegeben wird. |
| `Status` | Zeichenkette | Textuelle Beschreibung des Status. |
| `File` | Objekt | Details der erstellten Arbeitsmappe. |
| `File.Name` | Zeichenkette | Dateiname der erstellten Arbeitsmappe. |
| `File.Size` | Ganzzahl | Größe in Bytes. |
| `File.Path` | Zeichenkette | Relativer Pfad im Speicher. |
| `File.Url` | Zeichenkette | Direkte Download-URL (erfordert dasselbe JWT-Token). |

---

**HTTP-Statuscodes**

| Code | Bedeutung | Beschreibung |
|------|-----------|--------------|
| 200  | OK | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert | Ungültiges oder fehlendes JWT-Token. |
| 413  | Anforderungstext zu groß | Hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler. |
---

## SDK-Beispiele

Die folgenden Code-Snippets zeigen, wie **PutWorkbookCreate** mit den offiziellen Aspose.Cells Cloud SDKs aufgerufen wird.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System.IO;

var apiInstance = new WorkbookApi();
var name = "newworkbook.xlsx"; // string | Der Name des neuen Dokuments.
var templateFile = "Calendar.xlsx"; // string | Name der Vorlagendatei.
var dataFile = "Sample_Data.xml"; // string | Name der Datendatei (optional).
var isWriteOver = true; // bool? | Überschreiben, falls vorhanden.
var folder = "templates"; // string | Ordner, in dem sich die Dateien befinden.
var storageName = "MyStorage"; // string | Speichername.

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

## Fehlerbehandlung

| Statuscode | Situation | Empfohlene Aktion |
|------------|-----------|-------------------|
| **400** | Erforderliche Parameter fehlen oder ungültiger Dateityp. | Überprüfen Sie die Abfrageparameter, stellen Sie sicher, dass Vorlage und Datendatei vorhanden sind und unterstützt werden (`.xlsx`, `.xml`, `.json`). |
| **401** | JWT-Token fehlt, ist abgelaufen oder falsch formatiert. | Generieren Sie ein neues Zugriffstoken mithilfe Ihrer Client‑Id/Client‑Secret. |
| **413** | Hochgeladene Datei überschreitet das Service-Größenlimit (Standard: 50 MB). | Reduzieren Sie die Dateigröße oder teilen Sie die Arbeitsmappe in kleinere Teile auf. |
| **500** | Unerwarteter Serverfehler. | Wiederholen Sie den Vorgang nach kurzer Verzögerung; falls das Problem bestehen bleibt, wenden Sie sich an den Aspose-Support mit dem Wert des `Request‑Id`-Headers. |

---

## Siehe auch

- **[PutWorkbookSave](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookSave)** – Speichern einer vorhandenen Arbeitsmappe in einem bestimmten Format.  
- **[GetWorkbook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbook)** – Abrufen von Arbeitsmappeninformationen oder Herunterladen der Datei.  
- **[Upload File API](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)** – Hochladen von Vorlagen- oder Datendateien in den Cloud-Speicher.  

---
---