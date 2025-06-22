---
title: Importa array di stringhe nel foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importa stringa arra
type: docs
url: /it/import-string-array-into-excel-worksheet/
aliases: [/import-string-array-into-worksheet/,/import-data/string-array/,/import/string-array/]
keywords: Import string array data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati array di stringhe in file Excel. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 40
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Importa array di stringhe nel foglio di lavoro Excel
---
Questo foglio di lavoro REST API `import string array data` in Excel.

La richiesta è una richiesta HTTP con contenuto multiparte (vedere[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multiparte contiene i dati ImportStringArrayOption e la seconda contiene un file di dati.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

I parametri importanti sono descritti nella tabella seguente:

**ImportStringArrayOption**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Prima fila| interno||
| Prima colonna| interno||
| È verticale| corda| vero/falso.|
| Dati|Corda[]||
| Foglio di lavoro di destinazione| corda| nome del foglio di lavoro di destinazione.|
| ÈInserimento| corda| vero/falso.|
| ImportDataType| corda|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fonte| FileSource| Indica la posizione del file di dati quando il parametro BatchData è null.|

**Esempio**

```xml

<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>

```

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
