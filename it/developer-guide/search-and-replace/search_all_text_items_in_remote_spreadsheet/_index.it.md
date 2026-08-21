---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/{name}/search/content/all-textitems
aliases: []
keywords: "ricerca, elementi di testo, Aspose.Cells"
description: "Cerca tutti gli elementi di testo in un foglio di calcolo remoto utilizzando Aspose.Cells Cloud."
weight: 100
---

## Il metodo SearchAllTextItemsInRemoteSpreadsheet dei Web Service Aspose.Cells Cloud

Questo metodo consente di cercare tutti gli elementi di testo all'interno di un file di foglio di calcolo remoto. Supporta la ricerca in tutti i fogli e le celle del workbook, identificando le occorrenze del termine cercato. L'operazione viene eseguita nel cloud, senza richiedere archiviazione locale. Assicurati di disporre delle autorizzazioni necessarie per leggere il file di origine. Se il file di origine non è accessibile o si verifica un errore durante il processo di ricerca (ad esempio, un formato di file non supportato), verrà generata un'eccezione appropriata. Il metodo può restituire le posizioni delle corrispondenze (ad esempio, nome del foglio, coordinate della cella), a seconda dei dettagli dell'implementazione.

### Endpoint dell'API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/Query String/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| name           | string | Percorso                         | Nome del file del workbook. |
| folder         | string | Query                            | Percorso della cartella in cui è archiviato il workbook. |
| storageName    | string | Query                            | (Opzionale) Nome dello storage se si utilizza uno storage cloud personalizzato. Utilizza lo storage predefinito se omesso. |
| region         | string | Query                            | Impostazione di area lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della localizzazione. |
| password       | string | Query                            | Password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [TBD]          |      | [TBD] |

### **Risposta**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | La richiesta è andata a buon fine e la risposta contiene tutti gli elementi di testo trovati nel foglio di calcolo. |
| 400 | Richiesta non valida | URL o parametri della richiesta non validi. |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite. |
| 404 | Non trovato | File di origine non accessibile. |
| 413 | Payload troppo grande | Il payload della richiesta supera la dimensione consentita. |
| 500 | Errore interno del server | Il foglio di calcolo ha riscontrato un'anomalia durante l'acquisizione dei dati. |

## Come utilizzare SearchAllTextItemsInRemoteSpreadsheet con gli SDK

### Specifica di SearchAllTextItemsInRemoteSpreadsheet

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet" rel="noopener noreferrer">specifica dell'API SearchAllTextItemsInRemoteSpreadsheet</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}

{< tab tabNum="1" >}

```bash
# Utilizza HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Foglio1",
      "CellAddress": "A1",
      "Text": "Test di esempio"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`
---