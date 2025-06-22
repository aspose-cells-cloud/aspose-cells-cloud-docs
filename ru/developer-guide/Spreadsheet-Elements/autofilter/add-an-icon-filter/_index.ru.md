---
title: Добавьте фильтр значков на рабочий лист Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Добавить фильтр значков
type: docs
url: /ru/autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: Adds an icon filter on an Excel worksheet
description: Облако Aspose.Cells API поддерживает добавление фильтра значков на лист Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 65
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Добавить фильтр значков на рабочий лист Excel
---
Этот REST API указывает на добавление `icon filter` на рабочий лист Excel.

## РЕТ API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter

```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| Путь| Название рабочей книги.|
| Имя листа| нить| Путь| Название рабочего листа.|
|диапазон|нить| Запрос||
|fieldIndex|целое число| Запрос||
|iconSetType|нить| Запрос| Стрелки3/СтрелкиСерые3/Флаги3/Знаки3/Символы3/Символы32/Светофор31/Светофор32/Стрелки4/СтрелкиСерые4/Рейтинг4/От красного до черного4/Светофор4/Стрелки5/СтрелкиСерые5/Кварталы5/Рейтинг5/Звезды3/Коробки5/Треугольники3/Нет/Пользовательский набор/Смайлы3/Цветные смайлы3|
|iconId|целое число| Запрос||
|матчБланки|нить| Запрос|правда/ложь|
|обновить|нить| Запрос|правда/ложь|
|папка|нить| Запрос|Оригинальная папка рабочей тетради.|
|имя_хранилища| Запрос|нить|Имя хранилища.|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldIndex=0&iconSetType=ArrowsGray3&iconId=1" \
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

 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
