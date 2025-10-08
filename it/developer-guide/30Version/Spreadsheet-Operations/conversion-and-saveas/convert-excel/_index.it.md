---
title: Convertire un file Excel in un formato diverso
second_title: Documen
linktitle: Converti Excel
type: docs
url: /it/convert-an-excel-file-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/,/convert/excel-to-different-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API supporta la conversione di file Excel in diversi formati di file. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Converti Excel
---
Questo REST API indica il file Excel `convert` in un formato diverso.

La richiesta è una richiesta HTTP con contenuto multiparte (vedere[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)O[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multiparte contiene il file di dati e la seconda contiene le opzioni di salvataggio.

**Parametro di query**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|formato|corda| Formato del file: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg e così via.|
|password|corda| La password necessaria per aprire un file Excel.|
|Percorso in uscita|corda| Percorso in cui salvare il risultato. Se si tratta di un singolo file, `outPath` dovrebbe includere sia il nome del file che l'estensione. Nel caso di più file, `outPath` dovrebbe includere solo la cartella.|
|Nome di archiviazione|corda| Nome dell'archivio in cui si trova il file.|
|checkExcelRestriction|bool| Se verificare la restrizione del file Excel quando l'utente modifica gli oggetti correlati alle celle.|
|formato di flusso|corda| Formato del flusso di file di input.|
|regione|corda| Impostazioni regionali per la cartella di lavoro.|
|Adattamento pagina per foglio|bool| La pagina si adatta perfettamente al foglio di lavoro.|
|pageTallFitOnPerSheet|bool| La pagina è alta quanto il foglio di lavoro.|
|Nome foglio|corda| Converti il foglio di lavoro specificato.|
|indice della pagina|corda| Converti la pagina specificata del foglio di lavoro, sheetName è obbligatorio.|
|unaPaginaPerFoglio|bool| Nella conversione al formato PDF, una pagina per foglio.|
|AutoRowsFit|bool| Adatta automaticamente tutte le righe in questa cartella di lavoro.|
|AutoColumnsFit|bool| Adatta automaticamente la larghezza delle colonne in questa cartella di lavoro.|

**Parametro del corpo della richiesta**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|file di dati| file di dati|Il file di dati viene salvato nella prima parte del contenuto multiparte.|
|Opzioni di salvataggio| Oggetto|Opzione di salvataggio per salvare nella seconda parte del contenuto multiparte.|

## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Collegamento Swagger**|
|:- |:- |:- |:- |
|/cellule/converti|METTERE|Converte la cartella di lavoro dal contenuto della richiesta in un formato specifico|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
