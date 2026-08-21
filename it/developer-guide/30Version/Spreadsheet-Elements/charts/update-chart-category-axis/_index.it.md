---
title: "Aggiorna l'asse delle categorie del grafico"
type: docs
url: /it/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, Grafico, Asse delle categorie, REST API, Excel, Cloud SDK"
description: "Aggiorna l'asse delle categorie di un grafico in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud."
ArticleTitle: "Aggiorna l'asse delle categorie del grafico – Aspose.Cells Cloud API"
---

Questa API REST aggiorna l'asse delle categorie di un grafico.

## API PostChartCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Sicurezza e autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione |
| -------------- | ------- | -------- | ----------- |
| name           | string  | path     | Nome del file Excel. |
| sheetName      | string  | path     | Nome del foglio di lavoro contenente il grafico. |
| chartIndex     | integer | path     | Indice in base zero del grafico da aggiornare. |
| axis           | object  | body     | Oggetto JSON che definisce le proprietà dell'asse delle categorie. |
| folder         | string  | query    | Cartella nello spazio di archiviazione cloud in cui si trova il file (opzionale). |
| storageName    | string  | query    | Nome dello spazio di archiviazione (opzionale). |

**Schema del corpo della richiesta – oggetto `axis`**

| Proprietà | Tipo    | Descrizione |
|----------|---------|-------------|
| IsAutomaticMajorUnit | boolean | Determina se l'intervallo principale viene calcolato automaticamente. |
| MajorUnit | number | Valore dell'intervallo principale quando `IsAutomaticMajorUnit` è `false`. |
| IsAutomaticMinorUnit | boolean | Determina se l'intervallo secondario viene calcolato automaticamente. |
| MinorUnit | number | Valore dell'intervallo secondario quando `IsAutomaticMinorUnit` è `false`. |
| Title | object | Impostazioni del titolo dell'asse (ad esempio `Text`, `Font`, `Visible`). |
| TickLabelPosition | string | Posizione delle etichette dei tick (ad esempio `Low`, `High`, `NextToAxis`). |
| ... | ... | Altre proprietà dell'asse come definite nella specifica dell'API. |

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

**Prerequisiti / Autenticazione**

Per chiamare questo endpoint è necessario ottenere un token di accesso JWT dal servizio di autenticazione di Aspose.Cells Cloud (`/connect/token`). Includere il token nell'intestazione `Authorization`, come mostrato nell'esempio seguente.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Asse delle categorie",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Esempio di risposta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Note

* L'endpoint richiede HTTPS; l'uso di HTTP potrebbe generare avvisi su contenuti misti nei browser.
* Tutti i valori segnaposto (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) devono essere sostituiti con identificatori effettivi.
* I tipi di grafico supportati per l'aggiornamento dell'asse delle categorie sono elencati nel riferimento API.

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e consente di concentrarsi sulle attività del proprio progetto. Consultare il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}