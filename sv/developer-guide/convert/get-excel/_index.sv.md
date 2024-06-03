---
title: Hämtar Excel fil till annat format
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /sv/export-different-formats/
aliases: [/export-excel-workbook-to-different-file-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API-stöd få excel-filer till olika formatfiler. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 10
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Får Excel fil till andra format
---
Denna REST API indikerar till `get` excel-fil till annan filformat.


**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|formatera|sträng| filformat(csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/Numbers/wmf/svg )|
|Lösenord|sträng||
|är AutoFit|sträng|sant falskt|
|endastSparatabell|sträng|sant falskt|
|outPath|sträng|ny filposition.|
|mapp|sträng|Original arbetsboksmapp.|
|lagringsnamn|sträng|Lagringsnamn.|



## REST API

|**API**|**Typ**|**Beskrivning**|**Swagger Link**|
|:- |:- |:- |:- |
|/celler/{namn}|SKAFFA SIG|Exporterar arbetsbok till annat format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|


 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL**kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.


{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
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
Aspose.Cells.Cloud.SDK.Api.LightCellsApi LightCellsApi = new Aspose.Cells.Cloud.SDK.Api.LightCellsApi("your client id", "your client secret");
IDictionary<string, Stream> mapFiles = new Dictionary<string, Stream>();
mapFiles.Add("assemblytest.xlsx", File.OpenRead(@".\TestData\assemblytest.xlsx"));
mapFiles.Add("datasource.xlsx", File.OpenRead(@".\TestData\datasource.xlsx"));
Aspose.Cells.Cloud.SDK.Model.FilesResult filesResult = LightCellsApi.PostExport(files, "Workbook", "pdf");
Assert.IsNotNull(filesResult);


```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/
try{
    LightCellsApi liteApi = new LightCellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    String AssemblyTestXlsx = "assemblytest.xlsx";
    String DataSourceXlsx = "datasource.xlsx";
    HashMap<String,File> fileMap = new HashMap<String,File>();
    fileMap.put(AssemblyTestXlsx , new File("TestData\\" + AssemblyTestXlsx));
    fileMap.put(DataSourceXlsx , new File("TestData\\" + DataSourceXlsx) );
    FilesResult response = liteApi.postExport(fileMap, "workbook","pdf");
} catch (ApiException e) {
    e.printStackTrace();
}		

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
LightCellsAPI := NewLightCellsApiService(clientId, clientSecret)

var fileMap map[string]string
fileMap = make(map[string]string)
fileMap["Book1.xlsx"] = "TestData\\Book1.xlsx"
fileMap["Book2.xlsx"] = "TestData\\Book2.xlsx"
postOpts := new(PostExportOpts)
postOpts.Format = "pdf"
postOpts.ObjectType = "workbook"
_, httpResponse, err := LightCellsAPI.PostExport(fileMap, postOpts)
if err != nil {
	t.Error(err)
} else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
	t.Fail()
} else {
	fmt.Printf("\tTestCellsPostExport \n")
}


```

{{< /tab >}}

{{< /tabs >}}
