---
title:  Сортировка по диапазону
second_title: Aspose.Cells Cloud Documen
linktitle: Сор
type: docs
keywords: Range Sort
url: /ru/ranges/sort/
description:  Устанавливает границу контура вокруг диапазона ячеек.
weight: 20
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Сортировка по диапазону
---
Этот REST API указывает на сортировку по диапазону.

## РЕТ API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя|Нить|Путь|Название рабочей книги.|
|Имя листа|Нить|Путь|Название рабочего листа.|
|диапазонОперировать|Сорт|Тело| Запрос на сортировку диапазона|
|папка|Нить|Запрос|Оригинальная папка рабочей тетради.|
|имя_хранилища|Нить|Запрос|Имя хранилища.|

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```powershell

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с репозиторием GitHub для получения полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeSort.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeSort.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeSort.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeSort.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeSort.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeSort.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeSort.go" >}}

{{< /tab >}}

{{< /tabs >}}
