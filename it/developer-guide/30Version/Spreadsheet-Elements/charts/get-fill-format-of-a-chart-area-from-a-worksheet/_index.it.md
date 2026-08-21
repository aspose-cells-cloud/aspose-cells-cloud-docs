---
title: "Ottieni il formato di riempimento dell’area del grafico – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /it/charts/chart-area/fill-format/get/
aliases: [  /it/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Area del grafico"
  - "Formato di riempimento"
  - "REST API"
  - "Excel"
description: "Recupera il formato di riempimento (colore, motivo, gradiente) di un’area di grafico in un foglio di calcolo Excel tramite l’API Aspose.Cells Cloud. Include esempio cURL, frammenti di codice SDK, passaggi di autenticazione e dettagli della risposta."
ArticleTitle: "Ottieni il formato di riempimento dell’area del grafico Aspose.Cells Cloud API v3.0"
---

Questa API REST recupera le informazioni sul formato di riempimento di un’**Area del grafico**.

**Prerequisiti**  
Per chiamare questo endpoint è necessario disporre di un token di accesso OAuth/JWT valido. Ottieni il token utilizzando il flusso di autenticazione di Aspose.Cells Cloud e includilo nell’intestazione `Authorization` come `Bearer <jwt token>`. Se stai utilizzando uno degli SDK, assicurati che l’SDK sia configurato con i tuoi `client_id` e `client_secret` prima di richiamare il metodo.

## API GetChartAreaFillFormat

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                |
| -------------- | ------- | --------- | ------------------------------------------ |
| name           | string  | path      | Nome del foglio di calcolo (workbook).     |
| sheetName      | string  | path      | Nome del foglio di calcolo (worksheet).    |
| chartIndex     | integer | path      | Indice del grafico.                        |
| folder         | string  | query     | Cartella contenente il foglio di calcolo.  |
| storageName    | string  | query     | Nome dello storage.                        |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) definiscono un’interfaccia di programmazione accessibile pubblicamente e consentono di eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere ai servizi web di Aspose.Cells. L’esempio seguente mostra come chiamare l’API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Note**  
- Una chiamata riuscita restituisce HTTP 200 con i dettagli del formato di riempimento.  
- HTTP 401 indica un errore di autenticazione (token non valido o mancante).  
- HTTP 404 viene restituito quando il foglio di calcolo, il foglio o l’indice del grafico specificato non esistono.  
- HTTP 500 indica un errore lato server; riprova la richiesta o contatta il supporto se il problema persiste.

| Codice | Significato                                              |
|--------|----------------------------------------------------------|
| 200    | Operazione riuscita – formato di riempimento restituito |
| 401    | Non autorizzato – token non valido o mancante           |
| 404    | Non trovato – foglio di calcolo, foglio o grafico non trovato |
| 500    | Errore interno del server                                |

Per le operazioni correlate, consulta gli endpoint **Get Chart Area Border** (Ottieni il bordo dell’area del grafico) e **Get Chart Title** (Ottieni il titolo del grafico).

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK cloud

L’utilizzo di un SDK rappresenta il modo più efficiente per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}
---