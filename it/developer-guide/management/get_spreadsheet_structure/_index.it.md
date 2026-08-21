---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /it/cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, Struttura foglio di calcolo, API"
description: "Converte strutturalmente i metadati principali, i fogli di lavoro, le tabelle, le tabelle pivot, i grafici, le forme e altre informazioni di un libro Excel in un oggetto JSON di tipo JObject."
weight: 1000
---

## GetSpreadsheetStructure dei servizi web Aspose.Cells Cloud

Converte strutturalmente i metadati principali, i fogli di lavoro, le tabelle, le tabelle pivot, i grafici, le forme e altre informazioni di un libro Excel in un oggetto JSON di tipo JObject, per scenari come l'esportazione di dati, le risposte API e la registrazione dei log.

### Endpoint API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| Spreadsheet    | File   | FormData (corpo)                 | Carica il file del foglio di calcolo. |
| region         | String | Query                            | Impostazione della regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password       | String | Query                            | La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| Spreadsheet    | File | Carica il file del foglio di calcolo. |

### **Risposta**

```json
{
  "Worksheets": [
    {
      "Name": "Foglio1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Struttura del foglio di calcolo recuperata correttamente. |
| 400 | Richiesta non valida | Parametri della richiesta non validi o formato del file non supportato. |
| 401 | Non autorizzato | Autenticazione non riuscita o token JWT mancante. |
| 413 | Payload troppo grande | Il file caricato supera il limite di dimensione consentito. |
| 500 | Errore interno del server | Si è verificato un errore imprevisto sul server. |

## Come utilizzare GetSpreadsheetStructure con gli SDK

### Specifica di GetSpreadsheetStructure

La [specificazione dell'API GetSpreadsheetStructure](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose Cells Cloud. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=en-US&password=yourPassword" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Foglio1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`
---