---
title: "Ottieni Tutti gli Hyperlink – Aspose.Cells Cloud REST API"
type: docs
url: /it/hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, Ottieni Tutti gli Hyperlink, Excel API, REST API, Cloud SDK, Esempio cURL, hyperlink in fogli di calcolo"
description: "Recupera tutti gli hyperlink da un foglio di lavoro in un file Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint HTTPS, parametri obbligatori, esempio cURL, schema di risposta e codice di esempio per SDK."
weight: 10
ArticleTitle: "Ottieni Tutti gli Hyperlink – Documentazione Aspose.Cells Cloud REST API"
---

Questa REST API consente di recuperare **tutti gli hyperlink** da un foglio di lavoro specifico in un workbook Excel.

## Sicurezza e Autenticazione

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Parametri della richiesta

| Nome Parametro | Tipo   | Posizione | Obbligatorio | Predefinito | Descrizione                           |
| -------------- | ------ | --------- | ------------ | ----------- | ------------------------------------- |
| name           | string | path      | Sì           | –           | Nome del documento Excel.             |
| sheetName      | string | path      | Sì           | –           | Nome del foglio di lavoro.            |
| folder         | string | query     | No           | –           | Cartella contenente il documento.     |
| storageName    | string | query     | No           | –           | Nome del servizio di archiviazione da utilizzare. |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio riportato di seguito mostra come chiamare l'API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

La risposta JSON contiene un oggetto `Hyperlinks`.

- **Count** – numero totale di hyperlink presenti nel foglio di lavoro.
- **HyperlinkList** – un array in cui ogni elemento contiene un oggetto `link`. La proprietà `Href` memorizza l'indirizzo dell'hyperlink, mentre `Rel`, `Title` e `Type` forniscono metadati aggiuntivi (spesso `null` per link semplici).

### Risposte di errore

| Codice HTTP | Motivo                                                | Corpo di esempio                                                  |
| ----------- | ----------------------------------------------------- | ----------------------------------------------------------------- |
| **400**     | Richiesta non valida – parametri mancanti o non validi. | `{ "Code":"400", "Message":"Valore di parametro non valido." }`   |
| **401**     | Non autorizzato – token JWT mancante o non valido.    | `{ "Code":"401", "Message":"Il token di accesso è mancante o non valido." }` |
| **404**     | Non trovato – il workbook o il foglio di lavoro non esistono. | `{ "Code":"404", "Message":"File non trovato." }`             |
| **500**     | Errore interno del server – errore imprevisto.        | `{ "Code":"500", "Message":"Si è verificato un errore imprevisto." }` |

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo più rapido per integrare questa funzionalità. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Controlla il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}