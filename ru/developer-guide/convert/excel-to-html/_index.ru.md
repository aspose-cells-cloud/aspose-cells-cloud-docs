﻿---
title: Excel в HTM
second_title: Aspose.Cells Cloud Documen
linktitle: Excel в HTM
type: docs
url: /ru/convert/excel-to-html/
aliases: [/convert-excel-file-to-html-in-cloud/]
keywords: Convert excel files to html files
description: Aspose.Cells Cloud REST API поддерживает преобразование файлов Excel в файлы html. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 100
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, от Excel до HTML
---
Этот файл Excel REST API `saveas` имеет номер HTML.

[POST/cells/{имя}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API позволяет сохранить файл MS Excel как файл HTML с дополнительными настройками и сохранить результат в хранилище.

Этот файл Excel REST API `convert` имеет номер HTML.

[PUT/ячейки/конвертировать](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API позволяет конвертировать файл MS Excel в файл HTML с дополнительными настройками и сохранять результат в ответ.

Этот файл Excel REST API `export` имеет номер HTML.

[ПОЛУЧИТЬ /cells/{имя}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API позволяет конвертировать файл MS Excel в файл HTML с дополнительными настройками и сохранять результат в ответ.

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Сваггер Ссылка**|
|:- |:- |:- |:- |
|/ячейки/конвертировать|ПОМЕЩАТЬ|Преобразует книгу из содержимого запроса в некоторый формат.|[ПоложитьКонвертироватьWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/cells/{имя}|ПОЛУЧАТЬ|Экспортирует книгу в другой формат.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{имя}/saveAs|ПОЧТА|Экспортировать книгу в формат|[ОпубликоватьДокументСохранить как](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|



Эти API определяют общедоступный программный интерфейс и позволяют выполнять взаимодействие с REST непосредственно из веб-браузера.

 Вы можете использовать**cURL**инструмент командной строки для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.


{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.html" \
-X POST \
-d "{'SaveFormat':'html', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'html', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}
{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:


{{< tabs tabTotal="3" tabID="3" tabName1="C#" tabName2="Java" tabName3="Go" >}}

{{< tab tabNum="1" >}}

```csharp

Aspose.Cells.Cloud.SDK.Api.CellsApi cellsApi = new CellsApi("your client id", "your client secret");
var response = cellsApi.CellsWorkbookPutConvertWorkbook( File.OpenRead(@".\TestData\datasource.xlsx"), "html", null, null);
Assert.IsInstanceOf<System.IO.Stream>(response, "response is System.IO.Stream");

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

try{
    CellsApi api = new CellsApi(System.getenv("CellsCloudTestClientId"),System.getenv("CellsCloudTestClientSecret"));
    File response = api.cellsWorkbookPutConvertWorkbook(
        new File("TestData\\Book1.xlsx"), "html", null, null);
} catch (ApiException e) {
    e.printStackTrace();
}	

```
{{< /tab >}}

{{< tab tabNum="3" >}}

```go

CellsAPI := NewCellsApiService(clientId, clientSecret)
args := new(CellsWorkbookPutConvertWorkbookOpts)
args.Format = "html"
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
