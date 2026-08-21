---
title: "Elimina il titolo di un grafico in un foglio di lavoro"
type: docs
url: /it/charts/delete-chart-title/
aliases: [  /it/delete-chart-title-in-a-worksheet/ ]
weight: 150
keywords: "Aspose.Cells, API cloud, elimina titolo grafico, Excel, REST, SDK"
description: "Scopri come rimuovere il titolo di un grafico da un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud (v4.0). Include esempi in cURL, SDK e gestione degli errori."
---

Questa API REST elimina il titolo di un grafico.

## API REST

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### Sicurezza e autenticazione

Le API REST di Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                              |
| -------------- | ------- | --------- | ---------------------------------------- |
| name           | string  | path      | Nome del file del libro di lavoro.       |
| sheetName      | string  | path      | Nome del foglio di lavoro.               |
| chartIndex     | integer | path      | Indice in base zero del grafico.         |
| folder         | string  | query     | Cartella contenente il libro di lavoro.  |
| storageName    | string  | query     | Nome dell'archivio.                      |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                |
|--------|-----------------------------|------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                           |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.          |
| 500    | Errore interno del server   | Errore imprevisto nel server.                              |

## Come utilizzare l'API DeleteWorksheetChartTitle con gli SDK

### Specifica dell'API DeleteWorksheetChartTitle

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartTitle) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio riportato di seguito mostra come effettuare la chiamata, incluso il token **Bearer JWT** obbligatorio per l'autenticazione.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -X DELETE \
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

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells tramite vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_title_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3898d60ea8f7ea7bb460ffb5d7d29504" >}}

{{< /tab >}}

{{< /tabs >}}