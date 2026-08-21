---
title: "Esporta un'area del foglio di calcolo in PNG, PDF, CSV – API Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Area"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, esporta area foglio di calcolo, PNG, PDF, CSV, conversione Excel, REST API, SDK"
description: "Scopri come esportare un intervallo di celle specifico da un foglio di calcolo Excel in PNG, PDF, CSV e oltre 20 altri formati utilizzando l'API REST Aspose.Cells Cloud o gli SDK (C#, Java, Python, …)."
weight: 230
ArticleTitle: "Esporta l'area del foglio di calcolo in PNG, PDF, CSV con Aspose.Cells Cloud API – Guida completa"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API consente di convertire un'area specificata di un foglio di calcolo in vari formati di file. I formati supportati sono: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Questa guida illustra come esportare un **intervallo di celle specifico** da un foglio di calcolo Excel in PNG, PDF, CSV e oltre 20 formati aggiuntivi utilizzando l'API Aspose.Cells Cloud. Per operazioni correlate, come l'esportazione dell'intero foglio di calcolo o la conversione di un workbook, consulta le pagine **[Esporta intero foglio di calcolo](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** e **[Converti workbook in PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**.

## API REST

La [specificifica OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) definisce un’interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

### Parametri della richiesta

| Parametro            | Tipo   | Obbligatorio | Descrizione                                    |
|----------------------|--------|--------------|------------------------------------------------|
| `name`               | string | Sì           | Nome del file del workbook.                    |
| `sheetName`          | string | Sì           | Nome del foglio di calcolo di destinazione.    |
| `format`             | string | Sì           | Format di output desiderato (png, pdf, csv, …).|
| `area`               | string | No           | Intervallo di celle da esportare (es. `B3:K8`).|
| `verticalResolution`| int    | No           | Risoluzione verticale DPI per formati raster.  |
| `horizontalResolution`| int  | No           | Risoluzione orizzontale DPI per formati raster.|
| `folder`             | string | No           | Cartella nell'archivio cloud contenente il file.|
| `storage`            | string | No           | Nome del servizio di archiviazione.            |

### Risposta in caso di successo

* **200 OK** – Restituisce il file richiesto in formato binario (PNG, PDF, CSV, ecc.).

### Risposte di errore

| Codice di stato | Descrizione                                      |
|-----------------|--------------------------------------------------|
| 400             | Richiesta non valida – parametri mancanti o non validi. |
| 401             | Non autorizzato – token di autenticazione mancante o non valido. |
| 404             | Non trovato – il workbook o il foglio di calcolo specificato non esiste. |
| 500             | Errore interno del server – condizione imprevista sul server. |

**Esempio di payload di errore**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "Il parametro 'area' non è corretto. Il formato previsto è: B3:K8."
  }
}
```

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Immagine convertita (PNG binario)

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare. Un SDK astrae i dettagli di basso livello, consentendoti di concentrarti sulla logica del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}