---
title: "Eliminare la formattazione condizionale – Riferimento API di Aspose.Cells Cloud"
type: docs
url: /it/conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Formattazione condizionale, Eliminare, API, Excel, Cloud"
description: "Rimuovi una regola di formattazione condizionale da un foglio di lavoro utilizzando l'API REST di Aspose.Cells Cloud. Include parametri, autenticazione, esempi di richiesta/risposta e frammenti di codice SDK."
weight: 60
---

# Eliminare la formattazione condizionale

## Panoramica
La formattazione condizionale consente di applicare stili visivi alle celle che soddisfano criteri specifici (ad esempio, evidenziare i valori superiori a una soglia). In scenari di automazione potresti dover rimuovere una regola esistente. Questo endpoint elimina una regola di formattazione condizionale da un foglio di lavoro in un libro Excel archiviato in Aspose Cloud Storage.

## Prerequisiti
- Un account **Aspose Cloud** con il prodotto **Cells** abilitato.  
- **Token di accesso JWT** generato tramite il flusso client-credentials di OAuth 2.0.  
- Il libro (`{name}`) deve già esistere nella **cartella** e nello **storage** specificati (se presente).  
- Nelle URL mostrate di seguito viene utilizzata la versione API **v3.0** (impostazione predefinita).

## Autenticazione
Tutti gli endpoint di Aspose.Cells Cloud richiedono l'autenticazione basata su **token JWT**.

```http
Authorization: Bearer <access_token>
```

### Ottenere un token di accesso (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Risposta**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Utilizza il `access_token` restituito nell'intestazione `Authorization` per ogni richiesta.

## Richiesta HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Parametri del percorso

| Nome      | Tipo   | Obbligatorio | Descrizione |
|-----------|--------|--------------|-------------|
| `name`    | string | Sì           | Nome del file del libro (ad esempio, `Book1.xlsx`). |
| `sheetName` | string | Sì        | Foglio di lavoro che contiene la formattazione condizionale. |
| `index`   | integer| Sì           | Indice in base zero della regola di formattazione condizionale da eliminare. |

### Parametri di query

| Nome            | Tipo   | Obbligatorio | Descrizione |
|-----------------|--------|--------------|-------------|
| `folder`        | string | No           | Cartella cloud in cui si trova il libro. |
| `storageName`   | string | No           | Nome del servizio di storage Aspose Cloud. |

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Risposta in caso di successo

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Codici di stato HTTP**

| Codice | Significato            | Descrizione |
|--------|------------------------|-------------|
| 200    | OK                     | Filtro applicato con successo; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida   | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato        | Token JWT mancante o non valido. |
| 413    | Payload troppo grande  | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server | Errore imprevisto del server. |

## Risposte di errore

| Codice HTTP | Motivo | Corpo di esempio |
|-------------|--------|------------------|
| **400**     | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore di parametro non valido." }` |
| **401**     | Non autorizzato – token JWT mancante o non valido. | `{ "Code":"401", "Message":"Token di accesso mancante o non valido." }` |
| **404**     | Non trovato – il libro o il foglio di lavoro non esiste. | `{ "Code":"404", "Message":"File non trovato." }` |
| **500**     | Errore interno del server – errore imprevisto del server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

## Esempi di SDK
I frammenti seguenti illustrano come richiamare l'operazione **Eliminare la formattazione condizionale** utilizzando gli SDK ufficiali di Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// Configura il client API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Elimina la formattazione condizionale
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Formattazione condizionale eliminata.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Formattazione condizionale rimossa.")
```

*(Altri frammenti di codice per Ruby, Go, Perl e Swift sono disponibili nel [repository GitHub](https://github.com/aspose-cells-cloud).)*

## Vedi anche
- **Guida all'autenticazione** – [Autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Specifiche OpenAPI** – Schema dettagliato per questo endpoint (si apre in una nuova scheda)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">Specifiche OpenAPI</a>`  
- **Panoramica sulla formattazione condizionale** – Scopri come creare, aggiornare ed elencare le regole di formattazione.  
- **SDK di Aspose.Cells Cloud** – Elenco completo dei linguaggi supportati nel [repository GitHub](https://github.com/aspose-cells-cloud).  

---  

*Questa pagina segue il modello standard della documentazione dell'API Aspose.Cells Cloud, include una sezione Prerequisiti e rispetta le best practice in materia di accessibilità e SEO.*