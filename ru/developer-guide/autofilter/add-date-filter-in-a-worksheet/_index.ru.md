﻿---
title: Добавить фильтр даты в рабочую таблицу Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Добавить фильтр даты
type: docs
url: /ru/autofilter/add-date-filter/
aliases: [/add-date-filter-in-a-worksheet/,/autofilter/add-a-date-filter/]
keywords: Adds a date filter on an Excel worksheet
description: Облако Aspose.Cells API поддерживает добавление фильтра даты на рабочий лист Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 65
---
Этот REST API указывает на добавление `date filter` на рабочий лист Excel.

## РСЕТ API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter

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


[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-AddDataFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-AddDateWorksheetExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-PutWorksheetDateFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_date_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-AddDateFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddDateWorksheetExample-1.java" >}}



{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-AddDateFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "54cd61aee4496583dfacaf7dadef6463" >}}

{{< /tab >}}

{{< /tabs >}}
