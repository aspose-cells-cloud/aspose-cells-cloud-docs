---
title: Rimuovi raggruppamento colonne in Excel – Aspose.Cells Cloud API  
description: Rimuovi il raggruppamento delle colonne in un foglio di lavoro Excel usando l'API REST Aspose.Cells Cloud (v3.0). Include endpoint, parametri, autenticazione, esempio cURL, formato della risposta e frammenti SDK.  
keywords: Aspose.Cells, rimuovi raggruppamento, colonne, Excel, API, REST, cloud, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Rimuovi raggruppamento colonne in Excel  

Aspose.Cells Cloud fornisce un'operazione **POST** che rimuove il raggruppamento delle colonne da un foglio di lavoro specificato. Questa pagina descrive il formato della richiesta, i parametri obbligatori, il metodo di autenticazione, gli esempi di chiamata e l'uso degli SDK.

---  

## Prerequisiti  

| Requisito | Perché è necessario |
|-----------|---------------------|
| **Account Aspose Cloud** | Per accedere ai servizi Aspose.Cells Cloud. |
| **Token di accesso JWT** | Tutte le chiamate API devono essere autorizzate con un token bearer. Vedi la [guida all'autenticazione JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Cartella di lavoro memorizzata in Aspose Cloud Storage** | L'API opera su file situati nello storage cloud (o in uno storage esterno connesso). |
| **Nome del foglio di lavoro** | Il foglio di lavoro target deve esistere nella cartella di lavoro. |

---  

## Autenticazione  

Tutte le richieste richiedono un'intestazione **Authorization** contenente un token JWT valido:

```http
Authorization: Bearer <access_token>
```

Il token viene ottenuto tramite il flusso OAuth di Aspose Cloud. I token hanno una validità limitata; rinnovare quando necessario.

---  

## Endpoint  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` – **Percorso** – Nome del file della cartella di lavoro (es. `test.xlsx`).  
* `{sheetName}` – **Percorso** – Nome del foglio di lavoro (es. `Sheet1`).  

---  

## Parametri  

### Parametri di percorso  

| Nome | Tipo | Obbligatorio | Descrizione |
|------|------|--------------|-------------|
| `name` | string | Sì | Nome del file della cartella di lavoro. |
| `sheetName` | string | Sì | Nome del foglio di lavoro. |

### Parametri di query  

| Nome | Tipo | Obbligatorio | Descrizione |
|------|------|--------------|-------------|
| `firstIndex` | integer | Sì | Indice in base zero della prima colonna da scartare dal raggruppamento. |
| `lastIndex` | integer | Sì | Indice in base zero dell'ultima colonna da scartare dal raggruppamento. |
| `folder` | string | No | Percorso della cartella contenente la cartella di lavoro. |
| `storageName` | string | No | Nome del servizio di storage in cui risiede il file. |

---  

## Esempio di richiesta (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*Sostituisci `<access_token>` con un token JWT valido.*

---  

## Risposta in caso di successo  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

L'oggetto di risposta (`CellsCloudResponse`) contiene l'intervallo di colonne che sono state scartate con successo dal raggruppamento.

### Risposta in caso di errore  

Quando la richiesta fallisce, il servizio restituisce un payload JSON con i seguenti campi:

| Campo | Significato |
|-------|-------------|
| `Code` | Codice di errore in stile HTTP (es. 400, 401). |
| `Status` | Breve descrizione dell'errore. |
| `ErrorMessage` | Descrizione dettagliata dell'errore. |

---  

**Codici di stato HTTP**

| Codice | Significato                  | Descrizione                                         |
|--------|------------------------------|-----------------------------------------------------|
| 200    | OK                           | Filtro applicato con successo; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida         | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato              | Token JWT non valido o mancante. |
| 413    | Payload troppo grande        | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server    | Errore imprevisto sul server. |
---  

## Esempi di codice SDK  

Di seguito sono riportati frammenti pronti all'uso per gli SDK più diffusi. Sostituisci i valori segnaposto (`<YourAccessToken>`, `<YourFileName>`, ecc.) con i tuoi dati.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Colonne scartate dal raggruppamento: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Colonne scartate dal raggruppamento: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Colonne scartate dal raggruppamento: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Colonne scartate dal raggruppamento: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Colonne scartate dal raggruppamento: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **Nota:** Gli SDK per PHP, Ruby, Perl e altri linguaggi seguono lo stesso ordine dei parametri. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per esempi completi.

---  

## Riferimenti  

* **Specifiche OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Guida all'autenticazione:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **Repository SDK:** <https://github.com/aspose-cells-cloud>

---  

## Cronologia delle revisioni  

| Data | Autore | Modifiche |
|------|--------|----------|
| 2026‑07‑30 | AI Optimizer | Corretta codifica UTF‑8, aggiunti Prerequisiti, puliti meta keywords, migliorata gerarchia dei titoli, inseriti frammenti SDK. |
| 2026‑07‑29 | Originale | Bozza iniziale della documentazione. |

---