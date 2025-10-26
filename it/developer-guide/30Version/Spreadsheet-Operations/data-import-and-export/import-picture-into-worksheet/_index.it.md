---
title: Importa immagine nel foglio di lavoro Excel
second_title: Documen
linktitle: Importa immagine
type: docs
url: /it/import-picture-into-excel-worksheet/
aliases: [/import-picture-into-worksheet/,/import-data/picture/, /import/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di immagini in file Excel. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 19
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Importa immagine nel foglio di lavoro Excel
---
Questo foglio di lavoro REST API `import picture data` in Excel.

La richiesta è una richiesta HTTP con contenuto multiparte (vedere[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multiparte contiene i dati ImportPictureOption e la seconda contiene un file di dati.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

I parametri importanti sono descritti nella seguente tabella:

**OpzioneImportaImmagine**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
| Riga superiore sinistra| interno||
| Colonna in alto a sinistra| interno||
| Riga inferiore destra| interno||
| Colonna inferiore destra| interno||
| Nome del file| corda||
| Dati| Corda||
|Foglio di lavoro sulla destinazione| corda| nome del foglio di lavoro di destinazione.|
| ÈInserisci| corda| vero/falso.|
| ImportDataType| corda|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Fonte| FileSource| Indica la posizione del file di dati quando il parametro BatchData è null.|

**Esempio**

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

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

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
