---
title: "Split in Batch"
second: "Document"
type: docs
url: /it/batch/split
keywords: "Split in Batch, Aspose.Cells Cloud, REST API, Excel, PDF, CSV, JSON, Foglio di calcolo, SDK Cloud"
description: "Documentazione per l'API Aspose.Cells Cloud Batch Split, che consente di dividere file di fogli di calcolo in vari formati come PDF, CSV o JSON. Include i dettagli della richiesta, esempi di comandi cURL e l'utilizzo dell'SDK in diversi linguaggi di programmazione."
weight: 100
---

Questa API REST esegue una **split in batch** dei file idonei.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro   | Tipo               | Percorso/Query/Stringa/Corpo HTTP | Descrizione                                   |
|------------------|--------------------|-----------------------------------|-----------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                              | Payload della richiesta contenente le opzioni di suddivisione. |

### Proprietà di **BatchSplitRequest**

| Nome            | Tipo                | Descrizione                                     | Note       |
|-----------------|---------------------|-------------------------------------------------|------------|
| SourceFolder    | string              | Cartella contenente il file sorgente.          | [opzionale] |
| SourceStorage   | string              | Nome dello storage in cui risiede il file sorgente. | [opzionale] |
| MatchCondition  | MatchConditionRequest| Condizioni utilizzate per selezionare i file da dividere. | [opzionale] |
| Format          | string              | Format di output desiderato (es. pdf, csv).    | [opzionale] |
| FromIndex       | integer             | Indice iniziale delle pagine da dividere.      | [opzionale] |
| ToIndex         | integer             | Indice finale delle pagine da dividere.        | [opzionale] |
| OutFolder       | string              | Cartella di destinazione per i file suddivisi. | [opzionale] |
| SaveOptions     | SaveOptions         | Opzioni aggiuntive per il salvataggio dell'output. | [opzionale] |

### Proprietà di **MatchConditionRequest**

| Nome                 | Tipo       | Descrizione                                   | Note       |
|----------------------|------------|-----------------------------------------------|------------|
| RegexPattern         | string     | Espressione regolare per il matching dei nomi dei file. | [opzionale] |
| FullMatchConditions  | string[]   | Elenco di condizioni di match esatti.         | [opzionale] |

### Parametro nel corpo della richiesta

| Nome parametro | Tipo | Descrizione                                     |
| -------------- | ---- | ----------------------------------------------- |
| data           | file | Contenuto binario del file del workbook da creare. |

### **Risposta**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Codici di stato HTTP**

| Codice | Significato                     | Quando restituito                           |
|--------|---------------------------------|---------------------------------------------|
| 200 OK | Workbook creato correttamente   | Flusso normale                              |
| 201 Created | Workbook creato (risposta alternativa) | Quando l'API restituisce lo stato "created" |
| 400 Bad Request | Parametri non validi | Errore lato client                          |
| 401 Unauthorized | Token mancante o non valido | Errore di autenticazione                   |
| 409 Conflict | File esistente e `isWriteOver=false` | Conflitto con file esistente              |


## Come utilizzare l'API PostBatchSplit con gli SDK

### Specifica dell'API PostBatchSplit

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) definiscono un'interfaccia di programmazione pubblicamente accessibile e permettono di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

Utilizzare un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle tue attività di suddivisione. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}