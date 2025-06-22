---
title: Добавить диаграмму на рабочий лист
type: docs
url: /ru/charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Добавить диаграмму на рабочий лист
---
Этот REST API указывает на добавление новой диаграммы на рабочий лист.
 
## РЕТ API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название рабочей тетради.|
| Имя листа| нить| путь| Название рабочего листа.|
| Тип диаграммы| нить| запрос| Тип диаграммы см. в свойстве Тип в ресурсе диаграммы.|
| верхний левый ряд| целое число| запрос|0 |
| верхняя левая колонка| целое число| запрос|0 |
| нижняя правая строка| целое число| запрос|0 |
| нижняя правая колонка| целое число| запрос|0 |
| область| нить| запрос| Указывает значения, на основе которых строится ряд данных.|
| isVertical| булев| запрос| Истинный|
| категорияДанные| нить| запрос|Получает или задает диапазон значений оси категории. Это может быть диапазон ячеек (например, "d1:e10").|
| isAutoGetSerialName| булев| запрос| Истинный|
| заголовок| нить| запрос| Указывает название диаграммы.|
| папка| нить| запрос| Папка с рабочей тетрадью.|
| имя_хранилища| нить| запрос| имя хранилища.|
| данныеМетки| булев| запрос| Истинный|
| данныеМеткиПозиция| нить| запрос| Выше|
| pivotТаблицаЛист| нить| запрос||
| pivotTableName| нить| запрос||
 
 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.


{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl  -v "http://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" 
-X PUT
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "Code": "200",

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}
