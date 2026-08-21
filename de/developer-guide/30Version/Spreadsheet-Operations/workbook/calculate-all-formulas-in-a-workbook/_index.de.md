---
title: "Alle Formeln in einer Excel-Arbeitsmappe berechnen"
second_title: "Dokument"
linktitle: "Berechnen"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, Formeln berechnen, Excel-API, Cloud-SDK"
description: "Berechnen Sie alle Formeln in einer Excel-Arbeitsmappe über die Aspose.Cells Cloud REST-API. Enthält cURL-Beispiel, Anforderungsparameter, Antwortschema, Voraussetzungen und SDK-Snippets für mehrere Sprachen."
weight: 140
ArticleTitle: "Alle Formeln in einer Excel-Arbeitsmappe berechnen"
---

Diese REST-API berechnet **alle Formeln** in einer Excel-Arbeitsmappe.

**Voraussetzungen:** Bevor Sie diesen Endpunkt aufrufen, stellen Sie sicher, dass Folgendes vorliegt:
- Ein gültiges JWT-Authentifizierungstoken. (Siehe [Authentifizierungsanleitung](/authentication/).)  
- Ihre Aspose.Cells Cloud Client-ID und das zugehörige Geheimnis (Secret).  
- Die Ziel-Arbeitsmappe ist im vorgesehenen Speicherort hochgeladen. (Siehe [Speicherkonfiguration](/storage/).)

## PostWorkbookCalculateFormula-API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

Die Anforderungsparameter sind wie folgt aufgelistet:

| Parametername   | Typ                | Position | Beschreibung                                                                            |
| ---------------- | ------------------ | -------- | --------------------------------------------------------------------------------------- |
| **name**         | string             | path     | Name der Arbeitsmappe-Datei.                                                            |
| **options**      | CalculationOptions | body     | JSON-Objekt, das Berechnungseinstellungen festlegt (z. B. `CalcStackSize`, `IgnoreError`). |
| **ignoreError**  | boolean            | query    | Wenn `true`, werden beim Berechnen auftretende Fehler ignoriert.                        |
| **folder**       | string             | query    | Pfad zum Ordner, der die Arbeitsmappe enthält.                                          |
| **storageName**  | string             | query    | Name des Speicherdiensts, in dem die Arbeitsmappe gespeichert ist.                      |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/calculateformula?ignoreError=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CalcStackSize": 1,
        "IgnoreError": true,
        "PrecisionStrategy": "string",
        "Recursive": true
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "WorkbookUrl": "https://api.aspose.cloud/v3.0/storage/file/Book1.xlsx",
  "ErrorMessage": null
}
```

{{< /tab >}}

{{< /tabs >}}

#### Antwortdetails

| Feld             | Typ    | Beschreibung                                                              |
| ---------------- | ------ | ------------------------------------------------------------------------- |
| **Code**         | int    | HTTP-ähnlicher Statuscode (200 bedeutet Erfolg).                          |
| **Status**       | string | Kurze textuelle Beschreibung des Ergebnisses (z. B. `OK`).                |
| **WorkbookUrl**  | string | Direkte URL, von der die aktualisierte Arbeitsmappe heruntergeladen werden kann. |
| **ErrorMessage** | string | Detaillierte Fehlerinformationen bei fehlgeschlagener Anforderung; `null` bei Erfolg. |

#### Nächste Schritte / Häufige Fehler

- **Berechnungsfehler behandeln** – setzen Sie `ignoreError=false`, um eine Fehlerantwort zu erhalten, wenn eine Formel nicht ausgewertet werden kann.  
- **Ratenlimit berücksichtigen** – prüfen Sie den Header `X-RateLimit-Remaining`; erreicht er `0`, warten Sie, bevor Sie es erneut versuchen.  
- **HTTP-Statuscodes**:
  - `400` – Ungültige Anforderungsparameter.
  - `401` – Authentifizierung fehlgeschlagen (ungültiges oder abgelaufenes JWT).
  - `404` – Arbeitsmappe nicht gefunden.
  - `500` – Serverseitiger Fehler; kontaktieren Sie den Aspose-Support, falls das Problem weiterhin besteht.

| Code | Bedeutung             | Wann wird er zurückgegeben?                                             |
|------|-----------------------|-------------------------------------------------------------------------|
| 400  | Bad Request (Ungültige Anforderung) | Ungültige Anforderungsparameter oder fehlerhaftes JSON.            |
| 401  | Unauthorized (Nicht autorisiert)    | Fehlendes, ungültiges oder abgelaufenes JWT-Token.                  |
| 404  | Not Found (Nicht gefunden)          | Die angegebene Arbeitsmappe existiert nicht im Speicher.            |
| 500  | Internal Server Error (Interner Serverfehler) | Unerwarteter serverseitiger Fehler; kontaktieren Sie den Aspose-Support. |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("<clientId>", "<clientSecret>");
var request = new PostWorkbookCalculateFormulaRequest(
    name: "Book1.xlsx",
    folder: "",
    storageName: "",
    ignoreError: true,
    options: new CalculationOptions { CalcStackSize = 1, IgnoreError = true });

var response = api.PostWorkbookCalculateFormula(request);
Console.WriteLine($"Status: {response.Status}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<clientId>", "<clientSecret>");
PostWorkbookCalculateFormulaRequest request = new PostWorkbookCalculateFormulaRequest()
        .name("Book1.xlsx")
        .ignoreError(true)
        .options(new CalculationOptions().calcStackSize(1).ignoreError(true));

WorkbookResponse result = api.postWorkbookCalculateFormula(request);
System.out.println("Status: " + result.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\CellsApi;
use Aspose\Cells\Cloud\Model\CalculationOptions;
use Aspose\Cells\Cloud\Model\PostWorkbookCalculateFormulaRequest;

$api = new CellsApi("<clientId>", "<clientSecret>");
$options = new CalculationOptions([
    "CalcStackSize" => 1,
    "IgnoreError"   => true
]);

$request = new PostWorkbookCalculateFormulaRequest([
    "name"    => "Book1.xlsx",
    "ignoreError" => true,
    "options" => $options
]);

$response = $api->postWorkbookCalculateFormula($request);
echo "Status: " . $response->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new("<clientId>", "<clientSecret>")
options = AsposeCellsCloud::CalculationOptions.new(
  calc_stack_size: 1,
  ignore_error: true
)

request = AsposeCellsCloud::PostWorkbookCalculateFormulaRequest.new(
  name: 'Book1.xlsx',
  ignore_error: true,
  options: options
)

response = api.post_workbook_calculate_formula(request)
puts "Status: #{response.status}"
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
const {
  CellsApi,
  PostWorkbookCalculateFormulaRequest,
  CalculationOptions,
} = require("asposecellscloud");

const api = new CellsApi("<clientId>", "<clientSecret>");
const options = new CalculationOptions({ CalcStackSize: 1, IgnoreError: true });

const request = new PostWorkbookCalculateFormulaRequest({
  name: "Book1.xlsx",
  ignoreError: true,
  options: options,
});

api.postWorkbookCalculateFormula(request).then((response) => {
  console.log(`Status: ${response.status}`);
});
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
from asposecellscloud import CellsApi, PostWorkbookCalculateFormulaRequest, CalculationOptions

api = CellsApi("<clientId>", "<clientSecret>")
options = CalculationOptions(calc_stack_size=1, ignore_error=True)

request = PostWorkbookCalculateFormulaRequest(
    name="Book1.xlsx",
    ignore_error=True,
    options=options
)

response = api.post_workbook_calculate_formula(request)
print(f"Status: {response.status}")
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
use AsposeCellsCloud::CellsApi;
use AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest;
use AsposeCellsCloud::Object::CalculationOptions;

my $api = AsposeCellsCloud::CellsApi->new(
    client_id     => '<clientId>',
    client_secret => '<clientSecret>'
);

my $options = AsposeCellsCloud::Object::CalculationOptions->new(
    CalcStackSize => 1,
    IgnoreError   => JSON::true
);

my $request = AsposeCellsCloud::Object::PostWorkbookCalculateFormulaRequest->new(
    name        => 'Book1.xlsx',
    ignoreError => JSON::true,
    options     => $options
);

my $response = $api->post_workbook_calculate_formula(request => $request);
print "Status: " . $response->{Status} . "\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3/api"
    "github.com/asposecellscloud/asposecellscloud-go/v3/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client-id", "<clientId>")
    cfg.AddDefaultHeader("client-secret", "<clientSecret>")
    client := api.NewAPIClient(cfg)

    opts := model.CalculationOptions{
        CalcStackSize: 1,
        IgnoreError:   true,
    }

    req := model.PostWorkbookCalculateFormulaRequest{
        Name:        "Book1.xlsx",
        IgnoreError: true,
        Options:     &opts,
    }

    resp, _, err := client.CellsApi.PostWorkbookCalculateFormula(req)
    if err != nil {
        panic(err)
    }
    fmt.Printf("Status: %s\n", resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}
---