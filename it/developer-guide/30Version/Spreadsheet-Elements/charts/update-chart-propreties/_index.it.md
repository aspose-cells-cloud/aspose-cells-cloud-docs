---
title: "Aggiorna le proprietà del grafico"
type: docs
url: /it/charts/properties/update/
aliases: [  /it/update-chart-properties/ ]
weight: 160
keywords: "Aspose.Cells, grafico, aggiornamento, Excel, REST API, SDK"
description: "Scopri come aggiornare le proprietà del grafico (tipo, titolo, legenda, ecc.) in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include l'endpoint, i parametri, un esempio cURL e frammenti di codice per SDK in C#, Java, PHP, Ruby, Node.js, Perl e Go."
ArticleTitle: "Aggiorna le proprietà del grafico – Aspose.Cells Cloud REST API"
---

Questa REST API aggiorna le proprietà del grafico.

### **Sicurezza e autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

## API PostWorksheetChart

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Parametri della richiesta

| Nome parametro | Tipo    | Percorso/Query string/Corpo HTTP | Descrizione                                                   |
| -------------- | ------- | -------------------------------- | ------------------------------------------------------------- |
| name           | string  | percorso                         | Nome del file Excel.                                          |
| sheetName      | string  | percorso                         | Nome del foglio di calcolo contenente il grafico.             |
| chartIndex     | integer | percorso                         | Indice in base zero del grafico da aggiornare.                |
| chart          | object  | corpo                            | Oggetto JSON che definisce le proprietà del grafico da modificare. |
| folder         | string  | query                            | Cartella nello storage in cui si trova il file.               |
| storageName    | string  | query                            | Nome del servizio di storage.                                 |

### Schema del corpo della richiesta

L'oggetto **`chart`** contiene le proprietà che è possibile modificare. Di seguito è riportato un esempio rappresentativo in JSON che include diversi campi comunemente utilizzati:

```json
{
  "Title": {
    "Text": "Vendite trimestrali"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Nota:** È necessario fornire solo i campi che si desidera modificare. Le proprietà omesse mantengono i valori precedentemente impostati.

La <a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

## Risposta

L'API restituisce un oggetto JSON che indica il risultato dell'operazione. Un aggiornamento riuscito restituisce:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di stato di successo**

| Stato HTTP | Descrizione |
| ---------- | ----------- |
| 200        | OK – Le proprietà del grafico sono state aggiornate correttamente. |

**Intestazioni della risposta**

| Intestazione      | Descrizione |
| ----------------- | ----------- |
| `Content-Type`    | `application/json` – Indica che il corpo della risposta è in formato JSON. |
| `X-RequestId`     | Identificatore univoco della richiesta (utile per la risoluzione dei problemi). |

Le risposte di errore possibili includono:

| Stato HTTP | Descrizione                                     |
| ---------- | ----------------------------------------------- |
| 400        | Richiesta non valida – parametri o corpo non validi |
| 401        | Non autorizzato – token mancante o non valido   |
| 404        | Non trovato – file, foglio di calcolo o grafico non trovato |
| 500        | Errore interno del server                       |

Per altre operazioni relative ai grafici, consulta gli argomenti correlati come [Aggiorna il titolo del grafico](/charts/title/update/) e [Aggiorna la legenda del grafico](/charts/legend/update/).

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più efficace per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

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