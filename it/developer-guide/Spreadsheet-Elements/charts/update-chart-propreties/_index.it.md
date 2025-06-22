---
title: Aggiorna proprietà grafico
type: docs
url: /it/charts/propreties/update/
aliases: [/update-chart-propreties/]
weight: 160
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Aggiorna proprietà grafico
---
Questo REST API indica le proprietà del grafico di aggiornamento
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero||
| Nome del foglio| corda| sentiero||
| graficoIndice| intero| sentiero||
| grafico|| corpo||
| cartella| corda| domanda||
| Nome di archiviazione| corda| domanda| nome di archiviazione.|

<br/>
 
 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.
 
È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" 
-d '{"Type": "line"}'
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
    "Code":200,
    
    "Status":"OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK
 
 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.
 
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}
