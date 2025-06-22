---
title: Удалить все сводные таблицы на листе Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Прозрачный
type: docs
url: /ru/pivot-tables/clear/
aliases: [/delete-worksheet-pivot-tables/]
keywords: Delete all pivot tables in an Excel worksheet
description: Aspose.Cells Cloud REST API поддерживает удаление всех сводных таблиц на листе Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 80
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Удалить все сводные таблицы на листе Excel
---
Этот REST API указывает на удаление сводных таблиц рабочего листа
 
## РЕТ API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| Имя листа| нить| путь| Название рабочего листа.|
| папка| нить| запрос| Папка документов.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTables) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
-X DELETE \
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
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
 
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTable-delete-worksheet-pivot-table.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTables.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTable-delete-worksheet-pivot-table.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "12f056c6733b4961979d35a32ef99e61" >}}

{{< /tab >}}

{{< /tabs >}}
