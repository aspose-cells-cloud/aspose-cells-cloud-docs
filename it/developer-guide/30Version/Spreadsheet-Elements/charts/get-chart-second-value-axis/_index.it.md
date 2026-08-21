---
title: "Ottieni il Secondo Asse dei Valori del Grafico"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, secondo asse dei valori del grafico, Excel, API REST, cloud, API, asse del grafico Excel
description: Recupera il secondo asse dei valori di un grafico specificato in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud.
ArticleTitle: "Ottieni il Secondo Asse dei Valori del Grafico – Aspose.Cells Cloud API"
---

Questa REST API recupera il secondo asse dei valori di un grafico.

## API GetChartSecondValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Sicurezza e Autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione | Descrizione                                       |
| -------------- | ------- | --------- | ------------------------------------------------- |
| name           | string  | path      | Il nome del file Excel.                           |
| sheetName      | string  | path      | Il nome del foglio di calcolo contenente il grafico. |
| chartIndex     | integer | path      | L'indice in base zero del grafico.                |
| folder         | string  | query     | La cartella in cui è memorizzato il file.         |
| storageName    | string  | query     | Il nome dell'archivio Aspose Cloud.               |

**Prerequisiti**: Un token di accesso JWT valido ottenuto tramite il flusso OAuth2 di Aspose Cloud deve essere fornito nell'intestazione `Authorization` di ogni richiesta.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL. Tutti gli endpoint Aspose Cloud richiedono HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
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
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Second Value Axis"
  }
}
```

**Campi della risposta**

- **Code** – Codice di stato HTTP dell'operazione (es. `200` per successo).  
- **Status** – Descrizione testuale dello stato (`"OK"` per successo).  
- **Axis** – Oggetto contenente i dettagli del secondo asse dei valori:  
  - **AxisId** – Identificativo dell'asse.  
  - **IsVisible** – Valore booleano che indica se l'asse è visibile.  
  - **MinimumScale** – Valore minimo visualizzato sull'asse.  
  - **MaximumScale** – Valore massimo visualizzato sull'asse.  
  - **MajorUnit** – Intervallo tra le tacche principali.  
  - **MinorUnit** – Intervallo tra le tacche secondarie.  
  - **Title** – Testo del titolo dell'asse.

**Risposte di errore** (non 200)

- `400 Bad Request` – Parametri non validi o richiesta malformata.  
- `401 Unauthorized` – Token JWT mancante o non valido.  
- `404 Not Found` – File, foglio di calcolo o grafico specificato inesistente.  
- `500 Internal Server Error` – Errore imprevisto del server.

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sui compiti del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
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