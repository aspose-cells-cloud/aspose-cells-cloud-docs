---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Ottenere le celle unite in un foglio di lavoro remoto – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Ottenere le celle unite in un foglio di lavoro remoto"
type: docs
url: /it/cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, ottenere celle unite, foglio di lavoro remoto, API"
description: "Recupera tutte le aree di celle unite da un foglio di lavoro remoto in un foglio di calcolo."
weight: 10
---

## GetMergedCellsInRemotedWorksheet dei servizi web Aspose.Cells Cloud

Recupera tutte le aree di celle unite da un foglio di lavoro di un foglio di calcolo remoto.

### Endpoint dell'API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Percorso/QueryString/Corpo HTTP | Descrizione |
|----------------|--------|----------------------------------|-------------|
| name | string | Percorso | Nome del foglio di calcolo |
| worksheet | string | Percorso | Nome del foglio di lavoro |
| folder | string | Query | Percorso nello storage cloud del foglio di calcolo |
| storageName | string | Query | (Opzionale) Nome dello storage se si utilizza uno storage cloud personalizzato. Viene utilizzato lo storage predefinito se omesso |
| region | string | Query | Impostazioni regionali/linguistiche del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influiscono sulla formattazione dei numeri, sull'analisi delle date e sul comportamento specifico della localizzazione |
| password | string | Query | Password per aprire il file del foglio di calcolo |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione |
| -------------- | ---- | ----------- |
| — | — | *Nessuno* |

### **Risposta**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Codici di stato della risposta**

| Codice | Significato | Descrizione |
|--------|-------------|-------------|
| 200 | OK | La richiesta è andata a buon fine e l'elenco delle aree di celle unite viene restituito |
| 400 | Richiesta non valida | URL non valido o parametri di richiesta mal formati |
| 401 | Non autorizzato | Autenticazione non riuscita o credenziali non fornite |
| 413 | Payload troppo grande | La dimensione del payload della richiesta supera il limite consentito |
| 500 | Errore interno del server | Si è verificata un'anomalia nel recupero dei dati dal foglio di calcolo |

## Come utilizzare GetMergedCellsInRemotedWorksheet con gli SDK

### Specifica di GetMergedCellsInRemotedWorksheet

La [specifica dell'API GetMergedCellsInRemotedWorksheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire direttamente interazioni REST da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizzare HTTPS per una connessione sicura
curl -v "https://api.aspose.cloud/v4.0/cells/Sample.xlsx/worksheets/Sheet1/mergedcells?folder=MyFolder&storageName=MyStorage&region=en-US&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose Cells Cloud

L'utilizzo di un SDK è il modo più rapido per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come chiamare i servizi web di Aspose Cells Cloud utilizzando vari SDK:
`[TBD]`