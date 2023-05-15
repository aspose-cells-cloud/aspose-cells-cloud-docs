---
title: Excel till PD
second_title: Aspose.Cells Cloud Documen
linktitle: Excel till PD
type: docs
url: /sv/convert/excel-to-pdf/
aliases: [/convert-excel-file-to-pdf-in-cloud/]
keywords: Convert excel files to pdf files
description: Aspose.Cells Cloud REST API stöder konvertering av Excel-filer till pdf-filer. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 80
---
Denna REST API `saveas` excel-fil till PDF.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API låter dig spara MS Excel-filen som PDF-fil med ytterligare inställningar och spara resultatet i lagringen.

Denna REST API `convert` excel-fil till PDF.

[PUT /celler/konvertera](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)API låter dig konvertera MS Excel-filen till PDF-fil med ytterligare inställningar och spara resultatet i svaret.

Denna REST API `export` excel-fil till PDF.

[HÄMTA /celler/{namn}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  )API låter dig konvertera MS Excel-filen till PDF-fil med ytterligare inställningar och spara resultatet i svaret.

## REST API


|**API**|**Typ**|**Beskrivning**|**Swagger Link**|
|:- |:- |:- |:- |
|/celler/konvertera|SÄTTA|Konverterar arbetsbok från begäran om innehåll till något format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/celler/{namn}|SKAFFA SIG|Exporterar arbetsbok till annat format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{name}/saveAs|POSTA|Exportera arbetsbok till format|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



 Dessa[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API:er definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.




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





## Cloud SDK-familj

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:


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
