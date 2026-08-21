---
title: "Aspose.Cells Cloud API – Aggiornamento dell’asse dei valori di un grafico (POST /valueaxis)"
description: "Aggiorna l’asse dei valori di un grafico in un foglio di calcolo Excel utilizzando l’API REST di Aspose.Cells Cloud. Include endpoint, parametri, schema del corpo della richiesta, esempi (cURL e SDK), risposte e gestione degli errori."
keywords:
  - Aspose.Cells Cloud
  - Aggiornamento asse dei valori del grafico
  - REST API
  - Asse del grafico Excel
  - POST valueaxis
  - Esempio cURL
  - SDK
  - Payload JSON
  - Impostazioni asse grafico
last_updated: 2026-07-30
---

# Aggiornamento dell’asse dei valori di un grafico (POST /valueaxis)

**Riepilogo:**  
Modifica l’asse dei valori di un grafico specifico in un libro Excel archiviato su Aspose Cloud. È possibile impostare limiti, unità di suddivisione, scala logaritmica e altre proprietà dell’asse in un’unica richiesta.

---

## Prerequisiti

1. **Token di accesso JWT** – ottieni un token come descritto nella [guida all’autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
2. Il **libro di lavoro** target deve essere già caricato nello storage Aspose Cloud (o nello storage predefinito).  
3. Conoscere il **nome del foglio di calcolo** e l’**indice del grafico in base zero** che si desidera modificare.

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*Sostituisci i segnaposto con i tuoi valori effettivi.*

| Segnaposto | Descrizione |
|------------|-------------|
| `{name}` | Nome del file Excel (es. `Book1.xlsx`). |
| `{sheetName}` | Foglio di calcolo contenente il grafico (es. `Sheet1`). |
| `{chartIndex}` | Indice in base zero del grafico (es. `0`). |

---

## Autenticazione

L’API utilizza l’**autenticazione basata su token JWT**. Includi il token nell’header `Authorization`:

```
Authorization: Bearer <token jwt>
```

---

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

## Parametri della richiesta

| Nome          | Posizione | Tipo   | Obbligatorio | Descrizione |
|---------------|-----------|--------|--------------|-------------|
| **name**      | Path      | string | Sì           | Nome del file Excel archiviato nel cloud. |
| **sheetName** | Path      | string | Sì           | Foglio di calcolo contenente il grafico. |
| **chartIndex**| Path      | int    | Sì           | Indice in base zero del grafico da aggiornare. |
| **axis**      | Body      | object | Sì           | Impostazioni dell’asse (vedi *Schema del corpo della richiesta*). |
| **folder**    | Query     | string | No           | Percorso della cartella cloud dove risiede il file. |
| **storageName**| Query    | string | No           | Nome del servizio di storage da utilizzare. |

---

## Schema del corpo della richiesta (oggetto `axis`)

Devono essere presenti solo le proprietà che desideri modificare.

| Proprietà      | Tipo    | Obbligatoria | Descrizione |
|----------------|---------|--------------|-------------|
| `minimum`      | number  | No           | Limite inferiore dell’asse. |
| `maximum`      | number  | No           | Limite superiore dell’asse. |
| `majorUnit`    | number  | No           | Intervallo tra le tacche principali. |
| `minorUnit`    | number  | No           | Intervallo tra le tacche secondarie. |
| `logBase`      | number  | No           | Base del logaritmo quando `isLogarithmic` è `true`. |
| `isLogarithmic`| boolean | No           | Indica se l’asse utilizza una scala logaritmica. |
| `displayUnit`  | string  | No           | Etichetta dell’unità visualizzata sull’asse (es. `"Thousands"`). |
| `tickMark`     | string  | No           | Stile delle tacche (`"inside"`, `"outside"`, ecc.). |
| `crossAt`      | number  | No           | Posizione in cui l’asse interseca l’asse perpendicolare. |

### Esempio di corpo della richiesta

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## Esempi di richieste

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Units",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### Esempi di SDK  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Units",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Status: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Asse dei valori aggiornato.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Units',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Asse dei valori aggiornato.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Units',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Asse dei valori aggiornato.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Units',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Asse dei valori aggiornato.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Esempio Node.js
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Units',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Asse dei valori aggiornato.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Esempio Android (Java)
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Units"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Errore: \\(error)")
    } else {
        print("Asse dei valori aggiornato.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Units',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Asse dei valori aggiornato.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Units",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Errore:", err)
    } else {
        fmt.Println("Asse dei valori aggiornato.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## Risposte

### Esito positivo (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Il tipo di risposta è `CellsCloudResponse`.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |
---

## Risorse aggiuntive

- **Specifiche OpenAPI** – [Visualizza / scarica JSON‑YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **Repository SDK** – <https://github.com/aspose-cells-cloud>  
- **Guida all’autenticazione** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*Per eventuali domande o feedback, contatta il team di supporto di Aspose.Cells Cloud.*
---