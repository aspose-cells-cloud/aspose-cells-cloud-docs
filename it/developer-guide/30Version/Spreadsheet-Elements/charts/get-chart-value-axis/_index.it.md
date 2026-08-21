---
title: "Ottenere l'asse dei valori di un grafico"
type: docs
url: /it/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Asse dei valori del grafico, REST API, Excel, Cloud SDK, Ottenere l'asse dei valori di un grafico
description: "Aspose.Cells Cloud REST API - Recupera l'asse dei valori di un grafico in un foglio di calcolo Excel."
ArticleTitle: "Ottenere l'asse dei valori di un grafico - Aspose.Cells Cloud REST API"
---

Questa REST API consente di recuperare l'asse dei valori di un grafico. Fa parte della **Aspose.Cells Cloud REST API** e funziona con fogli di calcolo Excel archiviati nel cloud.

Per operazioni correlate, consulta l'endpoint **[Get Chart Category Axis](/charts/category-axis/get/)**.

## API GetChartValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                                  |
| -------------- | ------- | --------- | ------------------------------------------------------------ |
| name           | string  | path      | Il nome del file Excel (inclusa l'estensione).              |
| sheetName      | string  | path      | Il nome del foglio di calcolo contenente il grafico.        |
| chartIndex     | integer | path      | L'indice in base zero del grafico all'interno del foglio di calcolo. |
| folder         | string  | query     | La cartella nello storage cloud in cui si trova il file.    |
| storageName    | string  | query     | Il nome del servizio di storage (ad esempio, Aspose Cloud). |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
 -X GET \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Valori",
    "Format": {
      "NumberFormat": "Generale",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Codici di stato HTTP possibili**

| Codice | Descrizione                                                    |
|--------|----------------------------------------------------------------|
| 200    | Operazione riuscita – le informazioni sull'asse dei valori vengono restituite. |
| 400    | Richiesta non valida – mancano parametri obbligatori o sono non validi. |
| 401    | Non autorizzato – il token di autenticazione manca o non è valido. |
| 404    | Non trovato – il workbook, il foglio di calcolo o il grafico specificati non esistono. |
| 500    | Errore interno del server – si è verificato un errore imprevisto sul server. |

La risposta contiene un oggetto dettagliato `ValueAxis` con proprietà come `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` e `Format`. In un'implementazione completa, potrebbero essere forniti ulteriori dettagli sul formato.

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK per il cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Gli esempi di codice seguenti mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- Esempio C# placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Esempio Java placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- Esempio PHP placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Esempio Ruby placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Esempio Python placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Esempio Android placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Esempio Swift placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Esempio Perl placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Esempio Go placeholder -->

{{< /tab >}}

{{< /tabs >}}