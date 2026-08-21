---
---
title: Aggiungi CellArea alla Formattazione Condizionale
description: Aggiungi un'area di celle a una regola di formattazione condizionale in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempi cURL e SDK, schema di risposta e gestione degli errori.
keywords: Aspose.Cells, Formattazione Condizionale, CellArea, REST API, Excel, Cloud SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Aggiungi CellArea alla Formattazione Condizionale

**Riepilogo** – Aggiunge un'area di celle a una regola esistente di formattazione condizionale in un foglio di calcolo.

---

## Prerequisiti

1. **Account Aspose.Cells Cloud** – Ottieni il tuo **App SID** e **App Key**.  
2. **Token JWT** – Genera un token JWT utilizzando App SID/App Key (vedi la [guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. Il file Excel di destinazione deve già esistere nello storage/cartella specificato.

---

## Autenticazione

Tutte le chiamate richiedono **autenticazione basata su token JWT**. Passa il token nell'header `Authorization`:

```http
Authorization: Bearer <jwt token>
```

---

## Richiesta HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Parametri del percorso

| Nome      | Tipo   | Descrizione                                      |
|-----------|--------|--------------------------------------------------|
| `name`    | string | Nome del file Excel (es. `Book1.xlsx`).         |
| `sheetName`| string| Nome del foglio di calcolo contenente la regola (es. `Sheet1`). |
| `index`   | integer| Indice in base zero della regola di formattazione condizionale. |

### Parametri di query

| Nome        | Tipo   | Obbligatorio | Descrizione                                      |
|-------------|--------|--------------|--------------------------------------------------|
| `cellArea`  | string | **Sì**       | Intervallo di celle da aggiungere, in notazione A1 (es. `A1:C3`). |
| `folder`    | string | No           | Percorso della cartella in cui è memorizzato il file. |
| `storageName`| string| No           | Nome del servizio di storage.                   |

---

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Risposta prevista in caso di successo

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Schema della risposta – `CellArea`**

| Proprietà     | Tipo | Descrizione                                      |
|---------------|------|--------------------------------------------------|
| `StartRow`    | int  | Indice in base zero della prima riga.            |
| `StartColumn` | int  | Indice in base zero della prima colonna.         |
| `EndRow`      | int  | Indice in base zero dell'ultima riga.            |
| `EndColumn`   | int  | Indice in base zero dell'ultima colonna.         |

---

**Codici di stato HTTP**

| Codice | Significato              | Descrizione                                                  |
|--------|--------------------------|--------------------------------------------------------------|
| 200    | OK                       | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida     | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato          | Token JWT non valido o mancante.                             |
| 413    | Payload troppo grande    | Il file caricato supera il limite di dimensione.             |
| 500    | Errore interno del server| Errore imprevisto del server.                                |
---

## Esempi di SDK

Di seguito sono riportati brevi frammenti per gli SDK più comuni. Sostituisci `YOUR_APP_SID` e `YOUR_APP_KEY` con le tue credenziali e imposta il token JWT generato dove richiesto.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Note e suggerimenti

- **Formato CellArea** – Deve essere un intervallo A1 valido (`A1`, `A1:C3`, `Sheet2!B2:D5`). I formati non validi restituiscono **400 Bad Request**.
- **Aree sovrapposte** – Aggiungere un intervallo che si sovrappone a un'area esistente della stessa regola genera **409 Conflict**.
- **Indicizzazione in base zero** – Gli indici di riga/colonna nella risposta iniziano da `0`. Convertili nella notazione in base 1 di Excel se necessario.
- **Storage** – Se ometti `folder` e `storageName`, l'API utilizza lo storage predefinito o la cartella principale.

---

## Operazioni correlate

- **Elimina area di celle** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Aggiungi condizione alla formattazione condizionale** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Ottieni formattazione condizionale** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

Queste operazioni possono essere combinate per costruire flussi di lavoro completi di formattazione condizionale.

---
---