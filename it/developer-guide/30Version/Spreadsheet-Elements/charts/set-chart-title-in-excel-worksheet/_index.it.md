---
title: "Aspose.Cells Cloud API – Imposta il titolo di un grafico in un foglio Excel"
type: docs
url: /it/chart/title/add/
aliases: [/set-chart-title-in-excel-worksheet/]
weight: 30
keywords: "Aspose.Cells Cloud, API per il titolo del grafico, titolo del grafico Excel, API REST, esempi di SDK"
description: "Scopri come aggiungere o aggiornare il titolo di un grafico in un foglio Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi cURL, esempi di SDK, parametri richiesti, fasi di autenticazione e gestione degli errori."
---

Aggiunge un titolo al grafico o rende visibile un titolo esistente.

## API PutWorksheetChartTitle

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione | Descrizione                              |
| -------------- | ------- | --------- | ---------------------------------------- |
| name           | string  | path      | Nome del workbook.                       |
| sheetName      | string  | path      | Nome del foglio di lavoro.               |
| chartIndex     | integer | path      | Indice del grafico.                      |
| title          | string  | body      | Testo del titolo del grafico.            |
| folder         | string  | query     | Cartella contenente il workbook.         |
| storageName    | string  | query     | Nome dello storage.                      |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Risposte di errore**

| Codice HTTP | Payload di esempio                                                                   | Descrizione                                                  |
| ----------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------------ |
| 400         | `{ "Code": "400", "Message": "Payload della richiesta non valido." }`               | Il corpo della richiesta è malformattato o mancano campi obbligatori. |
| 401         | `{ "Code": "401", "Message": "Autenticazione fallita. Token JWT non valido o scaduto." }` | Il token bearer è mancante, non valido o scaduto.            |
| 404         | `{ "Code": "404", "Message": "Workbook, foglio di lavoro o grafico non trovato." }`   | La risorsa specificata non esiste.                           |
| 500         | `{ "Code": "500", "Message": "Errore interno del server." }`                         | Si è verificato un errore imprevisto sul server.             |

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo più rapido per sviluppare. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}