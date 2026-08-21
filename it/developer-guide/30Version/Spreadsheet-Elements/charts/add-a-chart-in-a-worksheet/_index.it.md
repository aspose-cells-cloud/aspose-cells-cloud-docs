---
title: "Aggiungi un grafico a un foglio di lavoro"
type: docs
url: /it/charts/add/
aliases: [  /it/add-a-chart-in-a-worksheet/ ]
weight: 20
description: "Scopri come aggiungere un grafico a un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud v3.0. Include endpoint, parametri, esempio cURL e frammenti di codice SDK."
keywords:
  - "aggiungi grafico Aspose.Cells"
  - "API Aspose.Cells per aggiungere grafico"
  - "API REST per grafici"
  - "esempi SDK Aspose.Cells"
ArticleTitle: "Aggiungi un grafico a un foglio di lavoro – Guida API Aspose.Cells Cloud"
---

Questa REST API aggiunge un nuovo grafico a un foglio di lavoro.

**Prerequisiti**  
Prima di chiamare questa operazione, ottieni un token di accesso JWT valido e assicurati che il workbook di destinazione sia memorizzato nella cartella o nell’area di archiviazione specificata.

## API PutWorksheetAddChart

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro          | Tipo    | Posizione | Descrizione                                                                                                                                                                              |
| ----------------------- | ------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                | stringa | path      | Nome del workbook.                                                                                                                                                                       |
| **sheetName**           | stringa | path      | Nome del foglio di lavoro.                                                                                                                                                              |
| **chartType**           | stringa | query     | Tipo di grafico (vedi la proprietà **Type** nella risorsa grafico). I tipi di grafico supportati includono **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar**, ecc. |
| **upperLeftRow**        | integer | query     | Indice della riga in alto a sinistra dell’area del grafico (in base 0).                                                                                                                 |
| **upperLeftColumn**     | integer | query     | Indice della colonna in alto a sinistra dell’area del grafico (in base 0).                                                                                                              |
| **lowerRightRow**       | integer | query     | Indice della riga in basso a destra dell’area del grafico (in base 0).                                                                                                                  |
| **lowerRightColumn**    | integer | query     | Indice della colonna in basso a destra dell’area del grafico (in base 0).                                                                                                               |
| **area**                | stringa | query     | Intervallo che fornisce i valori da rappresentare (es. `A1:B5`).                                                                                                                        |
| **isVertical**          | boolean | query     | Indica se l’orientamento del grafico è verticale.                                                                                                                                        |
| **categoryData**        | stringa | query     | Intervallo dei valori dell’asse delle categorie (es. `D1:E10`).                                                                                                                         |
| **isAutoGetSerialName** | boolean | query     | Se **true**, i nomi delle serie vengono generati automaticamente.                                                                                                                       |
| **title**               | stringa | query     | Titolo del grafico.                                                                                                                                                                      |
| **folder**              | stringa | query     | Cartella contenente il workbook.                                                                                                                                                         |
| **storageName**         | stringa | query     | Nome dell’area di archiviazione.                                                                                                                                                         |
| **dataLabels**          | boolean | query     | Mostra le etichette dei dati quando **true**.                                                                                                                                            |
| **dataLabelsPosition**  | stringa | query     | Posizione delle etichette dei dati (es. `Above`).                                                                                                                                        |
| **pivotTableSheet**     | stringa | query     | Nome del foglio contenente la tabella pivot.                                                                                                                                             |
| **pivotTableName**      | stringa | query     | Nome della tabella pivot.                                                                                                                                                                |

### **Risposta**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Bad Request                 | Parametri mancanti o non validi (es. tipo di file non supportato).          |
| 401    | Unauthorized                | Token JWT non valido o mancante.                                             |
| 413    | Payload Too Large           | Il file caricato supera il limite di dimensione.                            |
| 500    | Internal Server Error       | Errore imprevisto del server.                                                |

## Come utilizzare l'API PutWorksheetAddChart con gli SDK

### Specifica dell'API PutWorksheetAddChart

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# Non è richiesto un corpo della richiesta per questa operazione
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

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK astrae i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}