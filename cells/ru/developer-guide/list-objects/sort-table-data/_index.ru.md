---
title: Сортировка данных объекта списка в рабочей таблице Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Сор
type: docs
url: /ru/list-objects/sort-data/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/sort-data/]
keywords: Sort a list object(table) in an Excel worksheet
description: Aspose.Cells Cloud REST API поддерживает сортировку объекта списка (таблицы) на листе Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 40
---
Этот REST API указывает `sort table's data` на листе Excel.

## РСЕТ API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| имя листа| нить| путь||
| списокОбъектИндекс| целое число| путь||
| сортировщик данных|| тело||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
-X POST \
-d "{ \"CaseSensitive\": true, \"HasHeaders\": true, \"KeyList\": [ { \"Key\": 1, \"SortOrder\": \"Ascending\", \"CustomList\": \"string\" } ], \"SortLeftToRight\": true}" \
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

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Table-SortTableData-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-ListObjects-PostSortTableData-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ListObjects-post_sort_table_data-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Table-SortTableData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Table-SortTableData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "337292f6bcf5db7e7a0bea74f355071a" >}}

{{< /tab >}}

{{< /tabs >}}
