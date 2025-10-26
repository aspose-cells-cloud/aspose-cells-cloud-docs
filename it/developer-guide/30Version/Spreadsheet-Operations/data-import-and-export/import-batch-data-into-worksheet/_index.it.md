---
title: Importa dati batch nel foglio di lavoro Excel
second_title: Documen
linktitle: Importa dati batch
type: docs
url: /it/import-batch-data-into-excel/
aliases: [/import-batch-data-into-worksheet/,/import-data/batch-data/,/import/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati batch in file Excel. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 19
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Importa dati batch nel foglio di lavoro Excel
---
Questo foglio di lavoro REST API `import batch data` in Excel.

La richiesta è una richiesta HTTP con contenuto multiparte (vedere[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multiparte contiene i dati ImportBatchDataOption e la seconda contiene un file di dati.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

I parametri importanti sono descritti nella seguente tabella:

**ImportBatchDataOption**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Dati in batch|Lista<CellValue> | dati batch|
|Foglio di lavoro sulla destinazione| corda| nome del foglio di lavoro di destinazione.|
| ÈInserisci| corda| vero/falso.|
| ImportDataType| corda|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fonte| FileSource| Indica la posizione del file di dati quando il parametro BatchData è null.|

**CellValue**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| indice di riga| interno||
| indice di colonna| interno||
| tipo| corda| tipo di dati|
| valore| corda||
| stile| Stile(oggetto)||

**FileSource**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Tipo di origine file| corda| InMemoryFiles/CloudFileSystem/RequestFiles|
| Percorso file| corda| posizione del file|

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

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

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
