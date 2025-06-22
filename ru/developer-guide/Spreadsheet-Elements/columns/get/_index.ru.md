---
title: Получить столбцы из рабочего листа Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /ru/columns/get/
aliases: [/get-columns-from-an-excel-worksheet/,/get-columns-from-a-worksheet/,/get-column-from-a-worksheet/]
keywords: Get columns on an Excel workshee
description: Aspose.Cells Cloud REST API поддерживает получение столбцов на листе Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 10
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Получение столбцов из рабочего листа Excel
---
Этот REST API указывает на чтение данных столбца рабочего листа по индексу столбца.

## РЕТ API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
 
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название рабочей книги.|
| Имя листа| нить| путь| Название рабочего листа.|
| columnIndex| целое число| путь| Индекс столбца.|
| папка| нить| запрос| Папка с рабочей тетрадью.|
| имя_хранилища| нить| запрос| имя хранилища.|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

 Вы можете использовать**cURL** Инструмент командной строки для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash

{
"Column": {
  "GroupLevel": 0,
  "Index": 10,
  "IsHidden": false,
  "Width": 8.5,
  "Style": {
    "link": {
      "Href": "/style",
      "Rel": "self"
    }
  },
  "link": {
    "Href": "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
    "Rel": "self"
  }
},
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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
