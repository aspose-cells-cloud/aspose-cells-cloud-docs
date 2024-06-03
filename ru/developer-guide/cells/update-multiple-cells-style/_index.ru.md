---
title: Обновление нескольких стилей Cells
type: docs
url: /ru/update-multiple-cells-style/
weight: 20
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, обновление нескольких стилей Cells
---
Этот REST API указывает на установку `cells style` в ячейку в файле Excel.

 
## РСЕТ API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Имя рабочей книги.|
| имя листа| нить| путь| Имя рабочего листа.|
| диапазон| нить| запрос| Диапазон.|
| стиль|| тело| с настройками стиля обновления.|
| папка| нить| запрос| Папка рабочей книги.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
-X POST \
 -d "{ \"Font\": { \"Color\": { \"A\":255, \"R\": 255, \"G\": 255, \"B\": 0 }, \"DoubleSize\": 10, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true, \"Name\": \"Arial\", \"Size\": 22 }, \"Name\": \"string\", \"CultureCustom\": \"string\", \"Custom\": \"string\", \"BackgroundColor\": { \"A\": 10, \"R\": 10, \"G\": 10, \"B\": 10 }, \"ForegroundColor\": { \"A\": 255, \"R\": 255, \"G\": 255, \"B\": 0 } \
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



{{< tabs tabTotal="3" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostUpdateWorksheetCellStyle-.php" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-post_update_worksheet_cell_style-.rb" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "59dae0a6697e3c68ade244ed28b27d10" >}}

{{< /tab >}}

{{< /tabs >}}
