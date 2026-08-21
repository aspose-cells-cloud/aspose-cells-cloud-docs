---
title: "Come ottenere il contenuto di un intervallo da un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Ottieni"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, ottieni, intervallo, foglio di calcolo, REST"
description: "Scopri come recuperare il contenuto di un intervallo da un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta e codice di esempio."
weight: 20
ArticleTitle: "Come ottenere il contenuto di un intervallo da un foglio di calcolo Excel – Aspose.Cells Cloud API"
---

## Lavorare con il recupero del contenuto di un intervallo in un foglio di calcolo Excel

- [Come ottenere i dati di una cella in base a un intervallo con nome](/cells/ranges/get/values/)
- [Come ottenere un intervallo con nome da un libro Excel](/cells/ranges/get/name/)

**Prerequisiti**

- Un token di accesso valido per Aspose Cloud (oppure `client_id`/`client_secret` per OAuth).
- Il file Excel deve essere caricato nella cartella di archiviazione di destinazione.
- Aspose.Cells Cloud SDK versione 3.0 o successiva.

L'operazione **Ottieni intervallo** restituisce il contenuto di un intervallo specificato in un foglio di calcolo.  
Si tratta di una semplice richiesta `GET` che restituisce i dati dell'intervallo in formato JSON (o altri formati, su richiesta).

**Panoramica della richiesta**

| Elemento | Valore |
|---------|-------|
| **Metodo HTTP** | `GET` |
| **Endpoint** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Parametri di percorso** | `fileName` – nome del file Excel (inclusa estensione) <br> `sheetName` – nome del foglio di calcolo <br> `rangeName` – nome dell'intervallo (ad es., `A1:B10`) |
| **Parametri di query** (opzionali) | `folder` – cartella di archiviazione <br> `storage` – nome dell'archivio <br> `outFormat` – formato della risposta (ad es., `json`, `xml`) |
| **Intestazioni** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Esempio di cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**Esempio in C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Esempio in Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Esempio in Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Schema della risposta (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**Codici di stato HTTP**

| Codice | Significato                     | Descrizione                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida          | Parametri mancanti o non validi (ad es., tipo di file non supportato). |
| 401  | Non autorizzato               | Token JWT non valido o mancante. |
| 413  | Payload troppo grande         | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server     | Errore imprevisto del server. |

- `200 OK` – Intervallo recuperato correttamente.  
- `400 Bad Request` – Parametri mancanti o non validi.  
- `401 Unauthorized` – Token di accesso non valido o mancante.  
- `404 Not Found` – Il file, il foglio di calcolo o l'intervallo specificato non è stato trovato.  
- `500 Internal Server Error` – Errore imprevisto del server.

**Esempi di risposta di errore**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "I parametri della richiesta non sono validi o mancanti."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Token di accesso non valido o mancante."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "Impossibile trovare il file, il foglio di calcolo o l'intervallo specificato."
}
```

**Vedi anche**

- [Come ottenere i dati di una cella in base a un intervallo con nome](/cells/ranges/get/values/)  
- [Come ottenere un intervallo con nome da un libro Excel](/cells/ranges/get/name/)  
- [Aggiorna il contenuto di un intervallo](/cells/ranges/update/)  
- [Elimina un intervallo](/cells/ranges/delete/)  
---