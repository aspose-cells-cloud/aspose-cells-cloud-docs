---
title: "Calcola tutte le formule in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Calcola"
type: docs
url: /calculate-all-formulas-on-an-excel-file/
aliases:
  [/calculate-all-formulas-in-a-workbook/, /workbook/calculate-all-formulas/]
keywords: "Aspose.Cells, calcolo formule, API Excel, SDK cloud"
description: "Calcola tutte le formule in un foglio di calcolo Excel tramite l'API REST di Aspose.Cells Cloud. Include esempio cURL, parametri di richiesta, schema di risposta, prerequisiti e frammenti di codice SDK per diversi linguaggi."
weight: 140
ArticleTitle: "Calcola tutte le formule in un foglio di calcolo Excel"
---

Questa REST API calcola **tutte le formule** in un foglio di calcolo Excel.

**Prerequisiti:** Prima di chiamare questo endpoint, assicurati di disporre di:
- Un token di autenticazione JWT valido. (Vedi la [Guida all'autenticazione](/authentication/).)  
- Il client ID e il secret di Aspose.Cells Cloud.  
- Il foglio di calcolo di destinazione caricato nella posizione di archiviazione designata. (Vedi la [Configurazione dell'archiviazione](/storage/).)

## API PostWorkbookCalculateFormula

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/calculateformula
```

I parametri della richiesta sono elencati di seguito:

| Nome Parametro  | Tipo               | Posizione | Descrizione                                                                                  |
| --------------- | ------------------ | -------- | -------------------------------------------------------------------------------------------- |
| **name**        | string             | path     | Nome del file del foglio di calcolo.                                                         |
| **options**     | CalculationOptions | body     | Oggetto JSON che specifica le impostazioni di calcolo (ad es. `CalcStackSize`, `IgnoreError`). |
| **ignoreError** | boolean            | query    | Se impostato su `true`, gli errori riscontrati durante il calcolo vengono ignorati.          |
| **folder**      | string             | query    | Percorso della cartella contenente il foglio di calcolo.                                     |
| **storageName** | string             | query    | Nome del servizio di archiviazione in cui è memorizzato il foglio di calcolo.                |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookCalculateFormula) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

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

#### Dettagli della risposta

| Campo            | Tipo   | Descrizione                                                            |
| ---------------- | ------ | ---------------------------------------------------------------------- |
| **Code**         | int    | Codice di stato simile a HTTP (200 indica esito positivo).             |
| **Status**       | string | Breve descrizione testuale del risultato (ad es. `OK`).                 |
| **WorkbookUrl**  | string | URL diretto dal quale scaricare il foglio di calcolo aggiornato.       |
| **ErrorMessage** | string | Informazioni dettagliate sull'errore in caso di fallimento della richiesta; `null` in caso di successo. |

#### Passaggi successivi / errori comuni

- **Gestione degli errori di calcolo** – impostare `ignoreError=false` per ricevere una risposta di errore quando una formula non può essere valutata.
- **Attenzione ai limiti di frequenza (rate limit)** – controllare l'header `X-RateLimit-Remaining`; se raggiunge `0`, attendere prima di ritentare.
- **Guida agli stati HTTP**:
  - `400` – Parametri di richiesta non validi.
  - `401` – Autenticazione non riuscita (token JWT non valido o scaduto).
  - `404` – Foglio di calcolo non trovato.
  - `500` – Errore lato server; contattare il supporto Aspose se persiste.

| Codice | Significato           | Quando restituito                                         |
|--------|-----------------------|-----------------------------------------------------------|
| 400    | Richiesta non valida  | Parametri di richiesta non validi o JSON malformato.     |
| 401    | Non autorizzato       | Token JWT mancante, non valido o scaduto.                |
| 404    | Non trovato           | Il foglio di calcolo specificato non esiste nell'archivio.|
| 500    | Errore interno server | Guasto imprevisto lato server; contattare il supporto Aspose. |

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

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