---
title: "Aggiorna Asse Secondario di Categoria del Grafico"
type: docs
url: /charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, Grafico, Asse Secondario di Categoria, API REST, Aggiorna Grafico, Excel, API Cloud"
description: "Scopri come aggiornare l'asse secondario di categoria di un grafico in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud."
ArticleTitle: "Aggiorna Asse Secondario di Categoria del Grafico – Aspose.Cells Cloud API"
---

Questa REST API aggiorna l'asse secondario di categoria di un grafico.

## API PostChartSecondCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Sicurezza e Autenticazione**

Le API REST di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione | Descrizione                                              |
| -------------- | ------- | --------- | -------------------------------------------------------- |
| name           | string  | path      | Il nome del file Excel.                                  |
| sheetName      | string  | path      | Il nome del foglio di lavoro contenente il grafico.     |
| chartIndex     | integer | path      | L'indice in base zero del grafico da aggiornare.        |
| axis           | object  | body      | L'oggetto dell'asse secondario di categoria con le nuove impostazioni. |
| folder         | string  | query     | Il percorso della cartella in cui è salvato il file.    |
| storageName    | string  | query     | Il nome del servizio di archiviazione.                   |

**Autenticazione** – L'API richiede un token di accesso OAuth 2.0 valido. Genera un token JWT seguendo la [Guida all'autenticazione](https://docs.aspose.cloud/cells/authentication/). Includi il token nell'intestazione `Authorization`, come mostrato nell'esempio cURL riportato di seguito.

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* impostazioni asse, ad es. "Title": "Nuovo Titolo Asse", "IsVisible": true */
        }
      }'
```

*Sostituisci `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}` e `{storageName}` con i tuoi valori effettivi. Il corpo della richiesta deve contenere l'oggetto `axis` con le impostazioni desiderate.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Risposta corretta (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "Nuovo Titolo Asse",
      "IsVisible": true,
      /* proprietà aggiuntive dell'asse */
    }
  }
}
```

**Risposte di errore**  

| Codice di Stato | Descrizione                                           |
|-----------------|-------------------------------------------------------|
| 400             | Richiesta non valida – parametri mancanti o non validi. |
| 401             | Non autorizzato – token JWT non valido o mancante.    |
| 404             | Non trovato – il file, il foglio di lavoro o il grafico specificato non esiste. |
| 500             | Errore interno del server – condizione imprevista sul server. |

```json
{
  "Code": 400,
  "Message": "Payload della richiesta non valido."
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

Gli SDK semplificano lo sviluppo gestendo i dettagli di basso livello e consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- Esempio C# in sospeso -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Esempio Java in sospeso -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- Esempio PHP in sospeso -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Esempio Ruby in sospeso -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Esempio Python in sospeso -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Esempio Android in sospeso -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Esempio Swift in sospeso -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Esempio Perl in sospeso -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Esempio Go in sospeso -->

{{< /tab >}}

{{< /tabs >}}

**Note e Best Practice**

* Il parametro `chartIndex` è in base zero; il primo grafico in un foglio di lavoro ha indice 0.  
* L'API supporta sia il formato di cartella di lavoro `.xlsx` che `.xls`.  
* Includi solo le proprietà necessarie nell'oggetto `axis`; le proprietà non specificate mantengono i valori esistenti.  
* Rispetta le linee guida sul limite di velocità (tipicamente 100 richieste al minuto per account) per evitare throttling.