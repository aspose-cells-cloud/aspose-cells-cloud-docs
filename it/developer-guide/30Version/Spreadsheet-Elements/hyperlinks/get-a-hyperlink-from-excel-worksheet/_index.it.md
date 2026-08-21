---
title: "Ottieni collegamento ipertestuale del foglio di lavoro"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, ottieni collegamento ipertestuale del foglio di lavoro, API Excel per collegamenti ipertestuali, REST, autenticazione JWT, foglio di lavoro Excel, endpoint API"
description: "Recupera un collegamento ipertestuale specifico da un foglio di lavoro Excel utilizzando l'API Aspose.Cells Cloud (versione 3.0). Include endpoint, parametri, esempio cURL, dettagli sull'autenticazione, gestione degli errori e frammenti di SDK."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Ottieni collegamento ipertestuale del foglio di lavoro"
---

Questa REST API recupera un **collegamento ipertestuale** del foglio di lavoro tramite la **API Aspose.Cells Get Hyperlink**.

## Sicurezza e autenticazione

Le API Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Prima di chiamare l'endpoint, ottieni un token di accesso JWT utilizzando il tuo client ID e secret e includilo nell'intestazione `Authorization: Bearer <jwt token>`.

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Parametri della richiesta

| Nome parametro | Tipo    | Posizione | Descrizione                                             |
| -------------- | ------- | --------- | ------------------------------------------------------- |
| name           | string  | path      | Nome del file Excel.                                    |
| sheetName      | string  | path      | Nome del foglio di lavoro contenente il collegamento.  |
| hyperlinkIndex | integer | path      | Indice in base zero del collegamento ipertestuale da recuperare. |
| folder         | string  | query     | Cartella in cui è memorizzato il documento.            |
| storageName    | string  | query     | Nome del servizio di archiviazione.                     |

### Risposte di errore

| Codice HTTP | Motivo                                              | Corpo di esempio                                                    |
| ----------- | --------------------------------------------------- | ------------------------------------------------------------------- |
| **400**     | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore di parametro non valido." }`     |
| **401**     | Non autorizzato – token JWT mancante o non valido.  | `{ "Code":"401", "Message":"Token di accesso mancante o non valido." }` |
| **404**     | Non trovato – cartella di lavoro o foglio di lavoro inesistente. | `{ "Code":"404", "Message":"File non trovato." }`                   |
| **500**     | Errore interno del server – errore imprevisto nel server. | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}