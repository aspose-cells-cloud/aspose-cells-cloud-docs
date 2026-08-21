---
title: "Adattamento automatico della colonna in Excel con Aspose.Cells Cloud API – Guida rapida"
second_title: "Documento"
linktitle: "Colonna"
type: docs
url: /worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: "Aspose.Cells Cloud, adattamento automatico colonna, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Scopri come ridimensionare automaticamente una colonna (o un intervallo di colonne) in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi cURL, SDK (C#, Java, Python, ecc.) e dettagli completi su richiesta e risposta."
weight: 10
---

Questa API REST regola automaticamente la larghezza di una singola colonna o di un intervallo contiguo di colonne in un foglio di calcolo Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### Parametri della richiesta

| Nome parametro    | Tipo    | Posizione | Descrizione                                                                                      |
| ----------------- | ------- | --------- | ------------------------------------------------------------------------------------------------ |
| name              | string  | path      | Nome del file Excel.                                                                             |
| sheetName         | string  | path      | Nome del foglio di calcolo.                                                                      |
| firstColumn       | integer | query     | Indice in base zero della prima colonna da adattare automaticamente.                             |
| lastColumn        | integer | query     | Indice in base zero dell'ultima colonna da adattare automaticamente.                             |
| autoFitterOptions | object  | body      | Opzioni che controllano il comportamento dell'adattamento automatico (vedere [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow          | integer | query     | Indice in base zero della prima riga considerata nel calcolo della larghezza della colonna.      |
| lastRow           | integer | query     | Indice in base zero dell'ultima riga considerata nel calcolo della larghezza della colonna.      |
| folder            | string  | query     | Cartella nello storage in cui si trova il file.                                                  |
| storageName       | string  | query     | Nome del servizio di storage.                                                                    |

### Risposte di errore

| Status HTTP | Significato                                  | Corpo JSON di esempio                                          |
| ----------- | -------------------------------------------- | ------------------------------------------------------------- |
| 400         | Parametro/i non valido/i                     | `{"Code":400,"Message":"Parametro 'firstColumn' non valido."}` |
| 401         | Non autorizzato – token JWT mancante o non valido | `{"Code":401,"Message":"Autorizzazione non riuscita."}`        |
| 404         | File o foglio di calcolo non trovato         | `{"Code":404,"Message":"Foglio 'Sheet1' non trovato."}`        |
| 500         | Errore interno del server                    | `{"Code":500,"Message":"Si è verificato un errore imprevisto."}` |

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando **cURL** per richiamare i servizi Aspose.Cells Cloud. L'esempio seguente mostra come richiamare l'endpoint di adattamento automatico della colonna.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK per il cloud

Utilizzare un SDK rappresenta il metodo più rapido per integrare l'API nella propria applicazione. Gli SDK gestiscono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare l'endpoint di adattamento automatico della colonna utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}