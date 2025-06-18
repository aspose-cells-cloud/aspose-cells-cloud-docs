---
title: Importa la doppia matrice nel foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importa doppia arra
type: docs
url: /it/import/double-array/
aliases: [/import-double-array-into-excel-worksheet/,/import-double-array-into-worksheet/,/import-data/double-array/]
keywords: Import double array data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati a doppio array nei file Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 20
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Importa doppio array nel foglio di lavoro Excel
---
Questo REST API `import double array data` nel foglio di lavoro Excel.

La richiesta è una richiesta HTTP con contenuto in più parti (vedi[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto in più parti contiene i dati ImportDoubleArrayOption e la seconda contiene un file di dati.

## RSETAPI

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

I parametri importanti sono descritti nella tabella seguente:


**ImportDoubleArrayOption**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Prima riga| int||
| Prima colonna| int||
| È verticale| corda| vero falso.|
| Dati|Doppio[]||
| Foglio di lavoro di destinazione| corda| nome del foglio di lavoro di destinazione.|
| IsInserisci| corda| vero falso.|
| ImportDataType| corda|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fonte| FileSource| Indica la posizione del file di dati quando il parametro BatchData è null.|



**Esempio**

```xml

<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>

```

```json
{
    "Data": [1.99, 1.9, 2.0],
    "DestinationWorksheet": "Sheet1",
    "FirstRow": 0,
    "FirstColumn": 0,
    "IsVertical": false,
    "IsInsert": true,
    "importDataType": "DoubleArray"
}

```

## Famiglia di SDK Cloud

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.

I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




