---
title: Ottiene il file Excel in un altro formato
second_title: Documen
linktitle: Ottieni Exce
type: docs
url: /it/get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API supporta l'importazione di file Excel in diversi formati. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Ottiene il file Excel in altri formati
---
Questo REST API indica il file Excel `get` in un formato diverso.

**Parametro di query**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|formato|corda|Formato del file: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg e così via.|
|password|corda|La password necessaria per aprire un file Excel.|
|èAutoFit|corda|Adatta automaticamente la larghezza di righe e colonne in questa cartella di lavoro. Il valore predefinito è false.|
|soloSalvaTabella|corda|vero/falso|
|Percorso in uscita|corda| Percorso in cui salvare il risultato. Se si tratta di un singolo file, `outPath` dovrebbe includere sia il nome del file che l'estensione. Nel caso di più file, `outPath` dovrebbe includere solo la cartella.|
|outStorageName|corda| Nome dell'archivio in cui si trova il file salvato.|
|checkExcelRestriction|bool| Se verificare la restrizione del file Excel quando l'utente modifica gli oggetti correlati alle celle.|
|regione|corda| Impostazioni regionali per la cartella di lavoro.|
|Adattamento pagina per foglio|bool| La pagina si adatta perfettamente al foglio di lavoro.|
|pageTallFitOnPerSheet|bool| La pagina è alta quanto il foglio di lavoro.|
|unaPaginaPerFoglio|bool| Nella conversione al formato PDF, una pagina per foglio.|
|cartella|corda|Cartella della cartella di lavoro originale.|
|Nome di archiviazione|corda|Nome dell'archivio in cui si trova il file.|

## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Collegamento Swagger**|
|:- |:- |:- |:- |
|/cellule/{nome}|OTTENERE|Esporta la cartella di lavoro in un altro formato.|[Ottieni il libro di lavoro](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
