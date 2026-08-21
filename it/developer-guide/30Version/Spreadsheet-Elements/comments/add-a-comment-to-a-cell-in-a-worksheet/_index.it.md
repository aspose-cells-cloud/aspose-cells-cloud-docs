---
---
title: "Aggiungi commento al foglio di calcolo"
description: "Aggiungi un commento a una cella specifica in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (PUT /v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName})."
keywords: "Aspose.Cells, API cloud, aggiungi commento al foglio di calcolo, Excel, foglio di calcolo, commento cella"
weight: 20
api_version: "v3.0"
---

# Aggiungi commento al foglio di calcolo

Aggiungi un commento a una cella specifica in un foglio di calcolo di un workbook Excel utilizzando l'API REST Aspose.Cells Cloud.

---

## Prerequisiti / Autenticazione

* È richiesto un **token Bearer JWT** per ogni richiesta.  
  *Ottieni un token* tramite l'endpoint **/connect/token** (vedi la [guida all'autenticazione](/cells/authentication/)).  
* Includi il token nell'header `Authorization`:

```http
Authorization: Bearer <jwt token>
```

* Tutte le chiamate devono essere effettuate tramite **HTTPS** per proteggere il token e i dati.

---

## Richiesta HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Parametri del percorso

| Nome      | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|------------|-------------|
| `name`    | string | ✔️ | Nome del file del workbook (es. `test.xlsx`). |
| `sheetName` | string | ✔️ | Nome del foglio di calcolo (es. `Sheet1`). |
| `cellName` | string | ✔️ | Indirizzo della cella di destinazione (es. `A1`). |

### Parametri di query

| Nome        | Tipo   | Obbligatorio | Descrizione |
|-------------|--------|------------|-------------|
| `folder`    | string | facoltativo | Cartella contenente il workbook. |
| `storageName` | string | facoltativo | Nome del servizio di archiviazione in cui si trova il file. |

### Corpo della richiesta

Il corpo deve contenere un oggetto **Comment** in formato JSON.

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

**Campi dell'oggetto Comment**

| Campo                     | Tipo    | Obbligatorio | Descrizione |
|---------------------------|---------|------------|-------------|
| `CellName`                | string  | ✔️ | Indirizzo della cella (deve corrispondere al valore `{cellName}` del percorso). |
| `Author`                  | string  | facoltativo | Nome dell'autore del commento. |
| `HtmlNote`                | string  | facoltativo | Testo del commento in formato HTML. |
| `Note`                    | string  | facoltativo | Testo del commento in formato testo semplice. |
| `AutoSize`                | boolean | facoltativo | Ridimensiona automaticamente il riquadro del commento. |
| `IsVisible`               | boolean | facoltativo | Mostra il commento per impostazione predefinita. |
| `Width` / `Height`        | number  | facoltativo | Dimensioni del riquadro del commento (in punti). |
| `TextHorizontalAlignment`| string  | facoltativo | Allineamento orizzontale (`Left`, `Center`, `Right`). |
| `TextOrientationType`     | string  | facoltativo | Rotazione del testo (`NoRotation`, `Rotate90`, ecc.). |
| `TextVerticalAlignment`  | string  | facoltativo | Allineamento verticale (`Top`, `Center`, `Bottom`). |

---

## Esempio cURL

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

## Schema della risposta

| Campo   | Tipo   | Descrizione |
|---------|--------|-------------|
| `Comment` | object | Oggetto commento creato (vedi **Campi dell'oggetto Comment** sopra, più metadati del link). |
| `Code`   | integer | Codice di stato HTTP restituito dall'API (es. `200`). |
| `Status` | string  | Messaggio di stato in formato testo (es. `"OK"`). |

L'oggetto `Comment` contiene inoltre un sottoolgetto **link**:

| Sottocampo | Tipo   | Descrizione |
|------------|--------|-------------|
| `Href`    | string | URL di riferimento a se stesso per la risorsa commento. |
| `Rel`     | string | Tipo di relazione (`self`). |
| `Title`   | string | Titolo facoltativo (può essere `null`). |
| `Type`    | string | Tipo MIME facoltativo (può essere `null`). |

---

## Esempio di risposta con successo

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

## Risposte di errore

| Codice HTTP | Descrizione | Esempio |
|-------------|-------------|---------|
| **400**   | Richiesta non valida – parametri mancanti o non validi. | `{ "Error": { "Code": "InvalidParameter", "Message": "Il parametro 'cellName' è mancante o malformato." }, "Code": 400, "Status": "Bad Request" }` |
| **401**   | Non autorizzato – token mancante o non valido. | `{ "Error": { "Code": "InvalidToken", "Message": "Autenticazione fallita." }, "Code": 401, "Status": "Unauthorized" }` |
| **404**   | Non trovato – workbook, foglio di calcolo o cella inesistenti. | `{ "Error": { "Code": "FileNotFound", "Message": "Workbook 'test.xlsx' non trovato." }, "Code": 404, "Status": "Not Found" }` |
| **500**   | Errore interno del server – condizione imprevista sul server. | `{ "Error": { "Code": "ServerError", "Message": "Si è verificato un errore imprevisto." }, "Code": 500, "Status": "Internal Server Error" }` |

---

## Esempi SDK

I seguenti SDK forniscono wrapper già pronti per questa operazione. Sostituisci i valori segnaposto (`<YOUR_TOKEN>`, `<FILE_NAME>`, ecc.) con dati reali.

{{< tabs tabTotal="8" tabID="sdk" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Configura il client API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new WorksheetsApi(config);

// Prepara l'oggetto commento
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
    Console.WriteLine("Eccezione durante la chiamata a WorksheetsApi.PutWorksheetComment: " + e.Message );
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
    echo 'Eccezione durante la chiamata a WorksheetsApi->putWorksheetComment: ', $e->getMessage(), PHP_EOL;
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
  puts "Eccezione durante la chiamata a WorksheetsApi->put_worksheet_comment: #{e}"
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
    print("Eccezione durante la chiamata a WorksheetsApi->put_worksheet_comment: %s\\n" % e)
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
    warn "Eccezione durante la chiamata a WorksheetsApi->put_worksheet_comment: $@";
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
        fmt.Printf("Errore: %v\\n", err)
    } else {
        fmt.Printf("Risposta: %+v\\n", resp)
    }
}
```

{{< /tab >}}

{{< /tabs >}}

---

## Vedi anche

* **Ottieni commento del foglio di calcolo** – `GET /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Aggiorna commento del foglio di calcolo** – `POST /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Elimina commento del foglio di calcolo** – `DELETE /cells/{name}/worksheets/{sheetName}/comments/{cellName}`  
* **Cancella tutti i commenti** – `DELETE /cells/{name}/worksheets/{sheetName}/comments`  

---

## Note aggiuntive

* Il percorso dell'endpoint include **v3.0**. Una versione più recente (**v3.1**) è disponibile; aggiorna l'URL di base di conseguenza se hai bisogno delle funzionalità più recenti.  
* Per la definizione completa OpenAPI, visita il [riferimento API Aspose.Cells Cloud](/cells/#/Worksheets/PutWorksheetComment).  
* Ricorda di gestire il rate limiting (HTTP 429) e di effettuare nuovamente le richieste secondo le linee guida dell'API.  

---
---