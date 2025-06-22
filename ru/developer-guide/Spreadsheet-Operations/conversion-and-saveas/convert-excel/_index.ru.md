---
title: Конвертировать файл Excel в другой формат
second_title: Aspose.Cells Cloud Documen
linktitle: Конвертировать Excel
type: docs
url: /ru/convert-an-excel-file-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/,/convert/excel-to-different-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API поддерживает преобразование файлов Excel в различные форматы файлов. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 10
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Преобразование Excel
---
Этот REST API указывает на файл Excel `convert` в другом формате.

Запрос представляет собой HTTP-запрос с составным содержимым (см.[Запрос на изменение 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит файл данных, а вторая — параметры сохранения.

**Параметр запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|формат|нить|Формат файла: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg и т. д.|
|пароль|нить| Пароль, необходимый для открытия файла Excel.|
|outPath|нить| Путь для сохранения результата. Если это один файл, `outPath` должен включать как имя файла, так и расширение. В случае нескольких файлов `outPath` должен включать только папку.|
|имя_хранилища|нить| Имя хранилища, где находится файл.|
|checkExcelОграничение|бул| Проверять ли ограничения файла Excel, когда пользователь изменяет объекты, связанные с ячейками.|
|streamFormat|нить| Формат входного файлового потока.|
|область|нить| Региональные настройки для рабочей книги.|
|pageWideFitOnPerSheet|бул| Ширина страницы соответствует размеру рабочего листа.|
|страницаВысокийПоместитьсяНаНаЛисте|бул| Страница по высоте умещается на рабочем листе.|
|Имя листа|нить| Преобразовать указанный рабочий лист.|
|pageIndex|нить|Преобразовать указанную страницу рабочего листа, требуется sheetName.|
|одна страница на листе|бул| При конвертации в формат PDF — по одной странице на листе.|
|AutoRowsFit|бул| Автоматически подгоняет все строки в этой книге.|
|AutoColumnsFit|бул| Автоматически подгоняет ширину столбцов в этой книге.|

**Параметр тела запроса**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
|файл данных| файл данных|Файл данных сохраняется в первой части многокомпонентного контента.|
|СохранитьПараметры| Объект|Опция сохранения сохраняет во второй части многокомпонентного контента.|

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Ссылка Swagger**|
|:- |:- |:- |:- |
|/ячейки/преобразовать|ПОМЕЩАТЬ|Конвертирует рабочую книгу из содержимого запроса в некоторый формат|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
