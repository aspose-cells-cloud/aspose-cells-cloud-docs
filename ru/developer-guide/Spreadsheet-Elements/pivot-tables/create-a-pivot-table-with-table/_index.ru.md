---
title: Преобразовать таблицу в сводную таблицу
second_title: Aspose.Cells Cloud Documen
linktitle: Конвертировать
type: docs
url: /ru/pivot-tables/convert-table-to-pivottable/
aliases: [/create-a-pivottable-with-table/,/create-new-pivot-table-with-list-object-as-source-data/]
keywords: Create a pivot table with list object. Convert list object to pivot table
description: Aspose.Cells Cloud REST API поддерживает создание сводной таблицы с объектом списка. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 60
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Преобразование таблицы в сводную таблицу
---
Этот REST API указывает на создание `pivottable` с объектом списка.
 
## РЕТ API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| Имя листа| нить| путь||
| listObjectIndex| целое число| путь||
| destsheetName| нить| запрос||
| запрос|| тело||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
 
 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api-qa.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \ \
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
 
 
