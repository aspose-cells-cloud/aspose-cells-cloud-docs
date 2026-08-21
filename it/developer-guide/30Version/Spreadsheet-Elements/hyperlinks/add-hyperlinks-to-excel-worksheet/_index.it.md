---
title: "Aggiungi collegamento ipertestuale a un foglio di lavoro"
type: docs
url: /it/hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, aggiungi collegamento ipertestuale, Excel REST API, cloud SDK"
description: "Scopri come aggiungere un collegamento ipertestuale a un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud v3.0. Include l'endpoint, una guida completa ai parametri, un esempio cURL e frammenti di codice SDK per C#, Java, Python e altri linguaggi."
weight: 20
---

Questa API REST aggiunge un collegamento ipertestuale a un foglio di lavoro Excel.

## API REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                                                     |
| -------------- | ------- | --------- | ----------------------------------------------------------------------------------------------- |
| name           | string  | path      | Nome del documento.                                                                             |
| sheetName      | string  | path      | Nome del foglio di lavoro.                                                                      |
| firstRow       | integer | query     | Indice in base zero della prima riga dell'intervallo a cui verrà applicato il collegamento.     |
| firstColumn    | integer | query     | Indice in base zero della prima colonna dell'intervallo a cui verrà applicato il collegamento.  |
| totalRows      | integer | query     | Numero di righe interessate dall'intervallo del collegamento.                                   |
| totalColumns   | integer | query     | Numero di colonne interessate dall'intervallo del collegamento.                                 |
| address        | string  | query     | L'URL di destinazione a cui punta il collegamento ipertestuale (codificato in URL).             |
| folder         | string  | query     | Cartella del documento.                                                                         |
| storageName    | string  | query     | Nome dell'archiviazione.                                                                        |

La richiesta può anche includere un corpo JSON contenente gli stessi campi (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Fornire il corpo è utile quando si preferisce un payload rispetto ai parametri nella stringa di query.

### Risposte di errore

| Codice HTTP | Motivo                                                    | Esempio di corpo                                                   |
| ----------- | --------------------------------------------------------- | ------------------------------------------------------------------ |
| **400**     | Richiesta non valida – parametri mancanti o non validi.   | `{ "Code":"400", "Message":"Valore del parametro non valido." }`  |
| **401**     | Non autorizzato – token JWT mancante o non valido.        | `{ "Code":"401", "Message":"Token di accesso mancante o non valido." }` |
| **404**     | Non trovato – cartella di lavoro o foglio di lavoro non esistenti. | `{ "Code":"404", "Message":"File non trovato." }`                 |
| **500**     | Errore interno del server – errore imprevisto nel server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

Se la richiesta fallisce, l'API restituisce i codici di errore HTTP standard (ad esempio, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error) insieme a un payload JSON contenente un messaggio di errore e il codice.

## Famiglia di SDK Cloud

Utilizzare un SDK rappresenta il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}