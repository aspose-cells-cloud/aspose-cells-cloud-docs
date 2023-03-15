---
title: Получает файл Excel в другой формат
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /ru/export-different-formats/
aliases: [/export-excel-workbook-to-different-file-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API поддерживает преобразование файлов Excel в различные форматы файлов. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 10
---
Этот REST API указывает на файл excel `get` в файл другого формата.


**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|формат|нить| формат файла (csv/xls/html/mhtml/ods/pdf/xml/txt/tiff/xlsb/xlsm/xlsx/xltm/xltx/xps/png/jpg/gif/emf/bmp/md/числа/wmf/svg )|
|пароль|нить||
|isAutoFit|нить|правда/ложь|
|толькоСохранитьТаблицу|нить|правда/ложь|
|выходной путь|нить|новая позиция в файле.|
|папка|нить|Оригинальная папка с рабочей тетрадью.|
|имя_хранилища|нить|Имя хранилища.|



## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Свэггер Ссылка**|
|:- |:- |:- |:- |
|/ячейки/{имя}|ПОЛУЧАТЬ|Экспорт книги в другой формат.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

 Вы можете использовать**cURL** инструмент командной строки для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.


{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.


{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/
Aspose.Cells.Cloud.SDK.Api.LiteCellsApi liteCellsApi = new Aspose.Cells.Cloud.SDK.Api.LiteCellsApi("your client id", "your client secret");
IDictionary<string, Stream> mapFiles = new Dictionary<string, Stream>();
mapFiles.Add("assemblytest.xlsx", File.OpenRead(@".\TestData\assemblytest.xlsx"));
mapFiles.Add("datasource.xlsx", File.OpenRead(@".\TestData\datasource.xlsx"));
Aspose.Cells.Cloud.SDK.Model.FilesResult filesResult = liteCellsApi.PostExport(files, "Workbook", "pdf");
Assert.IsNotNull(filesResult);


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
    FilesResult response = liteApi.postExport(fileMap, "workbook","pdf");
} catch (ApiException e) {
    e.printStackTrace();
}		

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go
// For complete examples and data files, please go to https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/
LiteCellsAPI := NewLiteCellsApiService(clientId, clientSecret)

var fileMap map[string]string
fileMap = make(map[string]string)
fileMap["Book1.xlsx"] = "TestData\\Book1.xlsx"
fileMap["Book2.xlsx"] = "TestData\\Book2.xlsx"
postOpts := new(PostExportOpts)
postOpts.Format = "pdf"
postOpts.ObjectType = "workbook"
_, httpResponse, err := LiteCellsAPI.PostExport(fileMap, postOpts)
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
