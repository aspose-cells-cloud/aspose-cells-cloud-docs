---
title: Excel an PD
second_title: Aspose.Cells Cloud Documen
linktitle: Excel an PD
type: docs
url: /de/convert/excel-to-pdf/
aliases: [/convert-excel-file-to-pdf-in-cloud/]
keywords: Convert excel files to pdf files
description: Aspose.Cells Cloud REST API unterstützt die Konvertierung von Excel-Dateien in PDF-Dateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 80
---
Diese REST API `saveas` Excel-Datei an PDF.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) Mit API können Sie die MS Excel-Datei als PDF-Datei mit zusätzlichen Einstellungen speichern und das Ergebnis im Speicher speichern.

Diese REST API `convert` Excel-Datei an PDF.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)Mit API können Sie die MS Excel-Datei mit zusätzlichen Einstellungen in die PDF-Datei konvertieren und das Ergebnis in der Antwort speichern.

Diese REST API `export` Excel-Datei an PDF.

[GET /cells/{Name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  )Mit API können Sie die MS Excel-Datei mit zusätzlichen Einstellungen in die PDF-Datei konvertieren und das Ergebnis in der Antwort speichern.

## REST API


|**API**|**Typ**|**Beschreibung**|**Swagger-Link**|
|:- |:- |:- |:- |
|/Zellen/konvert|SETZEN|Konvertiert eine Arbeitsmappe aus Anforderungsinhalten in ein bestimmtes Format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/Zellen/{Name}|ERHALTEN|Exportiert die Arbeitsmappe in ein anderes Format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{Name}/saveAs|POST|Exportieren Sie die Arbeitsmappe in das Format|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



 Diese[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook), [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) APIs definieren eine öffentlich zugängliche Programmierschnittstelle und ermöglichen es Ihnen, REST-Interaktionen direkt von einem Webbrowser aus auszuführen.

 Sie können verwenden**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.




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





## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:


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
