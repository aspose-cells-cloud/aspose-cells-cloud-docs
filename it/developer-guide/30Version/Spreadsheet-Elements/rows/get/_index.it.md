---
---
title: "Recuperare una singola riga da un foglio di calcolo Excel utilizzando l'API Aspose.Cells Cloud"
description: "Scopri come recuperare una riga specifica da un foglio di calcolo Excel memorizzato nell'archivio Aspose Cloud utilizzando l'API REST Aspose.Cells Cloud. Include la sintassi della richiesta, i parametri, lo schema della risposta, un esempio cURL e il codice SDK (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, recupera riga, API Excel, spreadsheet REST, SDK C#, SDK Java, SDK Python"
date: 2026-07-30
api_version: "v3.0"
---

# Recuperare una singola riga da un foglio di calcolo Excel

**Endpoint**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Recupera una riga da un foglio di calcolo memorizzato nell'archivio Aspose Cloud. L'operazione richiede un token di accesso OAuth 2.0 valido con ambito **Read**.

---

## Indice
1. [Prerequisiti](#prerequisiti)  
2. [Richiesta HTTP](#richiesta-http)  
3. [Parametri](#parametri)  
   - [Parametri nel percorso](#parametri-nel-percorso)  
   - [Parametri di query](#parametri-di-query)  
4. [Esempio cURL](#esempio-curl)  
5. [Risposta](#risposta)  
   - [Schema di successo](#schema-di-successo)  
   - [Codici di stato](#codici-di-stato)  
6. [Esempi di codice SDK](#esempi-di-codice-sdk)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [Operazioni correlate](#operazioni-correlate)  
8. [Note e limiti](#note-e-limiti)  

---

## Prerequisiti
- **Account Aspose Cloud** con un abbonamento attivo.  
- **Token di accesso OAuth 2.0** che include l'ambito **Read**.  
- Il libro di lavoro di destinazione deve già esistere nell'archivio Aspose Cloud.  

---

## Richiesta HTTP
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*URL di base*: `https://api.aspose.cloud/v3.0`

---

## Parametri

### Parametri nel percorso
| Nome      | Tipo   | Obbligatorio | Descrizione                         |
|-----------|--------|--------------|-------------------------------------|
| `name`    | string | ✅           | Nome del file del libro di lavoro (ad esempio, `MioLibro.xlsx`). |
| `sheetName`| string | ✅          | Nome del foglio di calcolo (ad esempio, `Foglio1`). |
| `rowIndex`| integer| ✅           | Indice in base zero della riga da recuperare. |

### Parametri di query *(opzionali)*
| Nome            | Tipo   | Obbligatorio | Descrizione |
|-----------------|--------|--------------|-------------|
| `folder`        | string | ❌           | Percorso della cartella nell'archivio cloud in cui risiede il libro di lavoro. |
| `storageName`   | string | ❌           | Nome del servizio di archiviazione (se si utilizza un archivio personalizzato). |

---

## Esempio cURL
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MioLibro.xlsx/worksheets/Foglio1/rows/5?folder=Docs&storageName=MioArchivio" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Risposta

### Schema di successo (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* oggetto stile */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...celle aggiuntive... */
    ]
  }
}
```

### Codici di stato
| Codice | Significato |
|--------|-------------|
| **200** | Riga recuperata con successo. |
| **401** | Non autorizzato – token di accesso mancante o non valido. |
| **404** | Libro di lavoro, foglio di calcolo o riga non trovato. |
| **500** | Errore interno del server. |

### Esempio di errore (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Il token di accesso è mancante o non valido."
}
```

---

## Esempi di codice SDK

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MioLibro.xlsx",
    sheetName: "Foglio1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // opzionale
);

Console.WriteLine($"Riga {response.Row.Index} recuperata con {response.Row.Cells.Count} celle.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MioLibro.xlsx",
    "Foglio1",
    5,
    "Docs",
    null   // storageName – opzionale
);

System.out.println("Indice riga: " + response.getRow().getIndex());
System.out.println("Numero di celle: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MioLibro.xlsx",
        sheet_name="Foglio1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Riga {response.row.index} recuperata con {len(response.row.cells)} celle.")
except ApiException as e:
    print("Eccezione durante la chiamata a CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## Operazioni correlate
| Operazione | Descrizione |
|------------|-------------|
| **Aggiungi riga** | `POST /cells/{name}/worksheets/{sheetName}/rows` – Inserisce una nuova riga in un foglio di calcolo. |
| **Elimina riga** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – Rimuove una riga esistente. |
| **Recupera righe multiple** | `GET /cells/{name}/worksheets/{sheetName}/rows` – Recupera un insieme di righe. |
| **Panoramica righe** | `/cells/rows/` – Documentazione generale sugli endpoint relativi alle righe. |

---

## Note e limiti
- **Limite di richieste**: 100 richieste al minuto per account.  
- **Formati supportati**: XLS, XLSX, CSV, ODS.  
- L'indice della riga è in **base zero**; la prima riga ha indice `0`.  
- Assicurarsi che il libro di lavoro sia caricato nella cartella specificata prima di chiamare questo endpoint.  

---