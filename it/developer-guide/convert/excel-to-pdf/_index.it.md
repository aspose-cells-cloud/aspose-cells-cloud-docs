---
title: Excel al P.D
second_title: Aspose.Cells Cloud Documen
linktitle: Excel al P.D
type: docs
url: /it/convert/excel-to-pdf/
aliases: [/convert-excel-file-to-pdf-in-cloud/]
keywords: Convert excel files to pdf files
description: Aspose.Cells Cloud REST API supporta la conversione di file excel in file pdf. L'SDK supporta i tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 80
---
Questo REST API `saveas` file excel a PDF.

[POST /cells/{nome}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API consente di salvare il file MS Excel come file PDF con impostazioni aggiuntive e salvare il risultato nella memoria.

Questo REST API `convert` file excel a PDF.

[PUT /celle/converti](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)API consente di convertire il file MS Excel nel file PDF con impostazioni aggiuntive e di salvare il risultato nella risposta.

Questo REST API `export` file excel a PDF.

[OTTIENI /celle/{nome}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  )API consente di convertire il file MS Excel nel file PDF con impostazioni aggiuntive e di salvare il risultato nella risposta.

## RIPOSO API


|**API**|**Tipo**|**Descrizione**|**Collegamento spavaldo**|
|:- |:- |:- |:- |
|/celle/converti|METTERE|Converte la cartella di lavoro dal contenuto della richiesta in un formato|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/celle/{nome}|OTTENERE|Esporta la cartella di lavoro in un altro formato.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{nome}/saveAs|INVIARE|Esporta cartella di lavoro in formato|[PostDocumentoSalva con nome](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



 Questi[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PostDocumentoSalva con nome](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) Le API definiscono un'interfaccia di programmazione accessibile pubblicamente e ti consentono di eseguire interazioni REST direttamente da un browser web.

 Puoi usare**cURL** strumento da riga di comando per accedere facilmente ai servizi Web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate a Cloud API con cURL.




{{< tabs tabTotal="3" tabID="11" tabName11="Convert Workbook API" tabName12="Get Workbook format API" tabName13="Save  Workbook as format API" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}



```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}


```

{{< /tab >}}

{{< tab tabNum="13" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 



```

{{< /tab >}}

{{< /tabs >}}





## Famiglia di SDK cloud

 L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Si prega di controllare il[Deposito GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:


{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/
Aspose.Cells.Cloud.SDK.Api.CellsApi cellsApi = new CellsApi("your client id", "your client secret");
var response = cellsApi.CellsWorkbookPutConvertWorkbook( File.OpenRead(@".\TestData\datasource.xlsx"), "pdf", null, null);
Assert.IsInstanceOf<System.IO.Stream>(response, "response is System.IO.Stream");

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
try{
    CellsApi api = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    File response = api.cellsWorkbookPutConvertWorkbook(
        new File("TestData\\Book1.xlsx"), "pdf", null, null);
} catch (ApiException e) {
    e.printStackTrace();
}	

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
CellsAPI := NewCellsApiService(clientId, clientSecret)
args := new(CellsWorkbookPutConvertWorkbookOpts)
args.Format = "pdf"
file, err := os.Open("TestData\\Book1.xlsx")
if err != nil {
	return
}
localVarReturnValue, httpResponse, err := CellsAPI.CellsWorkbookPutConvertWorkbook(file, args)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\t TestCellsPutConvertWorkbook - %d\n", httpResponse.StatusCode)
}
```

{{< /tab >}}

{{< /tabs >}}
