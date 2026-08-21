---
title: "Protezione in Batch di File Excel"
second_title: "Documenti"
type: docs
url: /batch/protect
keywords: "Protezione in batch di file Excel, Aspose Cells Cloud, API REST, protezione Excel, protezione in batch"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per proteggere in batch più file Excel. Include i dettagli della richiesta, un esempio cURL e campioni di codice SDK per vari linguaggi."
weight: 100
---

Questa API REST consente la **protezione in batch** di file Excel idonei.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro        | Tipo                | Posizione | Descrizione                                                                                              |
|-----------------------|---------------------|-----------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body      | Payload JSON che specifica la cartella di origine, le condizioni di selezione, il tipo di protezione, la password e la cartella di output. |

### Proprietà di BatchProtectRequest

| Nome              | Tipo                     | Descrizione                                                                                 | Note |
|-------------------|--------------------------|---------------------------------------------------------------------------------------------|------|
| SourceFolder      | string                   | Cartella contenente i file Excel di origine.                                                | opzionale |
| MatchCondition    | MatchConditionRequest    | Criteri utilizzati per selezionare i file da proteggere.                                    | opzionale |
| ProtectionType    | string                   | Tipo di protezione da applicare (ad es. `All`, `ReadOnly`).                                 | opzionale |
| Password          | string                   | Password da impostare per i file protetti.                                                  | opzionale |
| OutFolder         | string                   | Cartella di destinazione per i file protetti.                                               | opzionale |

### Proprietà di MatchConditionRequest

| Nome                | Tipo       | Descrizione                                   | Note |
|---------------------|------------|-----------------------------------------------|------|
| RegexPattern        | string     | Espressione regolare utilizzata per confrontare i nomi dei file. | opzionale |
| FullMatchConditions | string[]   | Elenco di condizioni esatte per i nomi dei file. | opzionale |

### Parametro del corpo della richiesta

| Nome parametro | Tipo | Descrizione                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Contenuto binario del file del foglio di calcolo da creare. |

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

| Codice | Significato                 | Quando viene restituito                 |
|--------|-----------------------------|-----------------------------------------|
| 200 OK | Foglio di calcolo creato correttamente | Flusso normale                          |
| 201 Created | Foglio di calcolo creato (risposta alternativa) | Quando l’API restituisce lo stato "created" |
| 400 Bad Request | Parametri non validi | Errore lato client                      |
| 401 Unauthorized | Token mancante o non valido | Errore di autenticazione               |
| 409 Conflict | Il file esiste e `isWriteOver=false` | Conflitto con un file esistente        |

## Come utilizzare l’API PostProtectConvert con gli SDK

### Specifica dell’API PostProtectConvert

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/PostProtectConvert) definisce un’interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare una chiamata all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}