---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Ottenere le celle unite in un foglio di calcolo – Aspose.Cells Cloud API"
second_title: "Document"
linktype: "docs"
url: /cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, celle unite, foglio di calcolo, API"
description: "Ottenere tutte le aree di celle unite da un foglio di calcolo locale."
weight: 1000
---

## Il servizio web Aspose.Cells Cloud per ottenere le celle unite in un foglio di calcolo

Ottenere tutte le aree di celle unite da un foglio di calcolo locale.

### Endpoint dell’API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l’autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|------|----------------------------------|-------------|
| Spreadsheet | File | FormData | Carica il file del foglio di calcolo. |
| worksheet | String | Query | Nome del foglio di calcolo. |
| region | String | Query | Impostazione regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l’analisi delle date e il comportamento specifico della localizzazione. |
| password | String | Query | La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| N/A | N/A | Questa operazione non accetta un corpo JSON; il file del foglio di calcolo viene inviato tramite `multipart/form-data`. |

### **Risposta**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Aree di celle unite recuperate con successo. |
| 400 | Richiesta non valida | Uno o più parametri della richiesta non sono validi o mancanti. |
| 401 | Non autorizzato | Autenticazione non riuscita – token JWT non valido o mancante. |
| 413 | Payload troppo grande | Il foglio di calcolo caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificato un errore imprevisto sul server. |

## Come utilizzare l’operazione Get Merged Cells In Worksheet con gli SDK

### Specifica di Get Merged Cells In Worksheet

La [specifica dell’API Get Merged Cells In Worksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) definisce un’interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Sheet1&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Utilizzare gli SDK di Aspose Cells Cloud

L’utilizzo di un SDK è il modo più rapido per accelerare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
 `[TBD]`
---