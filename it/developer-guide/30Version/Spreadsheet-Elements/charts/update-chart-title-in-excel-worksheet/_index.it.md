---
title: "Aggiorna il titolo del grafico in un foglio di lavoro Excel"
type: docs
url: /it/charts/title/update/
aliases: [  /it/update-chart-title-in-excel-worksheet/ ]
weight: 160
keywords: Excel, Aspose.Cells, REST API, Titolo grafico, Aggiornamento, Cloud SDK
description: Scopri come aggiornare il titolo di un grafico in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud, cURL e vari SDK.
ArticleTitle: "Aggiorna il titolo del grafico in un foglio di lavoro Excel – Documentazione Aspose.Cells Cloud"
---

Questa API REST aggiorna il titolo del grafico.

**Prerequisiti:** È necessario disporre di un account Aspose Cloud valido e di un token JWT per l'autenticazione. I passaggi tipici includono:

- Registrarsi per un account Aspose Cloud.  
- Generare un token JWT tramite l'endpoint di autenticazione.  
- Assicurarsi che il foglio di lavoro di destinazione sia memorizzato in uno storage cloud supportato (predefinito o personalizzato).

## API PostWorksheetChartTitle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

Tutte le chiamate API devono essere effettuate tramite **HTTPS** per evitare avvisi relativi a contenuti misti.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                              |
| -------------- | ------- | --------- | ---------------------------------------- |
| name           | string  | path      | Nome del foglio di lavoro.               |
| sheetName      | string  | path      | Nome del foglio di lavoro.               |
| chartIndex     | integer | path      | Indice in base zero del grafico.         |
| title          | string  | body      | Nuovo titolo del grafico.                |
| folder         | string  | query     | Cartella contenente il foglio di lavoro. |
| storageName    | string  | query     | Nome dello storage.                      |

### Codici di stato della risposta

| Codice | Descrizione                                          |
| ------ | ---------------------------------------------------- |
| 200    | OK – Il titolo del grafico è stato aggiornato correttamente. |
| 400    | Richiesta non valida – Parametri mancanti o non validi. |
| 401    | Non autorizzato – Token JWT non valido o mancante.   |
| 404    | Non trovato – Foglio di lavoro, foglio di lavoro o grafico non trovato. |
| 500    | Errore interno del server – Condizione imprevista nel server. |

**Nota:** L'indice `chartIndex` è in base zero; il primo grafico in un foglio di lavoro viene fatto riferimento con `0`.

La <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Borsa valori"}' \
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

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}
---