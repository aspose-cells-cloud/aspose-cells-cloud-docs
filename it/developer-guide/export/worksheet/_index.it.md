﻿---
title: Esporta foglio di lavoro
second_title: Aspose.Cells Cloud Documen
linktitle: Workshee
type: docs
url: /it/export/excel-worksheet-to-different-formats/
keywords: Export Excel worksheet to kinds of format files
description: Aspose.Cells Cloud REST API supporta l'esportazione del foglio di lavoro Excel in tipi di file di formato. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Esporta foglio di lavoro
---
 Puoi esportare formati:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMERI](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)..

- **RESTO API**

|**API**|**Tipo**|**Descrizione**|**Collegamento spavaldo**|
|:- |:- |:- |:- |
|/celle/esporta|INVIARE|Esporta Excel dal contenuto della richiesta in un formato|[Postesportazione](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)|


 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL**strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.



- **Richiesta**

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **Risposta**

```bash
{
    "Files": [{
        "Filename": "Book1_xlsx_Sheet1.tif",
        "FileSize": 390,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet2.tif",
        "FileSize": 10040,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet3.tif",
        "FileSize": 2824,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet4.tif",
        "FileSize": 1350,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet5.tif",
        "FileSize": 12978,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet6.tif",
        "FileSize": 7002,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet7.tif",
        "FileSize": 11532,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet1.tif",
        "FileSize": 382,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet2.tif",
        "FileSize": 382,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet3.tif",
        "FileSize": 130084,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet4.tif",
        "FileSize": 120062,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **Famiglia di SDK Cloud**

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.

I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-shape-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export-shape-tiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< /tabs >}}
