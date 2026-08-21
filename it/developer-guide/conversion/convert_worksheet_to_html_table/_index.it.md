---
title: "Convertire Foglio di Lavoro in Tabella HTML"
ArticleTitle: "Convertire Foglio di Lavoro in Tabella HTML – Aspose.Cells Cloud API"
second_title: "Documenti"
linktype: "ConvertWorksheetToHtmlTable"
type: docs
url: /cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, ConvertWorksheetToHtmlTable, Tabella HTML, API"
description: "Converte un foglio di lavoro di un file foglio elettronico presente nel filesystem locale in un file tabella HTML utilizzando Aspose.Cells Cloud."
weight: 100
---

## Il Converti Foglio di Lavoro in Tabella HTML dei Servizi Web Aspose.Cells Cloud

Questa operazione legge un file foglio elettronico dal filesystem locale, converte il foglio di lavoro specificato in una tabella HTML e restituisce il risultato della conversione come flusso binario. La conversione viene eseguita interamente sul server cloud, pertanto non è necessario caricare preventivamente il file nello storage cloud. Supporta impostazioni locali opzionali e cartelle di lavoro protette da password.

### Endpoint dell’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro | Tipo   | Percorso/Query String/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| Spreadsheet    | File   | FormData                         | Carica il file foglio elettronico. |
| worksheet      | String | Query                            | Nome del foglio di lavoro all'interno del foglio elettronico. (obbligatorio) |
| region         | String | Query                            | Impostazione di regione/lingua del foglio elettronico (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password       | String | Query                            | La password per aprire il file foglio elettronico. |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| *None*         | *None* | *Nessun corpo JSON richiesto; il file viene inviato come multipart/form-data.* |

### **Risposta**

```json
{
  "File": "flusso binario della tabella HTML generata"
}
```

**Codici di Stato della Risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Foglio di lavoro convertito correttamente in tabella HTML e restituito come flusso di file. |
| 400 | Richiesta Non Valida | URL della richiesta non valido o parametri obbligatori mancanti. |
| 401 | Non Autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non Trovato | File sorgente non accessibile. |
| 500 | Errore Interno del Server | Il foglio elettronico ha riscontrato un'anomalia durante l'elaborazione dei dati per la conversione. |
| 413 | Payload Troppo Grande | Il file caricato supera il limite di dimensione consentito. |

## Come Utilizzare il Converti Foglio di Lavoro in Tabella HTML con gli SDK

### Specifica del Converti Foglio di Lavoro in Tabella HTML

La [Specifiche dell'API Converti Foglio di Lavoro in Tabella HTML](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "flusso binario della tabella HTML generata"
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells Cloud utilizzando diversi SDK:
`[TBD]`
---