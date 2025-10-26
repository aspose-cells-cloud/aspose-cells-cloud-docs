---
title: Скрыть строки на листе Excel
second_title: Documen
linktitle: Спрятан
type: docs
url: /ru/rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: Hide rows on an Excel worksheet
description: Aspose.Cells Cloud REST API поддерживает скрытие строк на листе Excel. SDK поддерживает различные языки разработки, включая Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 40
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Скрыть строки на листе Excel
---
Этот REST API указывает на необходимость скрыть строки на листе Excel.

## РСЕT API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
 
```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название рабочей книги.|
| Имя_листа| нить| путь| Название рабочего листа.|
| стартров| целое число| запрос| Начальный индекс строки, подлежащей обработке.|
| totalRows| целое число| запрос| Количество обрабатываемых рядов.|
| папка| нить| запрос| Папка с документами.|
| имя_хранилища| нить| запрос| имя хранилища.|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
