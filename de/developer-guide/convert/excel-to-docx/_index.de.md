---
title: Excel an Dok
second_title: Aspose.Cells Cloud Documen
linktitle: Excel an Dok
type: docs
url: /de/convert/excel-to-docx/
aliases: [/convert-excel-file-to-docx-in-cloud/]
keywords: Convert excel files to docx files
description: Aspose.Cells Cloud REST API unterstützt die Konvertierung von Excel-Dateien in docx-Dateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 90
---
Diese REST API `saveas` Excel-Datei in Docx.

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) Mit API können Sie die MS Excel-Datei als Docx-Datei mit zusätzlichen Einstellungen speichern und das Ergebnis im Speicher speichern.

Diese REST API `convert` Excel-Datei in Docx.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) Mit API können Sie die MS Excel-Datei mit zusätzlichen Einstellungen in eine Docx-Datei konvertieren und das Ergebnis in der Antwort speichern.

Diese REST API `export` Excel-Datei in Docx.

[GET /cells/{Name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) Mit API können Sie die MS Excel-Datei mit zusätzlichen Einstellungen in eine Docx-Datei konvertieren und das Ergebnis in der Antwort speichern.

## REST API

|**API**|**Typ**|**Beschreibung**|**Swagger-Link**|
|:- |:- |:- |:- |
|/Zellen/konvert|SETZEN|Konvertiert eine Arbeitsmappe aus Anforderungsinhalten in ein bestimmtes Format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/Zellen/{Name}|ERHALTEN|Exportiert die Arbeitsmappe in ein anderes Format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{Name}/saveAs|POST|Exportieren Sie die Arbeitsmappe in das Format|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



Diese APIs definieren eine öffentlich zugängliche Programmierschnittstelle und ermöglichen es Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

 Sie können verwenden**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.


{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=docx" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.docx" \
-X POST \
-d "{'SaveFormat':'docx', 'ImageFormat': 'docx'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'docx', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


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
var response = cellsApi.CellsWorkbookPutConvertWorkbook( File.OpenRead(@".\TestData\datasource.xlsx"), "docx", null, null);
Assert.IsInstanceOf<System.IO.Stream>(response, "response is System.IO.Stream");

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
try{
    LiteCellsApi liteApi = new LiteCellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    String AssemblyTestXlsx = "assemblytest.xlsx";
    String DataSourceXlsx = "datasource.xlsx";
    HashMap<String,File> fileMap = new HashMap<String,File>();
    fileMap.put(AssemblyTestXlsx , new File("TestData\\" + AssemblyTestXlsx));
    fileMap.put(DataSourceXlsx , new File("TestData\\" + DataSourceXlsx) );
    FilesResult response = liteApi.postExport(fileMap, "workbook","docx");
} catch (ApiException e) {
    e.printStackTrace();
}		

//2. solution
try{
    CellsApi api = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    File response = api.cellsWorkbookPutConvertWorkbook(
        new File("TestData\\Book1.xlsx"), "docx", null, null);
} catch (ApiException e) {
    e.printStackTrace();
}	

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go

LiteCellsAPI := NewLiteCellsApiService(clientId, clientSecret)

var fileMap map[string]string
fileMap = make(map[string]string)
fileMap["Book1.xlsx"] = "TestData\\Book1.xlsx"
fileMap["Book2.xlsx"] = "TestData\\Book2.xlsx"
postOpts := new(PostExportOpts)
postOpts.Format = "docx"
postOpts.ObjectType = "workbook"
_, httpResponse, err := LiteCellsAPI.PostExport(fileMap, postOpts)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\tTestCellsPostExport \n")
}

CellsAPI := NewCellsApiService(clientId, clientSecret)
args := new(CellsWorkbookPutConvertWorkbookOpts)
args.Format = "docx"
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
