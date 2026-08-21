---
---
title: "Elimina cartella – Aspose.Cells Cloud API | Rimuovi cartelle tramite REST"
description: "Scopri come eliminare una cartella (opzionalmente in modo ricorsivo) dall'archivio cloud di Aspose.Cells Cloud utilizzando l'endpoint DELETE /v4.0/cells/storage/folder/{path}. Include sintassi della richiesta, parametri, autenticazione, codice di esempio e gestione degli errori."
keywords: "Aspose.Cells, elimina cartella, archiviazione cloud, API, REST, Excel, gestione file"
slug: elimina-cartella
date: 2026-07-30
---

# Elimina cartella – Aspose.Cells Cloud API

Rimuovi una cartella (eventualmente tutto il suo contenuto) dall'archivio cloud di Aspose.Cells Cloud.

---

## Panoramica

L'operazione **Elimina cartella** rimuove permanentemente una cartella dall'account di archiviazione utilizzato da Aspose.Cells Cloud.  
Puoi eliminare una cartella vuota oppure, impostando il flag `recursive` su `true`, eliminare la cartella insieme a tutti i file e le sottocartelle in essa contenuti. Questo endpoint viene comunemente utilizzato negli script di pulizia, nei flussi di lavoro automatizzati o quando le directory temporanee non sono più necessarie.

---

## Richiesta HTTP

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – il percorso completo della cartella da eliminare (codificato in URL).

### Intestazioni HTTP obbligatorie

| Intestazione      | Valore                             | Descrizione                              |
|-------------------|------------------------------------|------------------------------------------|
| `Authorization`   | `Bearer {access_token}`            | Token JWT ottenuto dal servizio di autenticazione. |
| `Accept`          | `application/json`                | Formato della risposta atteso.           |
| `Content-Type`    | `application/json` *(opzionale)*  | Non richiesto per DELETE, ma può essere inviato. |

---

## Autenticazione

Aspose.Cells Cloud utilizza l’**autenticazione basata su token JWT**.  
Ottieni un token di accesso tramite l'[endpoint di autenticazione](/authentication/) e includilo nell’intestazione `Authorization` come mostrato sopra.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## Parametri

| Nome          | Tipo    | Posizione | Obbligatorio | Descrizione                                                                 |
|---------------|---------|-----------|--------------|-----------------------------------------------------------------------------|
| `path`        | stringa | Percorso  | Sì           | Percorso della cartella da eliminare (codificato in URL).                  |
| `storageName` | stringa | Query     | No           | Nome dell’archivio che contiene la cartella. Se omesso, viene utilizzato l’archivio predefinito. |
| `recursive`   | boolean | Query     | No           | `true` → elimina la cartella **e tutto il suo contenuto**. Valore predefinito: `false`. |

**Esempio di stringa di query**

```
?storageName=MyStorage&recursive=true
```

---

## Esempio di richiesta (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Risposta

Una richiesta riuscita restituisce **HTTP 200 OK** con un oggetto JSON vuoto:

```json
{}
```

Non viene fornito alcun payload aggiuntivo, poiché il risultato dell’operazione è binario: la cartella viene rimossa oppure viene restituito un errore.

---

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | File caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

Quando si verifica un errore, il corpo della risposta contiene un oggetto JSON con i campi `code` e `message` che descrivono il problema.

---

## Esempi di codice SDK

I seguenti esempi mostrano come chiamare **Elimina cartella** utilizzando gli SDK ufficialmente supportati. Sostituisci `{access_token}` e i valori dei parametri con i tuoi dati.

<details><summary>🟦 C# (.NET)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configura il client API
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// Elimina cartella (ricorsivamente)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// Inizializza il client API
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// Configurazione
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// Elimina cartella in modo ricorsivo
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Cartella eliminata.";
} catch (Exception $e) {
    echo 'Eccezione durante la chiamata a FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Cartella eliminata.'
rescue AsposeCellsCloud::ApiError => e
  puts "Errore: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Cartella eliminata'))
    .catch(err => console.error('Errore:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Cartella eliminata")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Cartella eliminata.\n";
};
if ($@) {
    warn "Errore durante l'eliminazione della cartella: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Errore: %v\n", err)
        return
    }
    fmt.Println("Cartella eliminata")
}
```
</details>

---

## Vedi anche

- **[Crea cartella](/crea-cartella/)** – Crea una nuova cartella nell’archivio cloud.  
- **[Copia cartella](/copia-cartella/)** – Duplica una cartella e il suo contenuto.  
- **[Sposta cartella](/sposta-cartella/)** – Sposta una cartella in un percorso diverso.  
- **[Specifiche OpenAPI]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">Operazione DeleteFolder</a> (explorer API interattivo).

---

## Elenco di controllo SEO e accessibilità (interno)

- **Titolo e H1** utilizzano il trattino lungo corretto (`–`) e contengono la parola chiave principale *Elimina cartella*.  
- Tutti i titoli seguono una gerarchia logica (`H1 → H2 → H3`).  
- Non rimangono artefatti di codifica UTF-8.  
- Parole chiave meta raggruppate in un’unica lista chiara (o omesse se preferito).  
- I link esterni includono `rel="noopener noreferrer"` per la sicurezza.  
- Le icone dell’interfaccia utente e i flag linguistici (se visualizzati nella pagina) dovrebbero avere gli attributi `aria-label`/`alt` (ad esempio, `aria-label="Italiano"`).  
- I tag `<link rel="alternate" hreflang="xx" href="…">` sono raccomandati nell’head della pagina per ogni versione linguistica.  

---