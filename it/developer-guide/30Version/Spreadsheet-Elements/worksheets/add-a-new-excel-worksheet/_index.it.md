---
title: "Aggiungi un foglio di Excel"
ArticleTitle: "Aggiungi un foglio di Excel - Guida all'API di Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Aggiungi"
type: docs
url: /it/worksheets/add/
aliases: [  /it/add-a-new-excel-worksheet/ ]
keywords: "Aggiungi foglio Excel, Aspose.Cells Cloud, API REST, PUT worksheet, cartella di lavoro Excel, richiesta API"
description: "Guida passo-passo per aggiungere un nuovo foglio a una cartella di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud, inclusi dettagli sulla richiesta, un esempio cURL e frammenti di codice SDK per diversi linguaggi."
weight: 20
---

Questa API REST aggiunge un nuovo foglio a una cartella di lavoro esistente.

**Prerequisiti**: Per chiamare questo endpoint è necessario disporre di un token di autenticazione Aspose Cloud valido, la cartella di lavoro target deve essere caricata nell'archivio Aspose Cloud e si deve conoscere il nome dell'archivio (in caso di utilizzo di un archivio personalizzato).

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Parametri della richiesta**

| Nome parametro | Tipo    | Posizione | Descrizione                                          |
| -------------- | ------- | --------- | ---------------------------------------------------- |
| name           | string  | path      | Nome del file della cartella di lavoro.              |
| sheetName      | string  | path      | Nome del nuovo foglio da creare.                     |
| position       | integer | query     | Posizione iniziale in base zero in cui inserire il foglio. |
| sheettype      | string  | query     | Tipo del nuovo foglio (ad esempio, **Chart**, **Dialog**). |
| folder         | string  | query     | Cartella contenente la cartella di lavoro.           |
| storageName    | string  | query     | Nome dell'archivio Aspose Cloud.                     |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codici di stato di risposta possibili**

| Codice di stato | Descrizione                                          |
|----------------|------------------------------------------------------|
| 200            | Foglio aggiunto correttamente.                       |
| 400            | Richiesta non valida – parametri non validi.         |
| 401            | Non autorizzato – token di autenticazione mancante o non valido. |
| 404            | Non trovato – la cartella di lavoro o la cartella non esiste. |
| 500            | Errore interno del server – condizione imprevista.   |

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sul tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}