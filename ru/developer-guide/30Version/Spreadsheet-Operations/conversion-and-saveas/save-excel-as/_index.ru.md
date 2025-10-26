---
title: Сохранить как Exce
second_title: Documen
linktitle: Сохранить
type: docs
url: /ru/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API поддерживает сохранение файлов Excel в различных форматах. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 30
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Сохранить как Excel
---
Этот REST API указывает на файл Excel `save` как на файл другого формата.

**Параметр пути**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|имя|нить| Имя файла.|

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|новое имя_файла|нить| новое имя файла|
|isAutoFitRows|нить| Автоматически подгоняет все строки в этой книге. Значение по умолчанию — false.|
|isAutoFitColumns|нить| Автоматически подбирает ширину столбцов в этой книге. Значение по умолчанию — false.|
|папка|нить|Оригинальная папка рабочей тетради.|
|имя_хранилища|нить| Имя хранилища, где находится файл.|
|outStorageName|нить| Имя хранилища, где находится сохраненный файл.|
|checkExcelRestriction|бул| Проверять ли ограничения файла Excel, когда пользователь изменяет ячейки, связанные с объектами.|
|область|нить| Региональные настройки для рабочей книги.|
|pageWideFitOnPerSheet|бул| Ширина страницы соответствует размеру листа.|
|pageTallFitOnPerSheet|бул| Страница по высоте умещается на рабочем листе.|
|Имя_листа|нить| Преобразовать указанный рабочий лист.|
|pageIndex|нить| Преобразовать указанную страницу рабочего листа, обязательно sheetName.|
|одна страница на листе|бул| При конвертации в формат PDF — одна страница на листе.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|SaveOptions| Объект|Параметр «Сохранить» сохраняет во второй части многочастного контента.|

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Ссылка на ресурс**|
|:- |:- |:- |:- |
|/cells/{name}/saveAs|ПОЧТА|Экспортировать книгу в формат|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

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

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK берёт на себя решение низкоуровневых задач и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

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
