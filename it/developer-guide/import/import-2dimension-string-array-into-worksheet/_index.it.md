---
title: Importa 2 Dimension String Array in Excel Workshee
second_title: Aspose.Cells Cloud Documen
linktitle: Importa l'arra di stringhe a 2 dimensioni
type: docs
url: /it/import/2dimension-string-array/
aliases: [/import-2dimension-string-array-into-excel-worksheet/,/import-2dimension-string-array-into-worksheet/,/import-data/-2dimension-string-array/,/import-data/2dimension-string-array/]
keywords: Import 2 dimension string array data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati di array di stringhe a 2 dimensioni in file Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
---
Questo REST API `import 2 dimension string array data` nel foglio di lavoro Excel.

La richiesta è una richiesta HTTP con contenuto in più parti (vedi[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multiparte contiene i dati Import2DimensionStringArrayOption e la seconda contiene un file di dati.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

I parametri importanti sono descritti nella tabella seguente:

**Import2DimensionStringArrayOption**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| Prima riga| int||
| Prima colonna| int||
| Dati|Corda[,]||
| Foglio di lavoro di destinazione| corda| nome del foglio di lavoro di destinazione.|
| IsInsert| corda| vero falso.|
| Tipo di dati di importazione| corda|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fonte| FileSource| Indica la posizione del file di dati quando il parametro BatchData è nullo.|



**Esempio**

```json

{
    "Data": [
        ["1.0", "2.9"],
        ["2.0", "2.1"]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 1,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionStringArray"
}

```

## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




