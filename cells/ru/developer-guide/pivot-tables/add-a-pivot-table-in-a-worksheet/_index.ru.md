---
title: Добавление сводной таблицы в рабочий лист Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Добавлять
type: docs
url: /ru/pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: Add a pivot table in an Excel worksheet
description: Aspose.Cells Cloud REST API поддерживает добавление сводной таблицы на рабочий лист Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 30
---
Этот REST API указывает на `add` сводную таблицу на листе.
 
## РСЕТ API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| имя листа| нить| путь| Имя рабочего листа.|
| запрос|| тело| CreatePivotTableRequest dto в теле запроса.|
| папка| нить| запрос| Папка документа.|
| имя_хранилища| нить| запрос| имя хранилища.|
| источник данных| нить| запрос| Данные для нового кэша сводной таблицы.|
| destCellName| нить| запрос| Ячейка в верхнем левом углу диапазона назначения отчета сводной таблицы.|
| имя_таблицы| нить| запрос| Имя нового отчета сводной таблицы.|
| использоватьSameSource| логический| запрос| Указывает, используется ли тот же источник данных, когда другая существующая сводная таблица использовала этот источник данных. Если свойство истинно, оно сэкономит память.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v  "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables"
-X PUT \
-d '{"Name":"MyPivot", "SourceData":"A5:E10", "DestCellName":"H20", "UseSameSource":true, "PivotFieldRows":[1], "PivotFieldColumns":[1], "PivotFieldData ":[1]}'\
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
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}
