---
title: "Elimina tutte le tabelle pivot in un foglio Excel"
description: "Elimina tutte le tabelle pivot da un foglio specificato utilizzando l'API REST Aspose.Cells Cloud."
keywords: "Aspose.Cells, Tabella Pivot, Elimina, API REST, Excel"
date: 2026-07-30
api_version: "v3.0"
---

# Elimina tutte le tabelle pivot in un foglio Excel

## Panoramica
Questa operazione rimuove **tutte** le tabelle pivot da un determinato foglio in un file Excel. È utile quando è necessario ripristinare l’analisi di un foglio o pulire tabelle pivot inutilizzate in un’unica chiamata.

## Prerequisiti
Prima di chiamare l’API, assicurati di aver completato i seguenti passaggi:

1. **Account Aspose Cloud** – Registrati per un account Aspose Cloud se non ne hai già uno.  
2. **Token JWT** – Genera un token JSON Web Token (JWT) per l’autenticazione. Consulta la [guida all’autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) per i dettagli.  
3. **Configurazione dello storage** – Carica il file Excel di destinazione nello storage di Aspose Cloud o in uno storage esterno collegato. Individua la **cartella** e il **nome dello storage** (se applicabile) in cui si trova il file.

## Autenticazione
Le API Aspose.Cells Cloud richiedono **autenticazione basata su token JWT**. Includi il token nell’intestazione `Authorization` di ogni richiesta:

```
Authorization: Bearer <jwt token>
```

## Richiesta HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### Parametri del percorso
| Nome | Tipo   | Obbligatorio | Descrizione |
|------|--------|--------------|-------------|
| `name` | string | Sì | Il nome del file Excel (ad esempio `Sample.xlsx`). |
| `sheetName` | string | Sì | Il nome del foglio da cui verranno rimosse tutte le tabelle pivot (ad esempio `Sheet1`). |

### Parametri di query
| Nome | Tipo   | Obbligatorio | Descrizione |
|------|--------|--------------|-------------|
| `folder` | string | No | La cartella contenente il file. |
| `storageName` | string | No | Il nome dello storage da utilizzare (se il file non si trova nello storage predefinito). |

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables?folder=SampleFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

## Risposta in caso di successo
Il servizio restituisce un oggetto standard `CellsCloudResponse` che indica lo stato dell’operazione.

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## Gestione degli errori

| Stato HTTP | Significato | Payload di esempio |
|------------|-------------|--------------------|
| **400** | Richiesta non valida – parametri mancanti o non validi | `{ "Code": 400, "Message": "Parametro obbligatorio 'name' mancante." }` |
| **401** | Non autorizzato – token JWT non valido o scaduto | `{ "Code": 401, "Message": "Token di autenticazione non valido." }` |
| **404** | Non trovato – il file o il foglio non esiste | `{ "Code": 404, "Message": "Foglio non trovato." }` |
| **500** | Errore interno del server – errore imprevisto | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

## Esempi di SDK

I frammenti seguenti mostrano come richiamare l’operazione utilizzando diversi SDK di Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Inizializza il client API
var apiInstance = new CellsApi("<client-id>", "<client-secret>");

// Configura i parametri della richiesta
string name = "Sample_Pivot_Table_Example.xls";
string sheetName = "Sheet2";
string folder = "SampleFolder";
string storageName = "MyStorage";

try
{
    var response = apiInstance.DeleteWorksheetPivotTables(name, sheetName, folder, storageName);
    Console.WriteLine($"Codice risposta: {response.Code}, stato: {response.Status}");
}
catch (Exception e)
{
    Console.WriteLine("Eccezione durante la chiamata a CellsApi.DeleteWorksheetPivotTables: " + e.Message);
}
```

### Java

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

public class DeletePivotTables {
    public static void main(String[] args) {
        CellsApi api = new CellsApi("<client-id>", "<client-secret>");
        String name = "Sample_Pivot_Table_Example.xls";
        String sheetName = "Sheet2";
        String folder = "SampleFolder";
        String storageName = "MyStorage";

        try {
            CellsCloudResponse result = api.deleteWorksheetPivotTables(name, sheetName, folder, storageName);
            System.out.println("Codice: " + result.getCode() + ", Stato: " + result.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python

```python
import asposecellscloud_sdk
from asposecellscloud_sdk import CellsApi, ApiException

# Configura il client API
configuration = asposecellscloud_sdk.Configuration()
configuration.api_key['client_id'] = '<client-id>'
configuration.api_key['client_secret'] = '<client-secret>'

api_instance = CellsApi(asposecellscloud_sdk.ApiClient(configuration))

name = 'Sample_Pivot_Table_Example.xls'
sheet_name = 'Sheet2'
folder = 'SampleFolder'
storage_name = 'MyStorage'

try:
    response = api_instance.delete_worksheet_pivot_tables(name, sheet_name, folder, storage_name)
    print(f'Codice: {response.code}, Stato: {response.status}')
except ApiException as e:
    print("Eccezione durante la chiamata a CellsApi->delete_worksheet_pivot_tables: %s\n" % e)
```

### Node.js

```javascript
const { CellsApi, Configuration } = require('asposecellscloud-sdk');

const config = new Configuration({
    clientId: '<client-id>',
    clientSecret: '<client-secret>'
});
const apiInstance = new CellsApi(config);

const name = 'Sample_Pivot_Table_Example.xls';
const sheetName = 'Sheet2';
const folder = 'SampleFolder';
const storageName = 'MyStorage';

apiInstance.deleteWorksheetPivotTables(name, sheetName, folder, storageName)
    .then(result => {
        console.log(`Codice: ${result.code}, Stato: ${result.status}`);
    })
    .catch(err => {
        console.error('Errore:', err);
    });
```

*Altri SDK (Go, PHP, Ruby, Swift, Perl, Android) sono disponibili nel [repository degli SDK di Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

## Vedere anche
- [Elimina una tabella pivot specifica](https://docs.aspose.cloud/cells/pivot-tables/delete-specific/)
- [Ottieni tutte le tabelle pivot in un foglio](https://docs.aspose.cloud/cells/pivot-tables/get-all/)
- [Panoramica sull'autenticazione](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)
- [Specifiche OpenAPI per DeleteWorksheetPivotTables](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables)

---

*Documento aggiornato l'ultima volta il 2026-07-30. Tutti i contenuti sono codificati in UTF-8.*