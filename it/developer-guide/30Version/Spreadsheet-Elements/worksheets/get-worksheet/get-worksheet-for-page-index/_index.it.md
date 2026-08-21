---
title: "Esporta una pagina di foglio di lavoro – Riferimento API di Aspose.Cells Cloud"
ArticleTitle: "Esporta una pagina di foglio di lavoro – Riferimento API di Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Pagina"
type: docs
url: /it/worksheets/page-to-different-formats/
aliases: [  /it/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, esportazione pagina foglio di lavoro, PDF, PNG, CSV, API REST, autenticazione JWT, formati file"
description: "Scopri come esportare una pagina specifica di un foglio di lavoro in PDF, PNG, CSV e altri formati utilizzando l'API REST di Aspose.Cells Cloud. Include richiesta cURL, guida ai parametri e esempi di SDK per diversi linguaggi."
weight: 240
---

Esportare una pagina specifica di un foglio di lavoro è utile quando hai bisogno di un'istantanea stampabile di un report, di un'immagine di un grafico o di un'estratto di dati senza scaricare l'intero libro di lavoro. Questo endpoint consente di recuperare una singola pagina nel formato più adatto al flusso di lavoro successivo.

L'API [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) consente di convertire una pagina specifica di un foglio di lavoro in vari formati file. I formati supportati sono: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## API REST

La [specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

> **Prerequisiti** – Devi disporre di un token di autenticazione JWT valido e del libro di lavoro memorizzato in una cartella cloud specificata tramite il parametro `folder`.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Risposta** – Il servizio restituisce la pagina richiesta nel formato scelto. Per i formati immagine (png, jpeg, gif, ecc.) il corpo contiene l'immagine binaria; per i formati documento (pdf, xls, csv, …) il corpo contiene il contenuto del file. Una chiamata riuscita restituisce HTTP 200.

*Esempio di risposta PNG (estratto in base64 troncato):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Parametri**

| Parametro              | Tipo    | Descrizione                                                             | Valore predefinito |
| ---------------------- | ------- | ----------------------------------------------------------------------- | ------------------ |
| `format`               | string  | Format del file di output (ad esempio, `pdf`, `png`, `csv`).            | `pdf`              |
| `verticalResolution`   | integer | Risoluzione verticale dell'immagine renderizzata (DPI).                 | `100`              |
| `horizontalResolution` | integer | Risoluzione orizzontale dell'immagine renderizzata (DPI).               | `100`              |
| `pageIndex`            | integer | Indice in base zero della pagina del foglio di lavoro da esportare (`0` = prima pagina). | `0`                |
| `folder`               | string  | Cartella di archiviazione cloud in cui si trova il libro di lavoro sorgente. | —                  |

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                               |
| ------ | --------------------------- | --------------------------------------------------------- |
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante.                          |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione.         |
| 500  | Errore interno del server   | Errore imprevisto sul server.                             |

**Errori possibili**

- **401 Non autorizzato** – Token JWT non valido o mancante.
- **404 Non trovato** – Il libro di lavoro o il foglio di lavoro specificato non esiste.
- **400 Richiesta non valida** – Valore di parametro non valido (ad esempio, `format` non supportato).
- **500 Errore interno del server** – Problema imprevisto lato server.

## Famiglia di SDK cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}