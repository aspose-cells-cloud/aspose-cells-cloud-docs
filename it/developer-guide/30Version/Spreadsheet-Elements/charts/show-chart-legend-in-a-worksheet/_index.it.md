---
title: "Mostra la legenda del grafico in un foglio di lavoro"
type: docs
url: /charts/legend/show/
aliases: [/show-chart-legend-in-a-worksheet/]
weight: 100
keywords: "Aspose.Cells Cloud, API per la legenda del grafico, legenda grafico Excel, REST PUT per la legenda del grafico, Aspose API v3.0"
description: "Scopri come visualizzare la legenda di un grafico in un foglio di lavoro di un file Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include dettagli sull'endpoint, i parametri, un esempio cURL e frammenti di codice per vari SDK."
---

Questa API REST consente di visualizzare la **legenda**—il riquadro esplicativo che identifica le serie di dati—in un grafico posizionato all'interno di un foglio di lavoro di un file Excel.

## API REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                      |
| -------------- | ------- | --------- | ------------------------------------------------ |
| name           | stringa | path      | Nome del file del workbook.                      |
| sheetName      | stringa | path      | Nome del foglio di lavoro contenente il grafico. |
| chartIndex     | intero  | path      | Indice in base zero del grafico.                 |
| folder         | stringa | query     | Cartella contenente il workbook.                 |
| storageName    | stringa | query     | Nome del servizio di archiviazione.              |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare direttamente interazioni REST da un browser web.

L'autenticazione avviene tramite un token Bearer JWT fornito nell'intestazione **Authorization**.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare la chiamata con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
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

L'API può restituire i seguenti codici di stato HTTP:

- **200 OK** – La legenda è stata visualizzata correttamente.
- **400 Bad Request** – Parametri non validi.
- **401 Unauthorized** – Autenticazione non riuscita.
- **404 Not Found** – Il workbook, il foglio di lavoro o il grafico specificato non esiste.
- **500 Internal Server Error** – Si è verificato un errore imprevisto sul server.

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK per il Cloud

Utilizzare un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}

---