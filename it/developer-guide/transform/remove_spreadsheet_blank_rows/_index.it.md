---
title: "Rimuovi righe vuote dai fogli di calcolo"
ArticleTitle: "Rimuovi righe vuote dai fogli di calcolo – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Rimuovi righe vuote dai fogli di calcolo"
type: docs
url: /it/cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, rimuovi righe vuote, foglio di calcolo, API"
description: "Elimina tutte le righe vuote da un file di foglio di calcolo."
weight: 100
---

## La rimozione delle righe vuote dai fogli di calcolo dei servizi web Aspose.Cells Cloud

Questo metodo rimuove dal foglio di calcolo le righe completamente vuote, prive di dati o oggetti. Esso analizza tutti i fogli e identifica le righe in cui ogni cella è vuota. L'operazione viene eseguita direttamente sul foglio di calcolo, garantendo che vengano eliminate solo le righe prive di contenuto. Questo aiuta a pulire il foglio di calcolo e rimuovere righe vuote non necessarie, rendendo i dati più organizzati e facili da gestire. Gli utenti dovrebbero assicurarsi che il foglio di calcolo sia backuppato prima di eseguire questa operazione, poiché le righe eliminate non possono essere recuperate.

### Endpoint Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| Spreadsheet    | File   | FormData                         | Carica il file del foglio di calcolo. |
| outPath        | String | Query                            | (Opzionale) Il percorso della cartella in cui è memorizzato il foglio di lavoro. Il valore predefinito è null. |
| outStorageName | String | Query                            | Nome dello Storage per il file di output. |
| region         | String | Query                            | Impostazione regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influisce sulla formattazione dei numeri, sull'analisi delle date e sul comportamento specifico della localizzazione. |
| password       | String | Query                            | La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Carica il file del foglio di calcolo. |

### **Risposta**

```json
{
  "ResponseFile": "flusso di file binario"
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Il file del foglio di calcolo elaborato, con le righe vuote rimosse, viene restituito. |
| 400 | Richiesta non valida | URL o parametri della richiesta non validi. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | File sorgente non accessibile. |
| 413 | Payload troppo grande | Il payload della richiesta supera la dimensione consentita. |
| 500 | Errore interno del server | Il foglio di calcolo ha riscontrato un'anomalia durante il recupero dei dati. |

## Come utilizzare la rimozione delle righe vuote dai fogli di calcolo con gli SDK

### Specifica della rimozione delle righe vuote dai fogli di calcolo

La [specifica dell'API Rimuovi righe vuote dai fogli di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}
{< tab tabNum="1" >}
```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "flusso di file binario"
}
```
{< /tab >}
{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[DA COMPLETARE]`
---