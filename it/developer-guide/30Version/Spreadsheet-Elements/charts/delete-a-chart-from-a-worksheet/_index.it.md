---
title: "Eliminare un grafico da un foglio di lavoro"
type: docs
url: /it/charts/delete/
aliases: [  /it/delete-a-chart-from-a-worksheet/ ]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Eliminazione grafico"
  - "Foglio di lavoro"
  - "Excel"
  - "Cloud SDK"
  - "Eliminazione grafico"
  - "Riferimento API"
description: "Elimina un grafico da un foglio di lavoro tramite il suo indice in base zero utilizzando l’API REST di Aspose.Cells Cloud."
ArticleTitle: "Eliminare un grafico da un foglio di lavoro tramite l’API REST di Aspose.Cells Cloud"
---

Questa REST API elimina un grafico da un foglio di lavoro tramite il suo indice.

Per le operazioni correlate, consulta le pagine **[Aggiungi un grafico](#)** e **[Ottieni un grafico](#)**.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Sicurezza e autenticazione

Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                           |
| -------------- | ------- | --------- | ----------------------------------------------------- |
| name           | string  | path      | Nome del workbook.                                    |
| sheetName      | string  | path      | Nome del foglio di lavoro.                            |
| chartIndex     | integer | path      | Indice in base zero del grafico da eliminare.         |
| folder         | string  | query     | Cartella contenente il workbook.                      |
| storageName    | string  | query     | Nome dello storage da utilizzare.                     |


### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                | Descrizione                                                           |
|--------|----------------------------|-----------------------------------------------------------------------|
| 200    | OK                         | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida       | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato            | Token JWT non valido o mancante.                                      |
| 413    | Payload troppo grande      | Il file caricato supera il limite di dimensione.                     |
| 500    | Errore interno del server  | Errore imprevisto del server.                                         |

## Come utilizzare l’API PutWorksheetAddChart con gli SDK

### Specifica dell’API PutWorksheetAddChart

La [specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare una chiamata all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
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

L’API restituisce i seguenti codici di stato:

| Codice | Descrizione                                      |
|--------|--------------------------------------------------|
| 200    | Grafico eliminato correttamente                  |
| 400    | Richiesta non valida (ad esempio, indice non valido) |
| 401    | Non autorizzato (token JWT mancante o non valido) |
| 404    | Workbook, foglio di lavoro o grafico non trovato |
| 500    | Errore del server                                |

**Gestione degli errori:** Per informazioni dettagliate sugli errori, fare riferimento al modello generico di errore nella specifica OpenAPI.

### Utilizzo degli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells mediante vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}