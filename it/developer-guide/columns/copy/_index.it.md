﻿---
title: Copia le colonne su un foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Poliziotto
type: docs
url: /it/columns/copy/
aliases: [/copy-columns-in-excel-worksheet/,/copy-columns-in-an-excel-worksheet/]
keywords: Copy column on an Excel workshee
description: Aspose.Cells Cloud REST API supporta la copia della colonna su un foglio di lavoro Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Copia colonne su un foglio di lavoro Excel
---
Questo REST API copia `columns` in un foglio di lavoro Excel.

## RSETAPI
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
 
```
 I parametri della richiesta sono:
 
| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| nome| corda| sentiero| Il nome della cartella di lavoro.|
| nomefoglio| corda| sentiero| Il nome del foglio di lavoro.|
| sourceColumnIndex| numero intero| domanda| Indice della colonna di origine|
| destinazioneColumnIndex| numero intero| domanda| Indice della colonna di destinazione|
| colonnaNumero| numero intero| domanda| Il numero della colonna copiata|
| foglio di lavoro| corda| domanda||
| cartella| corda| domanda| La cartella documenti.|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL**strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. Nell'esempio seguente viene illustrato come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&ColumnNumber=10" -H "accept: application/json" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

 {

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Famiglia di SDK Cloud

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.

I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:



{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Columns-CopyColumnsInWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-Columns-CopyColumnsInWorksheet-copy-Columns-in-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Columns-PostCopyWorksheetColumns-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Columns-copy_worksheet_Columns-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "CopyColumnsInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Columns-CopyColumnsInWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-Columns-CopyColumnsInWorksheet-copy-Columns-in-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Columns-CopyColumnsInWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "dec38026e75ab416ae85afd684c924d6" >}}

{{< /tab >}}

{{< /tabs >}}
