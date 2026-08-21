---
---
title: "Elimina tutti i commenti del foglio di lavoro"
description: "Elimina tutti i commenti da un foglio di lavoro in un file Excel utilizzando l'API Aspose.Cells Cloud. Scopri l'endpoint DELETE, i parametri richiesti, l'autenticazione, la richiesta cURL di esempio, il formato della risposta, i codici di errore e gli esempi di SDK."
keywords: "Aspose, Cells, elimina commenti, foglio di lavoro, API, REST, Excel, cloud"
url: /comments/clear/
aliases:
  - /delete-all-comments-in-a-worksheet/
weight: 50
---

# Elimina tutti i commenti del foglio di lavoro

**Versione API:** `v3.0`  
**Risorsa:** `Worksheets` → `DeleteWorksheetComments`  

Aspose.Cells Cloud fornisce un endpoint REST robusto che rimuove **tutti** i commenti da un foglio di lavoro specificato. Questa operazione è irreversibile: una volta eseguita, i commenti non possono essere recuperati.

---

## Prerequisiti

| Requisito | Dettagli |
|-----------|----------|
| **Autenticazione** | È necessario un token di accesso JWT valido nell'intestazione `Authorization` (`Bearer <jwt token>`). Ottieni il token tramite il [flusso di autenticazione OAuth2](https://docs.aspose.cloud/cells/authentication/). |
| **Archiviazione** | Il file deve trovarsi in un'archiviazione accessibile ad Aspose.Cells Cloud (viene utilizzata l'archiviazione predefinita se `storageName` viene omesso). |
| **Permessi** | Il token deve avere il permesso di leggere e scrivere il file di destinazione. |
| **SDK (opzionale)** | Gli SDK sono disponibili per .NET, Java, PHP, Ruby, Node.js, Python, Perl e Go (vedi la sezione **Esempi di SDK**). |

---

## Richiesta HTTP

### Endpoint

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments
```

### Parametri del percorso

| Nome         | Tipo   | Descrizione |
|--------------|--------|-------------|
| `name`       | string | Nome del file Excel (ad esempio `test.xlsx`). |
| `sheetName`  | string | Nome del foglio di lavoro (ad esempio `Sheet1`). |

### Parametri di query

| Nome            | Tipo   | Obbligatorio | Descrizione |
|-----------------|--------|--------------|-------------|
| `folder`        | string | opzionale    | Percorso della cartella contenente il file. |
| `storageName`   | string | opzionale    | Nome dell'archiviazione in cui si trova il file. |

### Intestazioni della richiesta

| Intestazione          | Valore                             |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer <jwt token>`               |
| `Accept`              | `application/json`                |
| `Content-Type`        | `application/json`                |

---

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments?folder=Documents&storageName=MyStorage" \
  -X DELETE \
  -H "Accept: application/json" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Sostituisci `test.xlsx`, `Sheet1`, `Documents`, `MyStorage` e `<jwt token>` con i tuoi valori effettivi.*

---

## Risposta

### Esito positivo (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Il corpo della risposta conforma al modello `CellsCloudResponse`.

### Risposte di errore

| Codice HTTP | Significato                              | Corpo di esempio |
|-------------|------------------------------------------|------------------|
| **400**     | Richiesta non valida – parametri non validi. | `{ "Code": 400, "Message": "Invalid request." }` |
| **401**     | Non autorizzato – token JWT mancante o non valido. | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**     | Non trovato – il file o il foglio di lavoro non esiste. | `{ "Code": 404, "Message": "Resource not found." }` |
| **500**     | Errore interno del server. | `{ "Code": 500, "Message": "Server error." }` |

---

## Esempi di SDK

I frammenti seguenti mostrano come chiamare l'endpoint utilizzando gli SDK ufficiali di Aspose.Cells Cloud (versione 3.13.0). Sostituisci i valori segnaposto (`<fileName>`, `<sheet>`, `<jwt token>`, ecc.) con i tuoi dati.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new WorksheetsApi();
var name = "test.xlsx"; // string | Nome del file.
var sheetName = "Sheet1"; // string | Nome del foglio di lavoro.
var folder = "Documents"; // string | Percorso della cartella (opzionale)
var storageName = "MyStorage"; // string | Nome dell'archiviazione (opzionale)

try
{
    var response = apiInstance.DeleteWorksheetComments(name, sheetName, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Eccezione durante la chiamata a WorksheetsApi.DeleteWorksheetComments: " + e.Message );
}
```

### Java  

```java
import com.aspose.cells.cloud.sdk.api.WorksheetsApi;
import com.aspose.cells.cloud.sdk.model.*;

public class DeleteWorksheetComments {
    public static void main(String[] args) {
        WorksheetsApi api = new WorksheetsApi();
        String name = "test.xlsx";
        String sheetName = "Sheet1";
        String folder = "Documents";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse resp = api.deleteWorksheetComments(name, sheetName, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### PHP  

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\WorksheetsApi;

$apiInstance = new WorksheetsApi();
$name = "test.xlsx";
$sheetName = "Sheet1";
$folder = "Documents";
$storageName = "MyStorage";

try {
    $result = $apiInstance->deleteWorksheetComments($name, $sheetName, $folder, $storageName);
    echo $result->getStatus();
} catch (Exception $e) {
    echo 'Eccezione durante la chiamata a WorksheetsApi->deleteWorksheetComments: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Ruby  

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::WorksheetsApi.new
name = 'test.xlsx'
sheet_name = 'Sheet1'
folder = 'Documents'          # opzionale
storage_name = 'MyStorage'    # opzionale

begin
  result = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
  puts result.status
rescue AsposeCellsCloud::ApiError => e
  puts "Eccezione durante la chiamata a WorksheetsApi->delete_worksheet_comments: #{e}"
end
```

### Node.js (TypeScript)  

```typescript
import { WorksheetsApi } from "@asposecloud/cells-sdk";

const api = new WorksheetsApi();
const name = "test.xlsx";
const sheetName = "Sheet1";
const folder = "Documents";
const storageName = "MyStorage";

api.deleteWorksheetComments(name, sheetName, folder, storageName)
    .then((response) => console.log(response.status))
    .catch((error) => console.error("Errore:", error));
```

### Python  

```python
from asposecellscloud import WorksheetsApi

api_instance = WorksheetsApi()
name = "test.xlsx"
sheet_name = "Sheet1"
folder = "Documents"          # opzionale
storage_name = "MyStorage"    # opzionale

try:
    response = api_instance.delete_worksheet_comments(name, sheet_name, folder, storage_name)
    print(response.status)
except Exception as e:
    print("Eccezione durante la chiamata a WorksheetsApi->delete_worksheet_comments:", e)
```

### Perl  

```perl
use AsposeCellsCloud::Api::WorksheetsApi;

my $api_instance = AsposeCellsCloud::Api::WorksheetsApi->new();

my $name = 'test.xlsx';
my $sheet_name = 'Sheet1';
my $folder = 'Documents';
my $storage_name = 'MyStorage';

eval {
    my $result = $api_instance->delete_worksheet_comments(
        name => $name,
        sheet_name => $sheet_name,
        folder => $folder,
        storage_name => $storage_name
    );
    print $result->{status}, "\n";
};
if ($@) {
    print "Eccezione durante la chiamata a WorksheetsApi->delete_worksheet_comments: $@\n";
}
```

### Go  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    cfg := sdk.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <jwt token>")
    api := sdk.NewWorksheetsApi(cfg)

    name := "test.xlsx"
    sheetName := "Sheet1"
    folder := "Documents"
    storageName := "MyStorage"

    resp, _, err := api.DeleteWorksheetComments(name, sheetName, folder, storageName)
    if err != nil {
        fmt.Printf("Errore: %v\n", err)
        return
    }
    fmt.Println(resp.Status)
}
```

---

## Note e limitazioni

* Questa operazione **elimina ogni commento** nel foglio di lavoro specificato. Utilizzala con attenzione—non è prevista alcuna funzione di annullamento.
* La richiesta **non accetta un corpo**; tutte le informazioni necessarie vengono trasmesse tramite URL ed intestazioni.
* Se il file di destinazione è **protetto** o il foglio di lavoro è in **sola lettura**, l'API restituirà un errore `400` o `401` a seconda della causa sottostante.
* L'endpoint funziona con file memorizzati sia in **Aspose Cloud Storage** che in **Amazon S3**, **Azure Blob** o **Google Cloud Storage**, quando correttamente referenziati tramite `storageName`.

---

## Risorse correlate

* **Specifiche OpenAPI** – [DeleteWorksheetComments](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComments)
* **Guida all'autenticazione** – [OAuth2 per Aspose.Cells Cloud](https://docs.aspose.cloud/cells/authentication/)
* **Repository degli SDK** – <https://github.com/aspose-cells-cloud>
* **API generica per i fogli di lavoro** – <https://docs.aspose.cloud/cells/worksheets/>

---

*Ultimo aggiornamento: 2026‑07‑30*