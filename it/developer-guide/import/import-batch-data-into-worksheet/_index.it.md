---
title: Importa dati batch nel foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importa dati batch
type: docs
url: /it/import/batch-data/
aliases: [/import-batch-data-into-excel-worksheet/,/import-batch-data-into-worksheet/,/import-data/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati batch in file Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 19
---
Questo REST API `import batch data` nel foglio di lavoro Excel.

La richiesta è una richiesta HTTP con contenuto in più parti (vedi[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto in più parti contiene i dati ImportBatchDataOption e la seconda contiene un file di dati.

## RSETAPI

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

I parametri importanti sono descritti nella tabella seguente:


**ImportBatchDataOpzione**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Dati batch|Elenco<CellValue> | dati batch|
| Foglio di lavoro di destinazione| corda| nome del foglio di lavoro di destinazione.|
| IsInserisci| corda| vero falso.|
| ImportDataType| corda|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fonte| FileSource| Indica la posizione del file di dati quando il parametro BatchData è null.|



**ValoreCella**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| rigaIndice| int||
| colonnaIndice| int||
| tipo| corda| tipo di dati|
| valore| corda||
| stile| Stile(oggetto)||



**FileSource**
|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| FileSourceType| corda| InMemoryFiles/CloudFileSystem/RequestFiles|
| Percorso del file| corda| posizione dell'archivio|


**Esempio**

```xml
<ImportIntArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportIntArrayOption>

```

## Famiglia di SDK Cloud

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si prende cura dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Repositorio GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Cloud Aspose.Cells.

I seguenti esempi di codice dimostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
