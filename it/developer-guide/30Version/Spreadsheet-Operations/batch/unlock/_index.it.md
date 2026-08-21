---
title: "Sblocco in Batch"
second: "Documento"
type: docs
url: /it/batch/unlock
keywords: "sblocco in batch, Aspose.Cells Cloud, Excel, API REST, foglio di calcolo, SDK cloud"
description: "Sblocca più file Excel in batch utilizzando l'API REST di Aspose.Cells Cloud. Supporta SDK per C#, Java, Python e altri linguaggi."
weight: 100
---

Questa API REST sblocca in batch i file Excel idonei.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome Parametro | Tipo | Posizione | Descrizione |
|----------------|------|-----------|-------------|
| **BatchLockRequest** |  | body | Corpo della richiesta contenente le impostazioni di sblocco. |

### Proprietà di **BatchLockRequest**

| Nome                | Tipo                     | Descrizione                                         | Note         |
|---------------------|--------------------------|-----------------------------------------------------|--------------|
| SourceFolder        | string                   | Cartella contenente i file Excel di origine.       | [opzionale]  |
| MatchCondition      | MatchConditionRequest    | Criteri utilizzati per selezionare i file da sbloccare. | [opzionale]  |
| Password            | string                   | Password applicata ai workbook protetti.           | [opzionale]  |
| OutFolder           | string                   | Cartella di destinazione per i file sbloccati.      | [opzionale]  |

### Proprietà di **MatchConditionRequest**

| Nome               | Tipo      | Descrizione                                 | Note         |
|--------------------|-----------|---------------------------------------------|--------------|
| RegexPattern       | string    | Espressione regolare per abbinare i nomi dei file. | [opzionale]  |
| FullMatchConditions| string[]  | Condizioni esatte di nome file da abbinare. | [opzionale]  |

### Parametro del corpo della richiesta

| Nome Parametro | Tipo | Descrizione                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Contenuto binario del file workbook da creare. |

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

| Codice | Significato                     | Quando restituito                          |
|--------|---------------------------------|--------------------------------------------|
| 200 OK | Workbook creato con successo    | Flusso normale                             |
| 201 Created | Workbook creato (risposta alternativa) | Quando l'API restituisce lo stato "created" |
| 400 Bad Request | Parametri non validi | Errore lato client                         |
| 401 Unauthorized | Token mancante o non valido | Errore di autenticazione                   |
| 409 Conflict | File esistente e `isWriteOver=false` | Conflitto con file esistente              |

## Come utilizzare l'API PostBatchLock con gli SDK

### Specifica dell'API PostBatchLock

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) definiscono un'interfaccia di programmazione accessibile pubblicamente e permettono di effettuare direttamente interazioni REST da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

L'utilizzo di un SDK è il modo più rapido per sviluppare funzionalità di sblocco. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}