---
title: Удалить фильтр в рабочей таблице Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Удалить фильтр
type: docs
url: /ru/delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/,/delete-auto-filter/]
keywords: Deletes a filter on an Excel worksheet
description: Облако Aspose.Cells API поддерживает удаление фильтра на листе Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 100
---
Этот REST API указывает на удаление `filter` на рабочем листе Excel.

## РСЕТ API

```bash

DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter

```

Параметры запроса:
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| Путь|Имя рабочей книги.|
| имя листа| нить| Путь| Имя рабочего листа.|
|диапазон|нить| Запрос||
|индекс поля|целое число| Запрос||
|dateTimeGroupingType|нить| Запрос| День/час/минута/месяц/секунда/год|
|год|целое число| Запрос||
|месяц|целое число| Запрос||
|день|целое число| Запрос||
|час|целое число| Запрос||
|минута|целое число| Запрос||
|второй|целое число| Запрос||
|matchBlanks|нить| Запрос|правда/ложь|
|обновить|нить| Запрос|правда/ложь|
|папка|нить| Запрос|Оригинальная папка с рабочей тетрадью.|
|имя_хранилища|нить| Запрос|Имя хранилища.|

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&criteria=Year" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}


## Семейство облачных SDK

 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-DeleteFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-DeleteFilterForFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-DeleteWorksheetFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-delete_worksheet_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-DeleteFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-DeleteFilterForFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-DeleteFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4e5d4702f8c09698ab20c1a577b259c9" >}}

{{< /tab >}}

{{< /tabs >}}
