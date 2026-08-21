---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Get Structure In Remote Spreadsheet – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "GetStructureInRemoteSpreadsheet"
type: docs
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, foglio di calcolo, struttura"
description: "Recupera i metadati strutturali di un file Excel remoto, inclusi fogli di lavoro, tabelle, tabelle pivot, grafici, forme e altre informazioni essenziali."
weight: 100
---

## La funzionalità Get Structure In Remote Spreadsheet dei servizi web Aspose.Cells Cloud

Converte strutturalmente i metadati principali, i fogli di lavoro, le tabelle, le tabelle pivot, i grafici, le forme e altre informazioni di un file Excel in un oggetto JSON di tipo JObject, per scenari come l'esportazione di dati, le risposte API e la registrazione dei log.

### Endpoint dell'API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo | Percorso/Query string/Corpo HTTP | Descrizione |
|----------------|------|----------------------------------|-------------|
| name | string | Percorso | Nome del file del foglio di calcolo. |
| folder | string | Query | Cartella in cui si trova il file. (Facoltativo) |
| storageName | string | Query | (Facoltativo) Nome dell'archiviazione se si utilizza un'archiviazione cloud personalizzata. Se omesso, viene utilizzata l'archiviazione predefinita. |
| region | string | Query | Impostazione regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influisce sulla formattazione dei numeri, sull'analisi delle date e sul comportamento specifico della località. |
| password | string | Query | La password per aprire il file del foglio di calcolo. |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

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
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | Struttura del file di lavoro recuperata con successo. |
| 400 | Richiesta non valida | Parametri della richiesta non validi. |
| 401 | Non autorizzato | Autenticazione non riuscita o token mancante. |
| 413 | Payload troppo grande | Il payload della richiesta supera la dimensione consentita. |
| 500 | Errore interno del server | Errore imprevisto sul server. |

## Come utilizzare Get Structure In Remote Spreadsheet con gli SDK

### Specifica di Get Structure In Remote Spreadsheet

La [specifica dell'API Get Structure In Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Vendite trimestrali",
    "Keywords": "sales,report,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`
---