---
title: "Adattamento automatico di più colonne in un foglio di lavoro Excel"
second_title: "Documento"
linktitle: "Colonne"
type: docs
url: /it/worksheets/autofit/columns/
aliases: [  /it/autofit-multiple-columns-of-worksheet/ ]
keywords: "Aspose.Cells, adattamento automatico colonne, Excel API, foglio di calcolo cloud, REST"
description: "Scopri come eseguire l'adattamento automatico di più colonne in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint, parametri, esempio cURL, gestione errori e frammenti di codice SDK per C#, Java, Python e altro ancora."
weight: 20
---

Questa API REST esegue l'**adattamento automatico di più colonne** in un foglio di lavoro Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### **Parametri della richiesta**

| Nome parametro      | Tipo    | Posizione | Descrizione                                                                                                                                  |
| ------------------- | ------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| name                | string  | path      | Nome del file.                                                                                                                               |
| sheetName           | string  | path      | Nome del foglio di lavoro.                                                                                                                   |
| firstColumn         | integer | query     | Indice della colonna iniziale.                                                                                                                |
| lastColumn          | integer | query     | Indice della colonna finale.                                                                                                                  |
| autoFitterOptions\* | object  | body      | Opzioni dell'adattatore automatico (vedere [Opzioni dell'adattatore automatico](/it/cells/auto-fitter-options/)). Include `AutoFitMergedCells`, `IgnoreHidden` e `OnlyAuto`. |
| firstRow            | integer | query     | Indice della riga iniziale per l'adattamento automatico (**opzionale**).                                                                      |
| lastRow             | integer | query     | Indice della riga finale per l'adattamento automatico (**opzionale**).                                                                        |
| folder              | string  | query     | Percorso della cartella nello storage (**opzionale**).                                                                                        |
| storageName         | string  | query     | Nome dello storage (**opzionale**).                                                                                                           |

\*Il nome del parametro è visualizzato come link alla documentazione correlata.

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=5&firstColumn=0" \
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

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sui compiti del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

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