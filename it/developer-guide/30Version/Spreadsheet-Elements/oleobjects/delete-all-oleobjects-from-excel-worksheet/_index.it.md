---
---
title: Elimina tutti gli oggetti OLE in un foglio di calcolo Excel
description: Scopri come rimuovere tutti gli oggetti OLE da un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempi di richiesta/risposta, frammenti di SDK, autenticazione, gestione degli errori e domande frequenti.
keywords: Aspose.Cells Cloud, eliminare oggetti OLE, API Excel, API REST, pulizia OLE foglio di calcolo, SDK cloud
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Elimina tutti gli oggetti OLE in un foglio di calcolo Excel

**OleObjects – Clear** rimuove **tutti** gli oggetti OLE (Object Linking and Embedding, ovvero collegamento e incorporazione di oggetti) da un foglio di calcolo specificato, lasciando intatti i dati delle celle. Questa operazione è utile per pulire fogli di calcolo obsoleti o preparare un workbook per una ridistribuzione.

---

## Prerequisiti

- Un **token di accesso JWT Aspose Cloud** valido (OAuth 2.0).  
- Il workbook di destinazione deve essere archiviato in Aspose Cloud (o devi specificare la `folder`/`storageName` in cui si trova).  
- Versione API **v3.0** o successiva.  

> **Nota:** L'operazione è *idempotente* – richiamarla quando non sono presenti oggetti OLE restituisce un esito positivo `200 OK`.

---

## Richiesta HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Parametri del percorso

| Nome      | Tipo   | Obbligatorio | Descrizione                          |
|-----------|--------|--------------|--------------------------------------|
| `name`    | string | ✔️           | Nome del file del workbook.          |
| `sheetName`| string | ✔️           | Nome del foglio di calcolo.          |

### Parametri di query

| Nome          | Tipo   | Obbligatorio | Descrizione                                  |
|---------------|--------|--------------|----------------------------------------------|
| `folder`      | string | opzionale    | Cartella contenente il workbook.             |
| `storageName` | string | opzionale    | Nome dello storage in cui si trova il workbook. |

**Intestazioni**

| Intestazione         | Valore                        |
|----------------------|-------------------------------|
| `Authorization`      | `Bearer <jwt token>`          |
| `Accept`             | `application/json`            |
| `Content-Type`       | `application/json`            |

---

## Esempio di richiesta (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*Sostituisci `<jwt token>` con un token di accesso valido e adatta `folder`/`storageName` secondo le tue esigenze.*

---

## Risposta corretta

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                              |
|--------|-----------------------------|----------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                         |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.        |
| 500    | Errore interno del server   | Errore imprevisto nel server.                            |
---

## Esempi di SDK

I seguenti frammenti di codice mostrano come richiamare **DeleteWorksheetOleObjects** con gli SDK ufficiali di Aspose.Cells Cloud. Sostituisci i valori segnaposto (`<YOUR_TOKEN>`, `<FILE_NAME>`, ecc.) con i tuoi dati.

| Linguaggio | Esempio |
|------------|---------|
| **C#** | <details><summary>Mostra esempio C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>Mostra esempio Java</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>Mostra esempio Python</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Mostra esempio Node.js</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('Tutti gli oggetti OLE eliminati'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Mostra esempio Go</summary>```go\npackage main\nimport (\n    \"context\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_TOKEN>\"\n    cfg.Host = \"https://api.aspose.cloud\"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), \"Sample.xlsx\", \"Sheet1\", map[string]interface{}{ \"folder\": \"Samples\" })\n    if err != nil { panic(err) }\n    println(\"Tutti gli oggetti OLE eliminati\")\n}\n```</details> |

*I file sorgente completi per tutti i linguaggi supportati sono disponibili nel [repository GitHub di Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).*

---

## Errori e gestione

- **Idempotenza** – Eliminare gli oggetti OLE in un foglio che ne contiene già nessuno restituisce comunque `200 OK`.  
- **Scadenza del token** – Se ricevi `401 Non autorizzato`, ottieni un nuovo token JWT e riprova.  
- **Nome del foglio non valido** – Assicurati che il nome del foglio corrisponda esattamente (in maiuscolo/minuscolo) a quello nel workbook; altrimenti verrà restituito un `400 Richiesta non valida`.  

Implementa logica di ritentativo con backoff esponenziale per errori transitori `500`.

---

## Domande frequenti

**Q1: Devo specificare i parametri `folder` e `storageName`?**  
**A:** No. Se omessi, Aspose Cloud assume lo storage predefinito e la cartella principale.

**Q2: Posso eliminare gli oggetti OLE da una cella specifica?**  
**A:** Questo endpoint elimina **tutti** gli oggetti OLE nel foglio di calcolo. Per rimuovere un singolo oggetto, utilizza l'operazione *Elimina un oggetto OLE specifico*.

**Q3: Cosa succede se il workbook è bloccato per la modifica?**  
**A:** L'API restituirà `400 Richiesta non valida` con un messaggio che indica che il file è bloccato. Assicurati che il file non sia aperto altrove prima di chiamare l'endpoint.

**Q4: Esiste un limite di dimensione per il workbook?**  
**A:** Il servizio rispetta i limiti generali di Aspose Cloud per le dimensioni dei file (attualmente fino a 2 GB per file). File più grandi potrebbero richiedere la divisione o l'elaborazione a blocchi.

---

## Best practice

- **Prestazioni** – Utilizza gli attributi `async` o `defer` quando carichi script di terze parti nel tuo sito di documentazione, per ridurre il tempo di caricamento iniziale della pagina.  
- **Sicurezza** – Aggiungi `rel="noopener noreferrer"` a qualsiasi link esterno che si apre in una nuova scheda.  
- **Accessibilità** – Le icone decorative (ad es. frecce verso il basso nelle barre laterali) dovrebbero avere `alt=""` e `role="presentation"` per rispettare gli standard WCAG AA.  
- **Coerenza** – Mantieni i formati di data in ISO‑8601 (`AAAA-MM-GG`) per evitare artifact di codifica.

---

## Operazioni correlate

- **Aggiungi oggetto OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Elimina un oggetto OLE specifico** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Usa i link di navigazione in fondo alla pagina per spostarti tra le azioni API correlate.

---
---