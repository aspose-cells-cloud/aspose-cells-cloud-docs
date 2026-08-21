---
title: "Copia il contenuto e i formati da un altro foglio di lavoro."
second_title: "Document"
linktitle: "Copia"
type: docs
url: /it/worksheets/copy/
aliases: [  /it/copy-excel-worksheet/ ]
keywords: "Aspose Cells API per copiare fogli di lavoro, REST API per copiare fogli Excel, Aspose Cloud SDK per copiare, copiare fogli di calcolo"
description: "Scopri come copiare un foglio di lavoro e i relativi formati in un nuovo foglio utilizzando l'API REST di Aspose.Cells Cloud. Include endpoint, parametri, esempi cURL e SDK per C#, Java, Python e altri linguaggi."
weight: 20
---

Questa REST API copia un foglio di lavoro e i suoi formati in un nuovo foglio all'interno dello stesso workbook.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

I parametri della richiesta sono elencati di seguito:

| Nome Parametro   | Tipo   | Posizione | Descrizione                                                              |
| ---------------- | ------ | --------- | ------------------------------------------------------------------------ |
| `name`           | string | path      | Il nome del file del workbook.                                           |
| `sheetName`      | string | path      | Il nome del foglio di lavoro di destinazione (il nuovo foglio).         |
| `sourceSheet`    | string | query     | Il nome del foglio di lavoro da copiare.                                |
| `options`        | object | body      | Oggetto JSON contenente le opzioni di copia (es. larghezza colonne, formule). |
| `sourceWorkbook` | string | query     | Il nome del workbook sorgente, se diverso dal workbook corrente.        |
| `sourceFolder`   | string | query     | Il percorso della cartella in cui è memorizzato il workbook sorgente.   |
| `folder`         | string | query     | Il percorso della cartella in cui verrà salvato il workbook di destinazione. |
| `storageName`    | string | query     | Il nome del servizio di archiviazione da utilizzare.                    |

### Esempi di richiesta e risposta

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Gestione degli errori

L'API restituisce i codici di stato HTTP standard insieme a un corpo di errore in formato JSON. Le risposte tipiche includono:

| Codice HTTP | Descrizione                                                | Esempio di corpo di errore JSON                               |
| ----------- | ---------------------------------------------------------- | ------------------------------------------------------------- |
| 400         | Richiesta non valida – parametri mancanti o non validi.    | `{ "Code": 400, "Message": "Parametri della richiesta non validi." }`   |
| 401         | Non autorizzato – token mancante o non valido.             | `{ "Code": 401, "Message": "Autenticazione non riuscita." }`        |
| 404         | Non trovato – il workbook, il foglio di lavoro o la cartella non esistono. | `{ "Code": 404, "Message": "Risorsa non trovata." }`           |
| 500         | Errore interno del server – condizione imprevista.         | `{ "Code": 500, "Message": "Si è verificato un errore imprevisto." }` |

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}