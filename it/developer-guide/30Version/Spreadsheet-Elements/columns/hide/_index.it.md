---
title: "Nascondere colonne in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Nascondi"
type: docs
url: /it/columns/hide/
aliases:
  - /it/hide-columns-in-excel-worksheet/
  - /it/hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, API per nascondere colonne, nascondere colonne Excel, REST API per nascondere colonne, Aspose.Cells SDK, automazione fogli di calcolo"
description: "Scopri come nascondere una o più colonne in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempio cURL, esempi di codice SDK e gestione degli errori."
weight: 40
---

Questa API REST nasconde colonne in un foglio di calcolo.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione | Descrizione                                                                      |
| -------------- | ------- | --------- | -------------------------------------------------------------------------------- |
| name           | string  | path      | Nome del file del workbook.                                                      |
| sheetName      | string  | path      | Nome del foglio di calcolo in cui verranno nascoste le colonne.                 |
| startColumn    | integer | query     | Indice in base zero della prima colonna da nascondere.                          |
| totalColumns   | integer | query     | Numero di colonne consecutive da nascondere, a partire da **startColumn**.      |
| folder         | string  | query     | Percorso della cartella contenente il workbook.                                 |
| storageName    | string  | query     | Nome del servizio di archiviazione in cui è ubicato il file.                    |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per chiamare facilmente i servizi web di Aspose.Cells. L'esempio riportato di seguito mostra come nascondere una colonna con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Codici di risposta possibili**

| Codice HTTP | Significato                                         | JSON di esempio (errore)                              |
| ----------- | --------------------------------------------------- | ----------------------------------------------------- |
| 200         | Operazione riuscita                                 | `{ "Code": 200, "Status": "OK" }`                     |
| 400         | Richiesta non valida (es. parametri non validi)     | `{ "Code": 400, "Message": "Intervallo colonne non valido." }` |
| 401         | Non autorizzato (token mancante o non valido)       | `{ "Code": 401, "Message": "Token di accesso non valido." }` |
| 404         | Non trovato (workbook o foglio di calcolo)         | `{ "Code": 404, "Message": "File non trovato." }`     |
| 500         | Errore interno del server                           | `{ "Code": 500, "Message": "Errore imprevisto." }`    |

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK per il Cloud

L'utilizzo di un SDK rappresenta il metodo più rapido per lo sviluppo. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}