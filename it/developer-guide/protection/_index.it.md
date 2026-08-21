---
title: "Aspose.Cells Cloud Web API – Imposta / Modifica la Password di Apertura per i File Excel"
second_title: "Guida Completa per gli Sviluppatori"
ArticleTitle: "Protezione del Foglio di Calcolo – Imposta la Password di Apertura e di Modifica"
linktitle: "Protezione"
type: docs
url: /it/protection/
keywords: "Aspose.Cells, Cloud, API, Foglio di Calcolo, Protezione, Password di Apertura, Password di Scrittura, Excel"
description: "Scopri come proteggere un libro Excel con una password di apertura o di scrittura utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, esempi di codice e gestione degli errori."
weight: 60
---

In questa guida imparerai come impostare, modificare e rimuovere sia la **password di apertura** sia la **password di scrittura** per i fogli di calcolo utilizzando l'API Web Aspose.Cells Cloud. Queste funzionalità aiutano a proteggere dati sensibili nei tuoi libri Excel.

**Prerequisiti**  
- Un account attivo Aspose.Cells Cloud con una chiave API e un SID validi.  
- Il libro che desideri proteggere deve essere caricato nello storage Aspose Cloud o accessibile tramite un URL pubblico.  

**Riferimento API**  

| **Metodo HTTP** | **Endpoint** | **Parametri di Query / Path** | **Descrizione** |
|-----------------|--------------|-------------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (path) – nome del libro<br>`openPassword` (query, facoltativo) – password richiesta per aprire il file<br>`readWritePassword` (query, facoltativo) – password richiesta per modificare il file | Imposta o aggiorna le password di apertura e/o di scrittura per il libro specificato. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (path) – nome del libro | Rimuove eventuali password che proteggono il libro. |

**Esempio di Corpo della Richiesta (JSON)**  

```json
{
  "OpenPassword": "LaMiaPasswordApertura123",
  "ReadWritePassword": "LaMiaPasswordModifica456"
}
```

**Esempio di Risposta (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Protezione del libro aggiornata correttamente."
}
```

**Codici di Stato HTTP**

| Codice | Significato                   | Descrizione                                        |
|--------|-------------------------------|----------------------------------------------------|
| 200    | OK                            | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Errata              | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non Autorizzato               | Token JWT non valido o mancante. |
| 413    | Payload Troppo Grande         | Il file caricato supera il limite di dimensione. |
| 500    | Errore Interno del Server     | Errore imprevisto sul server. |

**Esempi di Codice**

*C# (SDK Aspose.Cells Cloud)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Esempio.xlsx",
    openPassword: "LaMiaPasswordApertura123",
    readWritePassword: "LaMiaPasswordModifica456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (SDK Aspose.Cells Cloud)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Esempio.xlsx",
    open_password="LaMiaPasswordApertura123",
    read_write_password="LaMiaPasswordModifica456"
)
api.set_workbook_protection(request)
```

**Gestione degli Errori**  
Quando si verifica un errore, l'API restituisce un payload JSON contenente `Code`, `Message` e, opzionalmente, `Description`. Controlla il codice di stato e gestiscilo di conseguenza nella logica della tua applicazione.

**Argomenti Correlati**  

- **[Come proteggere un foglio di calcolo con una password utilizzando Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Come rimuovere la protezione da un foglio di calcolo con una password utilizzando Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---