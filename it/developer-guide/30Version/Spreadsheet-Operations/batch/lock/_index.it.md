---
title: "Blocco in Batch di File Excel"
second_title: "Documento"
type: docs
url: /batch/lock
keywords: "blocco in batch, Excel, Aspose.Cells, API Cloud, foglio di calcolo, protezione file"
description: "L'API Cloud Aspose.Cells consente il blocco in batch di più file Excel. Utilizza l'endpoint REST o uno dei SDK supportati (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, ecc.) per bloccare i file in blocco."
weight: 100
---

Questa API REST consente il **blocco in batch** dei file Excel idonei.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Sicurezza e Autenticazione**

Le API Cloud di Aspose.Cells sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.


### Parametri della Richiesta

| Nome Parametro   | Tipo               | Posizione | Descrizione                                   |
|------------------|--------------------|-----------|-----------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body      | Corpo JSON contenente i parametri di blocco. |

#### **Proprietà di BatchLockRequest**

| Nome            | Tipo                     | Descrizione                                           | Note     |
|-----------------|--------------------------|-------------------------------------------------------|----------|
| SourceFolder    | string                   | Cartella contenente i file Excel sorgente.            | opzionale |
| MatchCondition  | MatchConditionRequest    | Condizioni utilizzate per selezionare i file da bloccare. | opzionale |
| Password        | string                   | Password da applicare ai file bloccati.              | opzionale |
| OutFolder       | string                   | Cartella di destinazione per i file bloccati.        | opzionale |

#### **Proprietà di MatchConditionRequest**

| Nome               | Tipo      | Descrizione                                          | Note     |
|--------------------|-----------|------------------------------------------------------|----------|
| RegexPattern       | string    | Pattern di espressione regolare per abbinare i nomi dei file. | opzionale |
| FullMatchConditions| string[]  | Abbinamenti esatti dei nomi dei file per il blocco. | opzionale |

### Parametro del Corpo della Richiesta

| Nome Parametro | Tipo | Descrizione                                    |
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

**Codici di Stato HTTP**

| Codice | Significato                 | Quando Restituito                       |
|--------|-----------------------------|-----------------------------------------|
| 200 OK | Foglio di calcolo creato correttamente | Flusso normale                          |
| 201 Created | Foglio di calcolo creato (risposta alternativa) | Quando l'API restituisce lo stato "created" |
| 400 Bad Request | Parametri non validi | Errore lato client                      |
| 401 Unauthorized | Token mancante o non valido | Errore di autenticazione                |
| 409 Conflict | Il file esiste e `isWriteOver=false` | Conflitto con il file esistente         |

## Come Utilizzare l'API PostBatchLock con gli SDK

### Specifica dell'API PostBatchLock

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

L'utilizzo di un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività di blocco. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}