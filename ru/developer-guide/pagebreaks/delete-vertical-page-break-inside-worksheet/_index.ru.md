﻿---
title: Удалить вертикальный разрыв страницы
second_title: Aspose.Cells Cloud Documen
linktitle: Удалить вертикальный разрыв страницы
type: docs
url: /ru/page-breaks/delete-vertical-page-break/
aliases: [/delete-vertical-page-break-inside-worksheet/]
keywords: Delete a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API поддерживает удаление разрыва страницы на листе Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 60
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdwon, Удалить вертикальный разрыв страницы
---
 Этот REST API указывает на удаление разрыва страницы `vertical`.
## РСЕТ API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks/{index}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| имя листа| нить| путь||
| индекс| целое число| путь||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteVerticalPageBreak) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/verticalpagebreaks/0" \
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
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.
 
Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
 
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "c835cd32432e2cb4bd5951d616436c16" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a458cdd89dd6d47330fbf1083d7be9b5" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "facec817b056ba33169de10a8a413317" >}}

{{< /tab >}}

{{< /tabs >}}
