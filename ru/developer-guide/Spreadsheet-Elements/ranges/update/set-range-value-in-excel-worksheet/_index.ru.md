---
title: Установите значение диапазона на рабочем листе Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Установить значение
type: docs
url: /ru/ranges/update/values/
aliases: [/set-range-value-in-excel-worksheet/]
keywords: Set range value on an Excel workshee
description: Aspose.Cells Cloud REST API поддерживает установку диапазона значений на листе Excel. SDK поддерживает различные языки разработки. Они включают Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift
weight: 72
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Установка значения диапазона на рабочем листе Excel
---
Этот REST API указывает на помещение значения в диапазон, при необходимости значение будет преобразовано в другой тип данных, а числовой формат ячейки будет сброшен.
            
 
## РЕТ API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| название рабочей книги|
| Имя листа| нить| путь| имя рабочего листа|
| ценить| нить| запрос| Входное значение|
| диапазон|| тело| диапазон в рабочем листе|
| isConverted| булев| запрос|ЛОЖЬ|
| setStyle| булев| запрос|ЛОЖЬ|
| папка| нить| запрос| Папка с рабочей тетрадью.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать командную строку cURL для легкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?Value=25&isConverted=false&setStyle=false" \
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
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о низкоуровневых деталях и позволяет вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
 
  
{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}
