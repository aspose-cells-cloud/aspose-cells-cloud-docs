---
title: "Ottieni l'asse delle categorie del grafico"
type: docs
url: /it/charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, Asse delle categorie del grafico, Excel, REST API, Archiviazione cloud, OAuth2, Documentazione API"
description: "Recupera l'asse delle categorie di un grafico in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud."
ArticleTitle: "Ottieni l'asse delle categorie del grafico – Documentazione API Aspose.Cells Cloud"
---

Questa REST API recupera l'**asse delle categorie** di un grafico.  
Per chiamare questo endpoint è necessario fornire un token di accesso OAuth 2.0 valido e il file di lavoro deve essere memorizzato nell'archiviazione cloud di Aspose.

**Prerequisiti**  
Prima di utilizzare questo endpoint, assicurati che:  

- Un token OAuth 2.0 sia stato ottenuto e sia valido per i servizi Aspose Cloud.  
- Il file di lavoro sia caricato nell'archiviazione cloud di Aspose (cartella predefinita o una specificata).  
- Stai utilizzando la versione API **v3.0**, come indicato nell'URL della richiesta.  
- L'applicazione che effettua la chiamata abbia i permessi per leggere il file di lavoro e accedere ai suoi fogli di calcolo.

## API GetChartCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**Contesto** – Rimuovere tutti i grafici da un foglio di calcolo è utile quando è necessario ripristinare il layout visivo di un foglio, sostituire visualizzazioni obsolete o preparare un file di lavoro per un riutilizzo senza mantenere i dati dei grafici precedenti.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                            |
| -------------- | ------- | -------- | ------------------------------------------------------ |
| name           | string  | path     | Il nome del file di lavoro.                            |
| sheetName      | string  | path     | Il nome del foglio di calcolo contenente il grafico.  |
| chartIndex     | integer | path     | Indice in base zero del grafico di cui si richiede l'asse. |
| folder         | string  | query    | Il percorso della cartella nell'archivio in cui risiede il file di lavoro. |
| storageName    | string  | query    | Il nome del servizio di archiviazione (se diverso da quello predefinito). |

### **Risposta**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Asse delle categorie",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto sul server. |

## Come utilizzare l'API GetChartCategoryAxis con gli SDK

### Specifica dell'API GetChartCategoryAxis

La <a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Asse delle categorie",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello e consente di concentrarsi sui compiti del proprio progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}