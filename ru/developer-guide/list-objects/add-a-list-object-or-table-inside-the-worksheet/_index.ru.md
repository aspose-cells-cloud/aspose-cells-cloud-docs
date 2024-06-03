---
title: Добавьте объект списка на лист Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Объявление
type: docs
url: /ru/list-objects/add/
aliases: [/add-a-list-object-or-table-inside-the-worksheet/,/tables/add/]
keywords: Add a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API поддерживает добавление объекта списка (таблицы) в рабочий лист Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 10
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Добавить объект списка на лист Excel
---
Этот REST API указывает на `add a list object(table)` на листе Excel.
 
## РСЕТ API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| имя листа| нить| путь| Имя рабочего листа.|
| startRow| целое число| запрос| Начальная строка диапазона списка.|
| startColumn| целое число| запрос| Начальная строка диапазона списка.|
| эндРов| целое число| запрос| Начальная строка диапазона списка.|
| КонецКолонка| целое число| запрос| Начальная строка диапазона списка.|
| имеет заголовки|логическое значение| запрос| Истинный|
| списокОбъект|| тело| Список объектов|
| папка| нить| запрос| Папка документа.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
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
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.
 
Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="4" tabID="4" tabName1="C#" tabName2="VB.NET" tabName3="Java" tabName4="Go" >}}

{{< tab tabNum="1" >}}

```java


```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java


```

{{< /tab >}}

{{< tab tabNum="3" >}}

```java


```

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "6da60ae8d508b08871b2a0b692732ce7" >}}

{{< /tab >}}

{{< /tabs >}}
