---
---
title: "Come lavorare con l'eliminazione dei fogli di calcolo in un libro Excel"
second_title: "Document"
linktype: "Elimina"
type: docs
url: /it/worksheets/delete/
keywords: "Aspose.Cells, Cloud, REST API, Elimina Foglio di Calcolo, Excel, C#, Java, Python"
description: "Scopri come eliminare uno o più fogli di calcolo da un libro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi in C#, Java e Python, prerequisiti, suggerimenti sulla gestione degli errori e operazioni correlate."
weight: 20
ArticleTitle: "Elimina Foglio(i) in un Libro Excel con l'API di Aspose.Cells Cloud"
---

## Lavorare con l'Eliminazione di Fogli di Calcolo in un Libro Excel

Quando un'applicazione genera o modifica dinamicamente file Excel, potresti aver bisogno di rimuovere fogli di calcolo che non sono più necessari—come report temporanei, fogli di segnaposto o dati obsoleti. L'API REST di Aspose.Cells Cloud rende semplice eliminare un singolo foglio di calcolo o più fogli in una singola richiesta.

**Riferimento API**  

| Elemento | Dettagli |
|----------|----------|
| **Metodo HTTP** | `DELETE` |
| **Endpoint** | `/cells/{fileName}/worksheets` |
| **Parametri di percorso** | `fileName` – nome del file Excel (obbligatorio) |
| **Parametri di query** | `sheetName` – nome del foglio di calcolo da eliminare (opzionale, per l'eliminazione singola) <br> `folder` – cartella di origine nello storage (opzionale) <br> `storage` – nome dello storage (opzionale) |
| **Corpo della richiesta** | *Nessuno* |
| **Risposta di successo** | `200 OK` – foglio/i di calcolo eliminato/i correttamente. Restituisce un oggetto JSON contenente lo stato dell'operazione. |
| **Risposte di errore** | `400 Bad Request` – parametri non validi <br> `401 Unauthorized` – fallimento dell'autenticazione <br> `404 Not Found` – file o foglio di calcolo non trovato <br> `500 Internal Server Error` – problema lato server |

**Richiesta**  

Per eliminare uno o più fogli di calcolo, invia una richiesta `DELETE` all'endpoint sopra indicato, includendo il parametro obbligatorio `fileName` e, opzionalmente, il parametro di query `sheetName` per l'eliminazione di un singolo foglio. Quando `sheetName` è omesso, tutti i fogli di calcolo nel libro vengono rimossi.

**Parametri**  

- `fileName` (stringa, obbligatorio): Il nome del file Excel, incluso l'estensione.  
- `sheetName` (stringa, opzionale): Nome specifico del foglio di calcolo da eliminare. Se omesso, l'API elimina tutti i fogli di calcolo.  
- `folder` (stringa, opzionale): Percorso della cartella contenente il file nello storage.  
- `storage` (stringa, opzionale): Nome dello storage Aspose Cloud da utilizzare.

**Risposte**  

- **200 OK** – Esempio JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Foglio/i di calcolo eliminato/i correttamente."
  }
  ```
- **400 Bad Request** – Parametri della richiesta non validi.  
- **401 Unauthorized** – Token di autenticazione mancante o non valido.  
- **404 Not Found** – Il file o il foglio di calcolo specificato non esiste.  
- **500 Internal Server Error** – Errore imprevisto del server.

**Esempi**  

*Di seguito sono riportati brevi frammenti di codice che mostrano come chiamare l'endpoint di eliminazione utilizzando tre linguaggi popolari.*

**Esempio in C#**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Stato: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Errore: {ex.Message}");
}
```

**Esempio in Java**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Stato: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Errore: " + e.getMessage());
        }
    }
}
```

**Esempio in Python**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Stato: {response.status}")
except ApiException as e:
    print(f"Errore: {e}")
```

**Gestione degli errori**  

- Verifica che il token di autenticazione sia valido prima di effettuare la richiesta.  
- Controlla il codice di stato della risposta; gestisci opportunamente `400`, `401`, `404` e `500`.  
- Utilizza blocchi try-catch (o equivalenti) per catturare eccezioni di rete o dell'SDK.

**Operazioni correlate**  

- [Aggiungi un foglio di calcolo](/it/worksheets/add/) – Crea un nuovo foglio di calcolo in un libro esistente.  
- [Copia un foglio di calcolo](/it/worksheets/copy/) – Duplica un foglio di calcolo esistente.  
- [Rinomina un foglio di calcolo](/it/worksheets/rename/) – Modifica il nome di un foglio di calcolo.  
- [Sposta un foglio di calcolo](/it/worksheets/move/) – Riordina i fogli di calcolo all'interno di un libro.  
---