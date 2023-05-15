---
title: Importa i dati CSV nel foglio di lavoro Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importa dati csv
type: docs
url: /it/import/csv-data/
aliases: [/import-csv-data-into-excel-worksheet/, /import-csv-data-into-worksheet/,/import-data/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di dati csv in file Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 19
---
Questo REST API `import csv data` nel foglio di lavoro Excel.

La richiesta è una richiesta HTTP con contenuto in più parti (vedi[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto in più parti contiene i dati ImportCSVDataOption e la seconda contiene un file di dati.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

I parametri importanti sono descritti nella tabella seguente:


**ImportCSVDataOption**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| SeparatoreStringa| corda||
| ConvertNumericData| corda|vero falso.|
| Prima riga| int||
| Prima colonna| int||
| File sorgente| corda||
| CustomParser|Elenco<CustomParserConfig> ||


**CustomParserConfig**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| ColonnaIndice| int||
| ParseMethod| corda||
| Stile personalizzato| corda||

**Esempio**

```xml

 <ImportCSVDataOption>
     <DestinationWorksheet>Sheet1</DestinationWorksheet>
     <IsInsert>true</IsInsert>
     <ImportDataType>CSVData</ImportDataType>
     <SeparatorString>;</SeparatorString>
     <ConvertNumericData>true</ConvertNumericData>
     <FirstRow>1</FirstRow>
     <FirstColumn>2</FirstColumn>
     <SourceFile>TestImportDataCSV.csv</SourceFile>
     <CustomParsers>
         <CustomParserConfig>
             <ColumnIndex>0</ColumnIndex>
             <ParseMethod>ToString</ParseMethod>
             <CustomStyle>#</CustomStyle>
         </CustomParserConfig>
     </CustomParsers>
 </ImportCSVDataOption>

```

## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
