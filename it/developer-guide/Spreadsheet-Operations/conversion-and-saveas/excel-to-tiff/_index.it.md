---
title: Excel a TIF
second_title: Aspose.Cells Cloud Documen
linketitle: Excel to Tif
type: docs
url: /it/convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/,/convert/excel-to-tiff/]
keywords: Convert excel files to tiff files
description: Aspose.Cells Cloud REST API supporta la conversione di file Excel in file TIFF. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 90
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, da Excel a TIFF
---
Questo file Excel REST API `saveas` in TIFF.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API consente di salvare il file MS Excel come file TIFF con impostazioni aggiuntive e di salvare il risultato nella memoria.

Questo file Excel REST API `convert` in TIFF.

[METTI /celle/converti](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API consente di convertire il file MS Excel nel file TIFF con impostazioni aggiuntive e di salvare il risultato nella risposta.

Questo file Excel REST API `export` in TIFF.

[GET /cells/{nome}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API consente di convertire il file MS Excel nel file TIFF con impostazioni aggiuntive e di salvare il risultato nella risposta.

## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Collegamento Swagger**|
|:- |:- |:- |:- |
|/cellule/converti|METTERE|Converte la cartella di lavoro dal contenuto della richiesta in un formato specifico|[MettiConvertiCartellaLavoro](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/cellule/{nome}|OTTENERE|Esporta la cartella di lavoro in un altro formato.|[Ottieni il libro di lavoro](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{name}/saveAs|INVIARE|Esporta cartella di lavoro in formato|[Salva con nome PostDocument](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

Queste API definiscono un'interfaccia di programmazione accessibile al pubblico e consentono di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
-X POST \
-d "{'SaveFormat':'tiff', 'ImageFormat': 'tiff'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'tiff', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}
{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}
