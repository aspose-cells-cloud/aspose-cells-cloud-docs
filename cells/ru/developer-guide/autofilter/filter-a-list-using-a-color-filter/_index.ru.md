---
title: Добавьте цветной фильтр в рабочую таблицу Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Добавить цветной фильтр
type: docs
url: /ru/autofilter/add-color-filter/
aliases: [/filter-a-list-using-a-color-filter/,/autofilter/add-a-color-filter/]
keywords: Adds a color filter on an Excel worksheet
description: Облако Aspose.Cells API поддерживает добавление цветного фильтра на рабочий лист Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 65
---
Этот REST API указывает на добавление `color filter` на рабочий лист Excel.


## РСЕТ API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| имя листа| нить| путь||
| диапазон| нить| запрос||
| индекс поля| целое число| запрос||
| цветФильтр|| тело||
| matchBlanks| логический| запрос||
| обновить| логический| запрос||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-FilterListUsingColorFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-PutWorksheetColorFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_color_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FilterListUsingColorFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FilterListUsingColorFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "96fa12d386e68fa3315f16730e951b87" >}}

{{< /tab >}}

{{< /tabs >}}
