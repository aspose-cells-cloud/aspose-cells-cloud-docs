---
title: "Elimina tutti i grafici da un foglio di lavoro"
type: docs
url: /it/charts/clear/
aliases: [/it/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, Cloud, eliminare, tutti i grafici, foglio di lavoro, REST API, DELETE, SDK"
description: "Scopri come eliminare ogni grafico in un foglio di lavoro utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempio cURL, frammenti di codice SDK, passaggi di autenticazione e gestione degli errori."
ArticleTitle: "Elimina tutti i grafici da un foglio di lavoro utilizzando l'API Aspose.Cells Cloud"
---

Questa API REST elimina tutti i grafici dal foglio di lavoro specificato.

**Contesto** – Rimuovere tutti i grafici da un foglio di lavoro è utile quando è necessario ripristinare il layout visivo di un foglio, sostituire visualizzazioni obsolescenti o preparare un libro di lavoro per una nuova utilizzazione senza conservare i dati dei grafici precedenti.

Prima di chiamare l'API, assicurati che siano soddisfatti i seguenti prerequisiti:

- È disponibile un token JWT valido per l'autenticazione.  
- Il file del libro di esercizio esiste nella posizione e nella cartella di archiviazione specificate.  
- Stai utilizzando la versione dell'API **v3.0**.

## API DeleteWorksheetClearCharts

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                              |
| -------------- | ------ | -------- | ---------------------------------------- |
| name           | string | path     | Nome del file del libro di esercizio.    |
| sheetName      | string | path     | Nome del foglio di lavoro.               |
| folder         | string | query    | Cartella in cui è memorizzato il libro di esercizio. |
| storageName    | string | query    | Nome dell'archiviazione.                 |

**Intestazioni della richiesta**

| Intestazione    | Descrizione                     |
|---------------|---------------------------------|
| Authorization | Bearer `<token JWT>`            |
| Accept        | `application/json`              |
| Content-Type  | `application/json` (nessun corpo)   |

**Corpo della richiesta**

L'operazione DELETE **non richiede** un corpo della richiesta.

**Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto sul server. |

*Esempi di risposte di errore*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Parametro non valido: 'sheetName' è obbligatorio."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Autenticazione non riuscita. Token JWT non valido."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "Il payload della richiesta supera la dimensione massima consentita."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "Si è verificato un errore imprevisto sul server."
}
```

## Come utilizzare l'API DeleteWorksheetClearCharts con gli SDK

### Specifica dell'API DeleteWorksheetClearCharts

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
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

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo quando è necessario **eliminare tutti i grafici** da un foglio di lavoro. Un SDK gestisce i dettagli di basso livello e ti permette di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---