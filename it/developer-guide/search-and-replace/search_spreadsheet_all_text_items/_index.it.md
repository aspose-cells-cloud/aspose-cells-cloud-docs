---
title: "Cerca Tutti gli Elementi di Testo nel Foglio di Calcolo"
ArticleTitle: "Cerca Tutti gli Elementi di Testo nel Foglio di Calcolo – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Cerca Tutti gli Elementi di Testo nel Foglio di Calcolo"
type: docs
url: /cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, Cerca, Elementi di Testo, API"
description: "Cerca tutti gli elementi di testo all'interno di un file di foglio di calcolo utilizzando l'API Aspose.Cells Cloud."
weight: 100
---

## La funzione Cerca Tutti gli Elementi di Testo nel Foglio di Calcolo dei Servizi Web Aspose.Cells Cloud

Questo metodo consente di cercare tutti gli elementi di testo all'interno di un file di foglio di calcolo locale. Supporta la ricerca in tutti i fogli e le celle del workbook, identificando le occorrenze del termine cercato. L'operazione viene eseguita lato cloud, senza richiedere archiviazione cloud. Assicurati di disporre delle autorizzazioni necessarie per leggere il file sorgente. Se il file sorgente non è accessibile o si verifica un errore durante il processo di ricerca (ad esempio, un formato di file non supportato), verrà generata un’eccezione appropriata. Il metodo può restituire le posizioni delle corrispondenze (ad esempio, nome del foglio, coordinate della cella), a seconda dei dettagli dell'implementazione.

### Endpoint Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **Sicurezza e Autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro | Tipo | Percorso/Query String/Corpo HTTP | Descrizione |
|----------------|------|----------------------------------|-------------|
| Spreadsheet | File | FormData | Carica il file del foglio di calcolo. |
| region | String | Query | Impostazione di area/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l’analisi delle date e il comportamento specifico della località. |
| password | String | Query | La password per aprire il file del foglio di calcolo. |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [DA DEFINIRE] | [DA DEFINIRE] | [DA DEFINIRE] |

### **Risposta**

```json
{
  "SearchResults": [
    {
      "SheetName": "Foglio1",
      "CellName": "A1",
      "Text": "Test di esempio"
    }
    // ... altri elementi
  ],
  "TotalCount": 42
}
```

**Codici di Stato della Risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | La richiesta è andata a buon fine e la risposta contiene tutti gli elementi di testo trovati. |
| 400 | Richiesta Non Validata | URL non valido o parametri di richiesta mal formati. |
| 401 | Non Autorizzato | Autenticazione non riuscita o assenza di credenziali. |
| 404 | Non Trovato | File sorgente non accessibile. |
| 413 | Payload Troppo Grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore Interno del Server | Si è verificata un’anomalia nel recupero dei dati del foglio di calcolo. |

## Come Utilizzare la Funzione Cerca Tutti gli Elementi di Testo nel Foglio di Calcolo con gli SDK

### Specifica della Funzione Cerca Tutti gli Elementi di Testo nel Foglio di Calcolo

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}" rel="noopener noreferrer">Specifica dell'API Cerca Tutti gli Elementi di Testo nel Foglio di Calcolo</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=en-US&password=myPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "SearchResults": [
    {
      "SheetName": "Foglio1",
      "CellName": "A1",
      "Text": "Test di esempio"
    }
    // ... altri elementi
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

Utilizzare un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose Cells Cloud utilizzando vari SDK:
 `[DA DEFINIRE]`
---