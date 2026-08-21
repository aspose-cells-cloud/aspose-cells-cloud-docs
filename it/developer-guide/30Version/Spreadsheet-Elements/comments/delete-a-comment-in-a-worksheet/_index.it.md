---
---
title: "API di eliminazione del commento nel foglio di lavoro – Aspose.Cells Cloud"
description: "Elimina un commento specifico di una cella in un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempi di richiesta/risposta, frammenti SDK e gestione degli errori."
keywords: "Aspose.Cells, elimina commento, API Excel, REST, commento foglio di lavoro"
date: "2026-07-30"
lastModified: "2026-07-30"
---

# API di eliminazione del commento nel foglio di lavoro – Aspose.Cells Cloud

> **Ultima modifica della pagina:** 30 luglio 2026  

## Panoramica
Un **commento** è una nota di testo associata a una particolare cella in un foglio di lavoro Excel.  
L'operazione **Elimina commento foglio di lavoro** rimuove un commento dalla cella specificata.

![Aspose.Cells Cloud – Illustrazione per l'eliminazione del commento nel foglio di lavoro](/cells/images/Aspose-image-for-open-graph.jpg "Aspose.Cells Cloud – API di eliminazione del commento nel foglio di lavoro")

## Autenticazione
Tutti gli endpoint di Aspose.Cells Cloud richiedono l'**autenticazione basata su token JWT**.  
Includere il token nell'intestazione `Authorization`:

```
Authorization: Bearer <jwt token>
```

Per maggiori dettagli su come ottenere un token JWT, consulta la [Guida all'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Prerequisiti
- Un token di accesso JWT valido.  
- Il workbook di destinazione (`{name}`) deve esistere nella posizione di archiviazione specificata.  
- Opzionale: Uno degli SDK di Aspose.Cells Cloud installati per il linguaggio preferito.

## Richiesta HTTP

### Endpoint
```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### Parametri del percorso
| Parametro | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|--------------|-------------|
| `name`      | string | ✅ | Nome del workbook Excel (ad esempio, `test.xlsx`). |
| `sheetName` | string | ✅ | Nome del foglio di lavoro contenente il commento. |
| `cellName`  | string | ✅ | Indirizzo della cella il cui commento verrà eliminato (ad esempio, `A1`). |

### Parametri di query
| Parametro   | Tipo   | Obbligatorio | Descrizione |
|-------------|--------|--------------|-------------|
| `folder`      | string | ❌ | Percorso della cartella in cui è memorizzato il workbook. Se omesso, viene utilizzata la cartella root. |
| `storageName` | string | ❌ | Nome del servizio di archiviazione (ad esempio, `MyCloud`). Se omesso, viene utilizzato l'archivio predefinito. |

## Esempio di richiesta

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1?folder=Docs&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Risposta

### Esito positivo (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto nel server. |
### Risposte di errore

| Codice HTTP | Descrizione | Esempio |
|-------------|-------------|---------|
| 400 | Richiesta non valida – parametri mancanti o non corretti. | `{ "Code": 400, "Message": "Parametri non validi." }` |
| 401 | Non autorizzato – token non valido o mancante. | `{ "Code": 401, "Message": "Autenticazione richiesta." }` |
| 404 | Non trovato – il file, il foglio di lavoro o il commento non esiste. | `{ "Code": 404, "Message": "Risorsa non trovata." }` |
| 500 | Errore interno del server – condizione imprevista sul server. | `{ "Code": 500, "Message": "Errore del server." }` |

## Esempi SDK
Di seguito sono riportati frammenti pronti all'uso per i linguaggi più diffusi. Sostituisci `<jwt token>`, `test.xlsx`, `Sheet1` e `A1` con i tuoi valori.

### C#
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Client;

// Configura il client dell'API
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};

var apiInstance = new WorksheetsApi(config);
try
{
    var result = apiInstance.DeleteWorksheetComment(
        name: "test.xlsx",
        sheetName: "Sheet1",
        cellName: "A1",
        folder: "Docs",
        storageName: "MyStorage"
    );
    Console.WriteLine("Commento eliminato. Stato: " + result.Status);
}
catch (Exception e)
{
    Console.WriteLine("Eccezione durante la chiamata a WorksheetsApi.DeleteWorksheetComment: " + e.Message);
}
```

### Java
```java
import com.aspose.cloud.cells.api.WorksheetsApi;
import com.aspose.cloud.cells.client.ApiException;
import com.aspose.cloud.cells.model.CellsCloudResponse;

public class DeleteWorksheetCommentExample {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        api.getApiClient().setAccessToken("<jwt token>");
        try {
            CellsCloudResponse response = api.deleteWorksheetComment(
                "test.xlsx",
                "Sheet1",
                "A1",
                "Docs",
                "MyStorage"
            );
            System.out.println("Commento eliminato, stato: " + response.getStatus());
        } catch (ApiException e) {
            System.err.println("Eccezione durante la chiamata a WorksheetsApi#deleteWorksheetComment");
            e.printStackTrace();
        }
    }
}
```

### PHP
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\WorksheetsApi(
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->deleteWorksheetComment(
        'test.xlsx',
        'Sheet1',
        'A1',
        'Docs',
        'MyStorage'
    );
    echo "Commento eliminato. Stato: " . $result->getStatus();
} catch (Exception $e) {
    echo 'Eccezione durante la chiamata a WorksheetsApi->deleteWorksheetComment: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby
```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
begin
  result = api_instance.delete_worksheet_comment('test.xlsx', 'Sheet1', 'A1', 'Docs', 'MyStorage')
  puts "Commento eliminato – stato: #{result.status}"
rescue AsposeCellsCloud::ApiError => e
  puts "Eccezione durante la chiamata a WorksheetsApi->delete_worksheet_comment: #{e}"
end
```

### Node.js (TypeScript)
```typescript
import { WorksheetsApi, Configuration } from "@asposecloud/cells-cloud";

const config = new Configuration({
    accessToken: "<jwt token>",
    basePath: "https://api.aspose.cloud"
});

const api = new WorksheetsApi(config);

api.deleteWorksheetComment("test.xlsx", "Sheet1", "A1", "Docs", "MyStorage")
    .then((response) => {
        console.log("Commento eliminato. Stato:", response.status);
    })
    .catch((error) => {
        console.error("Errore durante l'eliminazione del commento:", error);
    });
```

### Python
```python
from asposecellscloud.apis import WorksheetsApi
from asposecellscloud import Configuration, ApiClient

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_client = ApiClient(configuration=config)
api = WorksheetsApi(api_client)

try:
    response = api.delete_worksheet_comment(
        name="test.xlsx",
        sheet_name="Sheet1",
        cell_name="A1",
        folder="Docs",
        storage_name="MyStorage"
    )
    print("Commento eliminato. Stato:", response.status)
except Exception as e:
    print("Eccezione durante la chiamata a WorksheetsApi->delete_worksheet_comment:", e)
```

### Perl
```perl
use AsposeCellsCloud::Api::WorksheetsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '<jwt token>',
    host => 'https://api.aspose.cloud'
);
my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new($config);

eval {
    my $result = $api_instance->delete_worksheet_comment(
        name        => 'test.xlsx',
        sheet_name  => 'Sheet1',
        cell_name   => 'A1',
        folder      => 'Docs',
        storage_name=> 'MyStorage'
    );
    print "Commento eliminato. Stato: " . $result->{status} . "\n";
};
if ($@) {
    warn "Eccezione durante la chiamata a WorksheetsApi->delete_worksheet_comment: $@\n";
}
```

### Go
```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/api"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/config"
)

func main() {
    cfg := config.NewConfiguration()
    cfg.AccessToken = "<jwt token>"
    cfg.Host = "https://api.aspose.cloud"

    apiInstance := api.NewWorksheetsApi(cfg)

    result, _, err := apiInstance.DeleteWorksheetComment(
        "test.xlsx",   // name
        "Sheet1",      // sheetName
        "A1",          // cellName
        "Docs",        // folder (opzionale)
        "MyStorage",   // storageName (opzionale)
    )
    if err != nil {
        fmt.Printf("Errore durante la chiamata a DeleteWorksheetComment: %v\n", err)
        return
    }
    fmt.Printf("Commento eliminato. Stato: %s\n", result.Status)
}
```

## Operazioni correlate
- [Aggiungi commento foglio di lavoro](/comments/add/)  
- [Aggiorna commento foglio di lavoro](/comments/update/)  

## Limitazione della velocità
Aspose.Cells Cloud applica un **limite predefinito di 100 richieste al minuto per account**. Superare questo limite restituisce HTTP 429 Too Many Requests. Implementa un ritardo esponenziale o rispetta l'intestazione `Retry-After` per evitare throttling.

## Vedi anche
- **Specifiche OpenAPI:** <https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment>  
- **Guida all'autenticazione:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Repository SDK:** <https://github.com/aspose-cells-cloud>  

---
---