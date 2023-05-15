---
title: Importa immagine in Excel Workshee
second_title: Aspose.Cells Cloud Documen
linktitle: Importa foto
type: docs
url: /it/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API supporta l'importazione di immagini in file Excel. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 19
---
Questo REST API `import picture data` nel foglio di lavoro Excel.

La richiesta è una richiesta HTTP con contenuto in più parti (vedi[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multipart contiene i dati ImportPictureOption e la seconda contiene un file di dati.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


I parametri importanti sono descritti nella tabella seguente:


**ImportPictureOption**

|Nome parametro|Tipo|Descrizione|
|:- |:- |:- |
| UpperLeftRow| int||
|Colonna superiore sinistra| int||
| LowerRightRow| int||
| Colonna in basso a destra| int||
| Nome del file| corda||
| Dati| Corda||
| Foglio di lavoro di destinazione| corda| nome del foglio di lavoro di destinazione.|
| IsInsert| corda| vero falso.|
| Tipo di dati di importazione| corda|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Fonte| FileSource| Indica la posizione del file di dati quando il parametro BatchData è nullo.|


**Esempio**


## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

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

