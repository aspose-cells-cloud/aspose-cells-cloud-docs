---
title: "Ottenere le interruzioni di pagina orizzontali"
second_title: "Documento"
linktitle: "Ottenere le interruzioni di pagina orizzontali"
type: docs
url: /it/page-breaks/get-horizontal-page-breaks/
aliases: [  /it/get-horizontal-page-breaks-inside-worksheet/ ]
keywords: "interruzioni di pagina orizzontali, Aspose.Cells Cloud, API REST, foglio di calcolo Excel, SDK"
description: "Recupera le interruzioni di pagina orizzontali da un foglio di calcolo Excel tramite l'API Aspose.Cells Cloud. Include l'endpoint, i parametri, un esempio cURL, il formato della risposta e frammenti di codice SDK per C#, Java, Python e altri."
ArticleTitle: "Ottenere le interruzioni di pagina orizzontali - Documentazione API Aspose.Cells Cloud"
weight: 10
---

**Interruzione di pagina orizzontale** – una pausa basata sulla riga che forza il foglio di calcolo a iniziare una nuova pagina stampata dopo la riga specificata. Questa API REST recupera tali interruzioni di pagina orizzontali.

## Sicurezza e autenticazione

Le API Aspose.Cells Cloud sono sicure e richiedono [autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione | Descrizione                                                        |
| -------------- | ------ | --------- | ------------------------------------------------------------------ |
| name           | string | path      | Il nome del file Excel.                                            |
| sheetName      | string | path      | Il nome del foglio di calcolo.                                     |
| folder         | string | query     | Il percorso della cartella nello storage in cui si trova il file. _(opzionale)_ |
| storageName    | string | query     | Il nome dello storage. _(opzionale)_                               |

La <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="Specifica OpenAPI per GetHorizontalPageBreaks">Specifica OpenAPI</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## Gestione degli errori

| Stato HTTP | Descrizione                                                   | Esempio JSON                                           |
| ---------- | ------------------------------------------------------------- | ------------------------------------------------------ |
| 400        | Richiesta non valida – parametri mancanti o non validi.       | `{ "Code": 400, "Message": "Parametro non valido." }`  |
| 401        | Non autorizzato – token JWT mancante o non valido.            | `{ "Code": 401, "Message": "Autenticazione non riuscita." }` |
| 404        | Non trovato – il file o il foglio di calcolo specificato non esiste. | `{ "Code": 404, "Message": "Risorsa non trovata." }`    |
| 500        | Errore interno del server – condizione imprevista sul server. | `{ "Code": 500, "Message": "Errore del server." }`     |

## Famiglia di SDK Cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}