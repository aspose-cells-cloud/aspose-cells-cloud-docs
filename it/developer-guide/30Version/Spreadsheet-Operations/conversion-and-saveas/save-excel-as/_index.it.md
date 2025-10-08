---
title: Salva con nome Eccedi
second_title: Documen
linktitle: Salva un
type: docs
url: /it/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API supporta il salvataggio di file Excel in diversi formati. L'SDK supporta diversi linguaggi di sviluppo, tra cui Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Salva con nome Excel
---
Questo REST API indica il file Excel `save` come file di formato diverso.

**Parametro percorso**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|nome|corda| Il nome del file.|

**Parametro di query**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|nuovo nomefile|corda| nuovo nome del file|
|isAutoFitRows|corda| Adatta automaticamente tutte le righe di questa cartella di lavoro. Il valore predefinito è false.|
|isAutoFitColumns|corda| Adatta automaticamente la larghezza delle colonne in questa cartella di lavoro. Il valore predefinito è false.|
|cartella|corda|Cartella della cartella di lavoro originale.|
|Nome di archiviazione|corda| Nome dell'archivio in cui si trova il file.|
|outStorageName|corda| Nome dell'archivio in cui si trova il file salvato.|
|checkExcelRestriction|bool| Se verificare la restrizione del file Excel quando l'utente modifica gli oggetti correlati alle celle.|
|regione|corda| Impostazioni regionali per la cartella di lavoro.|
|Adattamento pagina per foglio|bool| La pagina si adatta perfettamente al foglio di lavoro.|
|pageTallFitOnPerSheet|bool| La pagina è alta quanto il foglio di lavoro.|
|Nome foglio|corda| Converti il foglio di lavoro specificato.|
|indice della pagina|corda| Converti la pagina specificata del foglio di lavoro, sheetName è obbligatorio.|
|unaPaginaPerFoglio|bool| Nella conversione al formato PDF, una pagina per foglio.|

**Parametro del corpo della richiesta**

|Nome del parametro|Tipo|Descrizione|
|:- |:- |:- |
|Opzioni di salvataggio| Oggetto|Opzione di salvataggio per salvare nella seconda parte del contenuto multiparte.|

## RIPOSO API

|**API**|**Tipo**|**Descrizione**|**Link alla risorsa**|
|:- |:- |:- |:- |
|/cells/{name}/saveAs|INVIARE|Esporta cartella di lavoro in formato|[Salva con nome](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** Strumento da riga di comando per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "SaveResult": {
    "SourceDocument": {
      "Href": "test.xlsx",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "DestDocument": {
      "Href": "test.pdf",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "AdditionalItems": []
  },
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Famiglia Cloud SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}
