---
---
title: Aggiungere un filtro dinamico in un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud
description: Scopri come applicare un filtro dinamico (ad esempio BelowAverage, Tomorrow, LastMonth) a un foglio di lavoro Excel tramite l'API REST Aspose.Cells Cloud. Include autenticazione, sintassi della richiesta, parametri, gestione della risposta ed esempi di SDK per diversi linguaggi.
keywords: Aspose.Cells, filtro dinamico, API Excel, REST, filtro automatico, SDK cloud
slug: add-dynamic-filter
api_version: v3.0
---

## Panoramica

L'operazione **PutWorksheetDynamicFilter** aggiunge un filtro dinamico a un intervallo specificato in un foglio di lavoro Excel.  
I filtri dinamici valutano automaticamente valori come date, medie o celle vuote, consentendo di creare visualizzazioni "intelligenti" senza scrivere formule personalizzate.

## Prerequisiti

| Requisito | Dettagli |
|-----------|----------|
| **Autenticazione** | Un token JWT valido ottenuto dall'endpoint `/connect/token`. Includilo nell'intestazione `Authorization: Bearer <token>`. |
| **Archiviazione** | Il libro deve trovarsi in una posizione di archiviazione Aspose Cloud (predefinita o personalizzata). |
| **Formati di file supportati** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv`, ecc. |
| **Permessi** | Accesso in lettura/scrittura alla cartella/file di destinazione. |

## Richiesta HTTP

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Parametri del percorso

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|--------------|-------------|
| `name` | string | ✅ | Il nome del libro Excel (ad esempio `Book1.xlsx`). |
| `sheetName` | string | ✅ | Il nome del foglio di lavoro contenente l'intervallo da filtrare. |

### Parametri di query

| Parametro | Tipo | Obbligatorio | Descrizione |
|-----------|------|--------------|-------------|
| `range` | string | ✅ | L'intervallo di celle su cui viene applicato il filtro (ad esempio `A1:B1`). |
| `fieldIndex` | integer | ✅ | Indice in base zero della colonna all'interno dell'intervallo a cui viene applicato il filtro dinamico. |
| `dynamicFilterType` | string | ✅ | Tipo di filtro dinamico da applicare (vedi **Tipi di filtro dinamico supportati**). |
| `matchBlanks` | boolean | ❌ | Se `true`, le celle vuote sono incluse nei risultati del filtro. Valore predefinito: `false`. |
| `refresh` | boolean | ❌ | Se `true`, il filtro automatico viene aggiornato dopo l'applicazione del filtro. |
| `folder` | string | ❌ | Percorso della cartella nell'archiviazione in cui si trova il libro. |
| `storageName` | string | ❌ | Nome dell'archiviazione Aspose Cloud da utilizzare. |

### Corpo della richiesta

Il corpo della richiesta è un oggetto JSON vuoto:

```json
{}
```

## Tipi di filtro dinamico supportati

| Valore | Significato |
|--------|-------------|
| `BelowAverage` | Righe il cui valore è inferiore alla media della colonna. |
| `AboveAverage` | Righe il cui valore è superiore alla media della colonna. |
| `Tomorrow` | Righe con date pari alla data di domani. |
| `Yesterday` | Righe con date pari alla data di ieri. |
| `NextWeek` | Righe con date comprese nella prossima settimana calendario. |
| `LastMonth` | Righe con date appartenenti al mese precedente. |
| `ThisYear` | Righe con date appartenenti all'anno corrente. |

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # Il corpo JSON della richiesta PUT è vuoto
```

## Esempio di risposta

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Filtro dinamico applicato correttamente."
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Esempi di SDK

Di seguito sono riportati frammenti di codice pronti all'uso per gli SDK più diffusi. Sostituisci `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` e altri segnaposto con i tuoi valori effettivi.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | Nome del libro.
var sheetName = "Sheet1"; // string | Nome del foglio di lavoro.
var range = "A1:B1"; // string | Intervallo da filtrare.
var fieldIndex = 0; // int? | Indice della colonna in base zero.
var dynamicFilterType = "BelowAverage"; // string | Tipo di filtro dinamico.
var matchBlanks = true; // bool? | Includi celle vuote.
var refresh = true; // bool? | Aggiorna dopo l'applicazione.
var folder = "myFolder"; // string (opzionale)
var storageName = null; // string (opzionale)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Eccezione durante la chiamata a AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (opzionale)
            undefined              // storageName (opzionale)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Frammenti simili sono disponibili per Ruby, PHP, Go e Perl nel repository ufficiale degli SDK.)*

## Argomenti correlati

- **Aggiungere un filtro automatico standard** – [Aggiungere un filtro standard](/autofilter/add-filter)  
- **Aggiungere un filtro data** – [Aggiungere un filtro data](/autofilter/add-date-filter)  
- **Eliminare un filtro automatico** – [Eliminare il filtro automatico](/autofilter/delete-filter)  
- **Lavorare con i fogli di lavoro** – [Panoramica dell'API Fogli di lavoro](/worksheets/)

## Note

* Tutte le immagini utilizzate nella documentazione originale sono state verificate per l'accessibilità. Le icone decorative sono contrassegnate con `alt=""` e `role="presentation"`; le icone funzionali mantengono un testo descrittivo per l'attributo `alt`.  
* Le parole chiave meta sono state pulite rimuovendo voci vuote e duplicati.  
* La pagina ora segue una chiara gerarchia di titoli (un solo H1 nel front matter, H2 per le sezioni principali, H3/H4 per le sottosezioni), migliorando il SEO e la navigazione con gli screen reader.  

---