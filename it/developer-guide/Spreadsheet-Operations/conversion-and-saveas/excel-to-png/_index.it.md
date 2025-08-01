﻿---
title: Excel a PN
second_title: Aspose.Cells Cloud Documen
linktitle: Excel a PN
type: docs
url: /itconvert-excel-file-to-png-file/
keywords: Convert excel files to png files
description: Aspose.Cells Cloud REST API supporta la conversione di file Excel in file CSV. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 90
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Excel in CSV
---
Questo REST API indica a `convert` un file di foglio di calcolo in un file in formato png.

**Parametro di query**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|password|corda| La password necessaria per aprire il file Excel.|
|Nome di archiviazione|corda| Nome dell'archivio in cui si trova il file.|
|checkExcelRestriction|bool| Se verificare la restrizione del file Excel quando l'utente modifica celle con oggetti correlati.|

**Parametro del corpo della richiesta**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|file di dati| file di dati|Il file di dati viene salvato nella prima parte del contenuto multiparte.|

**Risposta**

[Informazioni sul file](/cells/it/file-info/)

## Specifiche REST API

|**API**|**Tipo**|**Descrizione**|**Collegamento Swagger**|
|:- |:- |:- |:- |
|/cellule/converti/png|INVIARE|Converti un foglio di calcolo in un file png.|[PostConvertWorkbookToPNG](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG)|

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Altre API implementano questa funzione

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)API consente di salvare il file MS Excel come file CSV con impostazioni aggiuntive e di salvare il risultato nell'archivio.

Questo file Excel REST API `convert` in CSV.

[METTI /celle/converti](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API consente di convertire il file MS Excel in un file CSV con impostazioni aggiuntive e di salvare il risultato nella risposta.

Questo file Excel REST API `export` in CSV.

[GET /cells/{nome}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API consente di convertire il file MS Excel in un file CSV con impostazioni aggiuntive e di salvare il risultato nella risposta.
