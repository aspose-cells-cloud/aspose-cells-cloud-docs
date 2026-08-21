---
title: "Conversione in Batch di File Excel"
second_title: "Documento"
type: docs
url: /it/batch/convert
keywords: "conversione in batch, Excel, Aspose.Cells Cloud, API REST, PDF, CSV, JSON, Markdown, foglio di calcolo"
description: "Scopri come utilizzare l'API Aspose.Cells Cloud per convertire in batch più file Excel in formati come PDF, CSV, JSON o Markdown. Questa guida include i dettagli dell'endpoint REST, i parametri della richiesta, un esempio cURL e frammenti di codice SDK per vari linguaggi."
weight: 100
---

Questa API REST consente la **conversione in batch** di file idonei.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome del parametro     | Tipo   | Posizione | Descrizione                                           |
|------------------------|--------|-----------|-------------------------------------------------------|
| **batchConvertRequest** | oggetto | body      | Corpo della richiesta contenente le impostazioni di conversione.         |

#### Proprietà di BatchConvertRequest

| Nome               | Tipo                | Descrizione                                           | Note |
|--------------------|---------------------|-------------------------------------------------------|------|
| **SourceFolder**   | stringa             | Percorso della cartella contenente i file Excel sorgente. | [opzionale] |
| **MatchCondition** | MatchConditionRequest | Condizioni utilizzate per selezionare i file da convertire. | [opzionale] |
| **Format**         | stringa             | Format di destinazione per la conversione (es. `pdf`, `csv`). | [opzionale] |
| **OutFolder**      | stringa             | Cartella di destinazione in cui verranno salvati i file convertiti. | [opzionale] |
| **SaveOptions**    | SaveOptions         | Opzioni aggiuntive che controllano il salvataggio dei file. | [opzionale] |

#### Proprietà di MatchConditionRequest

| Nome                    | Tipo       | Descrizione                                          | Note |
|-------------------------|------------|------------------------------------------------------|------|
| **RegexPattern**        | stringa    | Espressione regolare utilizzata per filtrare i nomi dei file. | [opzionale] |
| **FullMatchConditions** | string[]   | Elenco di condizioni esatte sui nomi dei file per il matching. | [opzionale] |


### Parametro del corpo della richiesta

| Nome del parametro | Tipo | Descrizione                                    |
|--------------------|------|------------------------------------------------|
| data               | file | Contenuto binario del file del workbook da creare. |
  
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

| Codice | Significato                     | Quando viene restituito                           |
|--------|---------------------------------|--------------------------------------------------|
| 200 OK | Workbook creato correttamente   | Flusso normale                                   |
| 201 Created | Workbook creato (risposta alternativa) | Quando l’API restituisce lo stato “created” |
| 400 Bad Request | Parametri non validi | Errore lato client                        |
| 401 Unauthorized | Token mancante o non valido | Errore di autenticazione                    |
| 409 Conflict | File esistente e `isWriteOver=false` | Conflitto con file esistente    

## Come utilizzare l'API PostBatchConvert con gli SDK

### Specifica dell'API PostBatchConvert

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/PostBatchConvert) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}