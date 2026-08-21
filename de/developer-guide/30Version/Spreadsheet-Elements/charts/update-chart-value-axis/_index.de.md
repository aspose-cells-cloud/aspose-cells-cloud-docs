---
title: "Aspose.Cells Cloud API – Wertachse eines Diagramms aktualisieren (POST /valueaxis)"
description: "Aktualisieren Sie die Wertachse eines Diagramms in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Enthält Endpunkt, Parameter, Anforderungstext-Schema, Beispiele (cURL und SDKs), Antworten und Fehlerbehandlung."
keywords:
  - Aspose.Cells Cloud
  - Diagrammwertachse aktualisieren
  - REST API
  - Excel-Diagramm-Achse
  - POST valueaxis
  - cURL-Beispiel
  - SDK
  - JSON-Payload
  - Diagramm-Achsen-Einstellungen
last_updated: 2026-07-30
---

# Diagrammwertachse aktualisieren (POST /valueaxis)

**Zusammenfassung:**  
Ändern Sie die Wertachse eines bestimmten Diagramms in einer Excel-Arbeitsmappe, die in Aspose Cloud gespeichert ist. Sie können Grenzwerte, Tick-Intervalle, logarithmische Skalierung und andere Achseneigenschaften in einer einzigen Anforderung festlegen.

---

## Voraussetzungen

1. **JWT-Zugriffstoken** – Holen Sie sich ein Token wie in der [Authentifizierungsanleitung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) beschrieben.  
2. Die Ziel-**Arbeitsmappe** muss bereits in den Aspose Cloud-Speicher (oder den Standard-Speicher) hochgeladen sein.  
3. Kennt den **Arbeitsblattnamen** und den **nullbasierten Diagrammindex**, den Sie ändern möchten.

---

## Endpunkt

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*Ersetzen Sie die Platzhalter durch Ihre tatsächlichen Werte.*

| Platzhalter | Beschreibung |
|-------------|-------------|
| `{name}` | Name der Excel-Datei (z. B. `Book1.xlsx`). |
| `{sheetName}` | Arbeitsblatt, das das Diagramm enthält (z. B. `Sheet1`). |
| `{chartIndex}` | Nullbasierter Index des Diagramms (z. B. `0`). |

---

## Authentifizierung

Die API verwendet eine **JWT-Token-basierte Authentifizierung**. Geben Sie das Token im `Authorization`-Header an:

```
Authorization: Bearer <jwt token>
```

---

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## Anforderungsparameter

| Name          | Speicherort | Typ    | Erforderlich | Beschreibung |
|---------------|-------------|--------|--------------|-------------|
| **name**      | Pfad        | string | Ja           | Name der Excel-Datei im Cloud-Speicher. |
| **sheetName** | Pfad        | string | Ja           | Arbeitsblatt, das das Diagramm enthält. |
| **chartIndex**| Pfad        | int    | Ja           | Nullbasierter Index des zu aktualisierenden Diagramms. |
| **axis**      | Textkörper  | object | Ja           | Achseneinstellungen (siehe *Anforderungstext-Schema*). |
| **folder**    | Abfrage     | string | Nein         | Cloud-Ordnerpfad, in dem sich die Datei befindet. |
| **storageName**| Abfrage    | string | Nein         | Name des zu verwendenden Speicherdienstes. |

---

## Anforderungstext-Schema (`axis`-Objekt)

Es müssen nur die Eigenschaften angegeben werden, die Sie ändern möchten.

| Eigenschaft    | Typ     | Erforderlich | Beschreibung |
|----------------|---------|--------------|-------------|
| `minimum`      | number  | Nein         | Untere Grenze der Achse. |
| `maximum`      | number  | Nein         | Obere Grenze der Achse. |
| `majorUnit`    | number  | Nein         | Intervall zwischen Hauptstrichen. |
| `minorUnit`    | number  | Nein         | Intervall zwischen Nebenstrichen. |
| `logBase`      | number  | Nein         | Basis des Logarithmus, wenn `isLogarithmic` auf `true` gesetzt ist. |
| `isLogarithmic`| boolean | Nein         | Gibt an, ob die Achse eine logarithmische Skalierung verwendet. |
| `displayUnit`  | string  | Nein         | Auf der Achse angezeigte Einheit (z. B. `"Thousands"`). |
| `tickMark`     | string  | Nein         | Stil der Striche (`"inside"`, `"outside"` usw.). |
| `crossAt`      | number  | Nein         | Position, an der die Achse die senkrechte Achse schneidet. |

### Beispiel für Anforderungstext

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

## Beispielanforderungen

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

### SDK-Beispiele  

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
System.out.println("Wertachse aktualisiert.");
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
echo "Wertachse aktualisiert.\n";
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
puts 'Wertachse aktualisiert.'
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
print('Wertachse aktualisiert.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Node.js-Beispiel
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
   .then(response => console.log('Wertachse aktualisiert.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Android (Java)-Beispiel
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
        print("Fehler: \\(error)")
    } else {
        print("Wertachse aktualisiert.")
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
print "Wertachse aktualisiert.\n";
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
        fmt.Println("Fehler:", err)
    } else {
        fmt.Println("Wertachse aktualisiert.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## Antworten

### Erfolg (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Der Antworttyp ist `CellsCloudResponse`.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|-------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |
---

## Weitere Ressourcen

- **OpenAPI-Spezifikation** – [Anzeigen / Herunterladen als JSON-YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **SDK-Repository** – <https://github.com/aspose-cells-cloud>  
- **Authentifizierungsanleitung** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*Für Fragen oder Feedback wenden Sie sich bitte an das Aspose.Cells Cloud-Supportteam.*