---
title: "Arbeitsblattkommentar hinzufügen"
description: "Fügen Sie mithilfe der Aspose.Cells Cloud REST API (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}) einen Kommentar zu einer bestimmten Zelle in einem Excel-Arbeitsblatt hinzu."
keywords: "Aspose.Cells, Cloud-API, Arbeitsblattkommentar hinzufügen, Excel, Tabellenkalkulation, Zellkommentar"
weight: 20
api_version: "v3.0"
---

# Arbeitsblattkommentar hinzufügen

Fügen Sie mithilfe der Aspose.Cells Cloud REST API einen Kommentar zu einer bestimmten Zelle in einem Arbeitsblatt einer Excel-Arbeitsmappe hinzu.

---

## Voraussetzungen / Authentifizierung

* Für jede Anfrage ist ein **Bearer JWT-Token** erforderlich.  
  *Holen Sie sich ein Token* über den **/connect/token**-Endpunkt (siehe [Authentifizierungsanleitung](/cells/authentication/)).  
* Fügen Sie das Token in den `Authorization`-Header ein:

```http
Authorization: Bearer <jwt token>
```

* Alle Aufrufe müssen über **HTTPS** erfolgen, um Token und Daten zu schützen.

---

## HTTP-Anfrage

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Pfadparameter

| Name      | Typ    | Erforderlich | Beschreibung |
|-----------|--------|------------|-------------|
| `name`    | Zeichenkette | ✔️ | Der Name der Arbeitsmappendatei (z. B. `test.xlsx`). |
| `sheetName` | Zeichenkette | ✔️ | Der Name des Arbeitsblatts (z. B. `Sheet1`). |
| `cellName` | Zeichenkette | ✔️ | Die Adresse der Zielzelle (z. B. `A1`). |

### Abfrageparameter

| Name        | Typ    | Erforderlich | Beschreibung |
|-------------|--------|------------|-------------|
| `folder`    | Zeichenkette | optional | Der Ordner, der die Arbeitsmappe enthält. |
| `storageName` | Zeichenkette | optional | Der Name des Speicherdiensts, in dem sich die Datei befindet. |

### Anforderungstext

Der Text muss ein **Comment**-Objekt im JSON-Format enthalten.

```json
{
  "CellName": "A1",
  "Author": "string",
  "HtmlNote": "string",
  "Note": "string",
  "AutoSize": true,
  "IsVisible": true,
  "Width": 10,
  "Height": 10,
  "TextHorizontalAlignment": "Left",
  "TextOrientationType": "NoRotation",
  "TextVerticalAlignment": "Top"
}
```

**Felder des Comment-Objekts**

| Feld                      | Typ     | Erforderlich | Beschreibung |
|---------------------------|---------|------------|-------------|
| `CellName`                | Zeichenkette | ✔️ | Zelladresse (muss mit dem Wert des Pfadparameters `{cellName}` übereinstimmen). |
| `Author`                  | Zeichenkette | optional | Name des Kommentarautors. |
| `HtmlNote`                | Zeichenkette | optional | HTML-formatierter Kommentartext. |
| `Note`                    | Zeichenkette | optional | Reintext-Kommentar. |
| `AutoSize`                | Boolean | optional | Automatische Größenanpassung des Kommentarfelds. |
| `IsVisible`               | Boolean | optional | Kommentar standardmäßig anzeigen. |
| `Width` / `Height`        | Zahl    | optional | Größe des Kommentarfelds (in Punkten). |
| `TextHorizontalAlignment`| Zeichenkette | optional | Horizontale Ausrichtung (`Left`, `Center`, `Right`). |
| `TextOrientationType`     | Zeichenkette | optional | Textausrichtung (`NoRotation`, `Rotate90`, …). |
| `TextVerticalAlignment`  | Zeichenkette | optional | Vertikale Ausrichtung (`Top`, `Center`, `Bottom`). |

---

## cURL-Beispiel

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "A1",
        "Author": "test",
        "HtmlNote": "<font style=\"font-weight:bold;font-family:Tahoma;font-size:9pt;color:#000000;text-align:left;\">this is a comment</font>",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10,
        "TextHorizontalAlignment": "Left",
        "TextOrientationType": "NoRotation",
        "TextVerticalAlignment": "Top"
      }'
```

---

## Antwort-Schema

| Feld    | Typ    | Beschreibung |
|---------|--------|-------------|
| `Comment` | Objekt | Das erstellte Kommentarobjekt (siehe oben **Felder des Comment-Objekts**, plus Link-Metadaten). |
| `Code`   | Ganzzahl | Vom API zurückgegebener HTTP-Statuscode (z. B. `200`). |
| `Status` | Zeichenkette | Textuelle Statusmeldung (z. B. `"OK"`). |

Das `Comment`-Objekt enthält zudem ein Unterobjekt **link**:

| Untereigenschaft | Typ    | Beschreibung |
|------------------|--------|-------------|
| `Href`           | Zeichenkette | Selbstreferenz-URL für die Kommentarressource. |
| `Rel`            | Zeichenkette | Beziehungstyp (`self`). |
| `Title`          | Zeichenkette | Optionaler Titel (kann `null` sein). |
| `Type`           | Zeichenkette | Optionaler MIME-Typ (kann `null` sein). |

---

## Erfolgreiches Antwortbeispiel

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "test",
    "HtmlNote": "<Font Style=\"FONT-WEIGHT: bold;FONT-FAMILY: Tahoma;FONT-SIZE: 9pt;COLOR: #000000;TEXT-ALIGN: left;\">this is a comment</Font>",
    "Note": "this is a comment",
    "AutoSize": true,
    "IsVisible": true,
    "Width": 10,
    "Height": 10,
    "TextHorizontalAlignment": "Left",
    "TextOrientationType": "NoRotation",
    "TextVerticalAlignment": "Top",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/comments/A1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Fehlerantworten

| HTTP-Code | Beschreibung | Beispiel |
|-----------|-------------|---------|
| **400**   | Ungültige Anfrage – fehlende oder ungültige Parameter. | `{ "Error": { "Code": "InvalidParameter", "Message": "Der Parameter 'cellName' fehlt oder ist fehlerhaft." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | Nicht autorisiert – Token fehlt oder ist ungültig. | `{ "Error": { "Code": "InvalidToken", "Message": "Authentifizierung fehlgeschlagen." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**   | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Zelle existiert nicht. | `{ "Error": { "Code": "FileNotFound", "Message": "Arbeitsmappe 'test.xlsx' nicht gefunden." }, "Code": 404, "Status": "Not Found" }` |
| **500**   | Interner Serverfehler – unerwarteter Zustand auf dem Server. | `{ "Error": { "Code": "ServerError", "Message": "Ein unerwarteter Fehler ist aufgetreten." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## SDK-Beispiele

Die folgenden SDKs bieten vorgefertigte Wrapper für diesen Vorgang. Ersetzen Sie Platzhalterwerte (`<YOUR_TOKEN>`, `<FILE_NAME>` usw.) durch echte Daten.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// API-Client konfigurieren
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Kommentarobjekt vorbereiten
var comment = new Comment
{
    CellName = "A1",
    Author = "test",
    Note = "this is a comment",
    HtmlNote = "<font style=\"font-weight:bold;\">this is a comment</font>",
    AutoSize = true,
    IsVisible = true,
    Width = 10,
    Height = 10
};

try
{
    var response = apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, folder: null, storageName: null);
    Console.WriteLine(response);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling WorksheetsApi.PutWorksheetComment: " + e.Message );
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.*;
import com.aspose.cells.cloud.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

WorksheetsApi worksheetsApi = new WorksheetsApi(client);

Comment comment = new Comment()
        .cellName("A1")
        .author("test")
        .note("this is a comment")
        .htmlNote("<font style=\"font-weight:bold;\">this is a comment</font>")
        .autoSize(true)
        .isVisible(true)
        .width(10)
        .height(10);

try {
    CommentResponse resp = worksheetsApi.putWorksheetComment("test.xlsx", "Sheet1", "A1", comment, null, null);
    System.out.println(resp);
} catch (ApiException e) {
    e.printStackTrace();
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<your_client_id>');
$config->setAppKey('<your_client_secret>');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

$comment = new Aspose\Cells\Model\Comment([
    'CellName' => 'A1',
    'Author'   => 'test',
    'Note'     => 'this is a comment',
    'HtmlNote' => '<font style="font-weight:bold;">this is a comment</font>',
    'AutoSize' => true,
    'IsVisible'=> true,
    'Width'    => 10,
    'Height'   => 10
]);

try {
    $result = $apiInstance->putWorksheetComment('test.xlsx', 'Sheet1', 'A1', $comment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = AsposeCellsCloud::WorksheetsApi.new

comment = AsposeCellsCloud::Comment.new(
  cell_name: 'A1',
  author: 'test',
  note: 'this is a comment',
  html_note: '<font style="font-weight:bold;">this is a comment</font>',
  auto_size: true,
  is_visible: true,
  width: 10,
  height: 10
)

begin
  result = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
  puts result
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling WorksheetsApi->put_worksheet_comment: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const { WorksheetsApi, Configuration, Comment } = require('asposecellscloud');

let config = new Configuration();
config.clientId = '<your_client_id>';
config.clientSecret = '<your_client_secret>';

let api = new WorksheetsApi(config);

let comment = new Comment({
  CellName: 'A1',
  Author: 'test',
  Note: 'this is a comment',
  HtmlNote: '<font style="font-weight:bold;">this is a comment</font>',
  AutoSize: true,
  IsVisible: true,
  Width: 10,
  Height: 10
});

api.putWorksheetComment('test.xlsx', 'Sheet1', 'A1', comment)
  .then(response => console.log(response))
  .catch(err => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.models import Comment

config = asposecellscloud.Configuration()
config.client_id = '<your_client_id>'
config.client_secret = '<your_client_secret>'

api_instance = asposecellscloud.WorksheetsApi(asposecellscloud.ApiClient(config))

comment = Comment(
    CellName='A1',
    Author='test',
    Note='this is a comment',
    HtmlNote='<font style="font-weight:bold;">this is a comment</font>',
    AutoSize=True,
    IsVisible=True,
    Width=10,
    Height=10
)

try:
    api_response = api_instance.put_worksheet_comment('test.xlsx', 'Sheet1', 'A1', comment)
    print(api_response)
except ApiException as e:
    print("Exception when calling WorksheetsApi->put_worksheet_comment: %s\\n" % e)
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Object::Comment;

my $config = AsposeCellsCloud::Configuration->new(
    client_id     => '<your_client_id>',
    client_secret => '<your_client_secret>'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $comment = AsposeCellsCloud::Object::Comment->new(
    CellName => 'A1',
    Author   => 'test',
    Note     => 'this is a comment',
    HtmlNote => '<font style="font-weight:bold;">this is a comment</font>',
    AutoSize => 1,
    IsVisible=> 1,
    Width    => 10,
    Height   => 10
);

eval {
    my $result = $api_instance->put_worksheet_comment(
        name      => 'test.xlsx',
        sheet_name=> 'Sheet1',
        cell_name => 'A1',
        comment   => $comment
    );
    print $result;
};
if ($@) {
    warn "Exception when calling WorksheetsApi->put_worksheet_comment: $@";
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/model"
)

func main() {
    cfg := cellscloud.NewConfiguration()
    cfg.ClientId = "<your_client_id>"
    cfg.ClientSecret = "<your_client_secret>"

    apiInstance := api.NewWorksheetsApi(cfg)

    comment := model.Comment{
        CellName: "A1",
        Author:   "test",
        Note:     "this is a comment",
        HtmlNote: "<font style=\"font-weight:bold;\">this is a comment</font>",
        AutoSize: true,
        IsVisible: true,
        Width: 10,
        Height: 10,
    }

    resp, _, err := apiInstance.PutWorksheetComment("test.xlsx", "Sheet1", "A1", comment, nil, nil)
    if err != nil {
        fmt.Printf("Error: %v\\n", err)
    } else {
        fmt.Printf("Response: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Siehe auch

* **Arbeitsblattkommentar abrufen** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Arbeitsblattkommentar aktualisieren** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Arbeitsblattkommentar löschen** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Alle Kommentare löschen** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## Zusätzliche Hinweise

* Der Endpunktpfad enthält **v3.0**. Eine neuere Version (**v3.1**) ist verfügbar; aktualisieren Sie die Basis-URL entsprechend, wenn Sie die neuesten Funktionen benötigen.  
* Für die vollständige OpenAPI-Definition besuchen Sie die [Aspose.Cells Cloud API-Referenz](/cells/#/Worksheets/PutWorksheetComment).  
* Denken Sie daran, die Ratenbegrenzung (HTTP 429) gemäß den API-Richtlinien zu behandeln und entsprechend zu retryen.  

---  
---