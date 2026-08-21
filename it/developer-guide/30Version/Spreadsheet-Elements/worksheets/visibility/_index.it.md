---
title: "Come gestire la visibilità in un foglio di lavoro di Excel"
second_title: "Documento"
linktitle: "Visibilità"
type: docs
url: /it/worksheets/panes/
keywords: "Aspose.Cells Cloud, API per nascondere fogli di lavoro, API per mostrare fogli di lavoro, visibilità fogli di lavoro Excel, API REST Excel, Aspose.Cells v3.0"
description: "Impara a nascondere o mostrare programmaticamente i fogli di lavoro di Excel utilizzando l'API REST Aspose.Cells Cloud. Include URL delle richieste, esempi cURL e .NET SDK, gestione degli errori e note specifiche per la versione."
weight: 20
---

## Gestione della visibilità in un foglio di lavoro di Excel

*La visibilità del foglio di lavoro* definisce se una scheda è visualizzata all'utente finale. Con Aspose.Cells Cloud puoi nascondere o mostrare un foglio di lavoro tramite una semplice chiamata REST. Gli endpoint API utilizzati sono:

* **Nascondere un foglio di lavoro** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Mostrare un foglio di lavoro** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Versione API supportata:** **v3.0** (a partire da marzo 2026)

### Prerequisiti
1. Un account **Aspose.Cells Cloud** attivo.  
2. Un **client ID** e un **client secret** validi (o un token di accesso OAuth 2.0).  
3. Il cartellone di lavoro (`{fileName}`) deve essere già caricato nello storage cloud di Aspose.  

---

## Nascondere un foglio di lavoro

### Richiesta
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Risposta
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Esempio cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Esempio .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Foglio di lavoro nascosto: {response.Worksheet.Visible}");
```

### Errori comuni
| Codice HTTP | Descrizione                              | Soluzione                                                                 |
|-------------|------------------------------------------|---------------------------------------------------------------------------|
| 400         | Corpo JSON non valido o `Visible` mancante | Assicurati che il corpo della richiesta sia JSON valido con la chiave.    |
| 401         | Non autorizzato – token mancante/scaduto | Aggiorna il token OAuth e includilo nell'header.                          |
| 404         | Foglio di lavoro o file non trovato       | Verifica che `{fileName}` e `{sheetName}` siano corretti.                 |
| 409         | Foglio di lavoro già nascosto             | Controlla la visibilità corrente prima di inviare la richiesta.          |

---

## Mostrare un foglio di lavoro

### Richiesta
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Risposta
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Esempio cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Esempio .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Foglio di lavoro visibile: {response.Worksheet.Visible}");
```

### Errori comuni
| Codice HTTP | Descrizione                              | Soluzione                                                                 |
|-------------|------------------------------------------|---------------------------------------------------------------------------|
| 400         | Corpo JSON non valido o `Visible` mancante | Fornisci un payload JSON corretto con `"Visible": true`.                 |
| 401         | Non autorizzato – token mancante/scaduto | Rigenera il token di accesso e riprova.                                   |
| 404         | Foglio di lavoro o file non trovato       | Conferma che i nomi del file e del foglio esistono nello storage.         |
| 409         | Foglio di lavoro già visibile             | Nessuna azione necessaria; il foglio di lavoro è già mostrato.           |

---

## Operazioni correlate
> *Blocca riquadri* | *Dividi riquadri* | *Zoom* – consulta le pagine corrispondenti per ulteriori controlli sul layout del foglio di lavoro.

---

## Domande frequenti

<dl>
  <dt>Come nascondo un foglio di lavoro usando l'API Aspose.Cells Cloud?</dt>
  <dd>Inviare una richiesta `PUT` a `/cells/{fileName}/worksheets/{sheetName}/visibility` con il corpo JSON `{ "Visible": false }`. Includere un token bearer OAuth 2.0 valido. Una risposta `200 OK` restituisce l'oggetto foglio di lavoro aggiornato.</dd>

  <dt>Quale risposta ricevo dopo aver mostrato un foglio di lavoro?</dt>
  <dd>L'API restituisce `200 OK` con un payload contenente l'oggetto foglio di lavoro in cui `"Visible": true`. La risposta include le proprietà `Name`, `Index` e `Visible` del foglio di lavoro.</dd>

  <dt>Posso nascondere più fogli di lavoro in una singola chiamata?</dt>
  <dd>No. L'endpoint per la visibilità funziona su un singolo foglio di lavoro identificato da `{sheetName}`. Per nascondere più fogli, iterare su ciascun nome nel proprio codice client.</dd>
</dl>

---

*Scritto dal team Aspose Docs – oltre 15 anni di esperienza nell'automazione dei flussi di lavoro di Excel.*