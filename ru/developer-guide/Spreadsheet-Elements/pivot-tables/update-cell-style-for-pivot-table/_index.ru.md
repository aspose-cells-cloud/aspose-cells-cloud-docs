---
title: Обновить стиль ячейки для сводной таблицы
second_title: Aspose.Cells Cloud Documen
linktitle: Формат
type: docs
url: /ru/pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: Update cell style for a pivot table
description: Aspose.Cells Cloud REST API поддерживает обновление стиля ячеек для сводной таблицы. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 90
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Обновление стиля ячеек для сводной таблицы
---
Этот REST API указывает на обновление ячейки `style` для сводной таблицы.
 
## РЕТ API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| Имя листа| нить| путь| Название рабочего листа.|
| pivotTableIndex| целое число| путь| Индекс сводной таблицы|
| столбец| целое число| запрос||
| ряд| целое число| запрос||
| стиль|| тело| Стиль dto в теле запроса.|
| нужноПересчитать| булев| запрос|ЛОЖЬ|
| папка| нить| запрос| Папка документов.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'  \
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
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}




