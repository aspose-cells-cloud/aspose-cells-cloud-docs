---
title: "Aspose.Cells Cloud API – Uppdatera diagramvärdeaxel (POST /valueaxis)"
description: "Uppdatera värdeaxeln för ett diagram i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller endpoint, parametrar, begärandetextschema, exempel (cURL och SDK:er), svar och felhantering."
keywords:
  - Aspose.Cells Cloud
  - Uppdatera diagramvärdeaxel
  - REST API
  - Excel-diagramaxel
  - POST valueaxis
  - cURL-exempel
  - SDK
  - JSON-payload
  - diagramaxelinställningar
last_updated: 2026-07-30
---

# Uppdatera diagramvärdeaxel (POST /valueaxis)

**Sammanfattning:**  
Ändra värdeaxeln för ett specifikt diagram i en Excel-arbetsbok som lagras i Aspose Cloud. Du kan ställa in gränser, stegvärden, logaritmisk skalning och andra axelinställningar i en enda begäran.

---

## Förutsättningar

1. **JWT-åtkomsttoken** – skaffa en token enligt beskrivningen i [Autentisering guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
2. Den mål-**arbetsbok** måste redan laddats upp till Aspose Cloud-lagring (eller standardlagringen).  
3. Känn till **arkets namn** och **indexet för diagrammet (nollbaserat)** som du vill ändra.

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*Ersätt platshållarna med dina faktiska värden.*

| Platshållare | Beskrivning |
|-------------|-------------|
| `{name}` | Namn på Excel-filen (t.ex. `Book1.xlsx`). |
| `{sheetName}` | Arket som innehåller diagrammet (t.ex. `Sheet1`). |
| `{chartIndex}` | Nollbaserat index för diagrammet (t.ex. `0`). |

---

## Autentisering

API:et använder **JWT tokenbaserad autentisering**. inkludera token i `Authorization`-headern:

```
Authorization: Bearer <jwt token>
```

---

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT tokenbaserad autentisering</a>.

## Begärandeparametrar

| Namn          | Plats   | Typ    | Obligatoriskt | Beskrivning |
|---------------|---------|--------|---------------|-------------|
| **name**      | Sökväg  | string | Ja            | Namn på Excel-filen lagrad i molnet. |
| **sheetName** | Sökväg  | string | Ja            | Arket som innehåller diagrammet. |
| **chartIndex**| Sökväg  | int    | Ja            | Nollbaserat index för diagrammet som ska uppdateras. |
| **axis**      | Text    | object | Ja            | Axelinställningar (se *Begärandetextschema*). |
| **folder**    | Fråga   | string | Nej           | Molnsökväg till mappen där filen finns. |
| **storageName**| Fråga  | string | Nej           | Namn på lagringstjänsten som ska användas. |

---

## Begärandetextschema (`axis`-objekt)

Endast egenskaperna du behöver ändra behöver finnas med.

| Egenskap       | Typ     | Obligatoriskt | Beskrivning |
|----------------|---------|---------------|-------------|
| `minimum`      | number  | Nej           | Undre gräns för axeln. |
| `maximum`      | number  | Nej           | Övre gräns för axeln. |
| `majorUnit`    | number  | Nej           | Intervall mellan stora tick-märken. |
| `minorUnit`    | number  | Nej           | Intervall mellan små tick-märken. |
| `logBase`      | number  | Nej           | Logaritmbas när `isLogarithmic` är `true`. |
| `isLogarithmic`| boolean | Nej           | Om axeln använder logaritmisk skalning. |
| `displayUnit`  | string  | Nej           | Enhetsetikett som visas på axeln (t.ex. `"Tusental"`). |
| `tickMark`     | string  | Nej           | Stil för tick-märken (`"inside"`, `"outside"`, etc.). |
| `crossAt`      | number  | Nej           | Position där axeln korsar den vinkelräta axeln. |

### Exempel på begärandetext

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

## Exempel på begäranden

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

### SDK-exempel  

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
System.out.println("Value axis updated.");
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
echo "Value axis updated.\n";
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
puts 'Value axis updated.'
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
print('Value axis updated.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Node.js-exempel
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
   .then(response => console.log('Value axis updated.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Android (Java)-exempel
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
        print("Error: \\(error)")
    } else {
        print("Value axis updated.")
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
print "Value axis updated.\n";
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
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## Svar

### Framgång (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Svarstypen är `CellsCloudResponse`.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                     |
|-----|-----------------------------|-------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel. |
---

## Ytterligare resurser

- **OpenAPI-specifikation** – [Visa / ladda ner JSON-YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **SDK-förvar** – <https://github.com/aspose-cells-cloud>  
- **Autentiseringsguide** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*Vid frågor eller feedback, vänligen kontakta Aspose.Cells Cloud-supportteamet.*