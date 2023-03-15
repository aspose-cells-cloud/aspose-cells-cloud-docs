---
title: Удалить условное форматирование
type: docs
url: /ru/conditional-formattings/delete/
aliases: [/remove-conditional-formatting/]
keywords: REST API, spreadsheets, excel, delete cell area from condition formattin
description: "Cells.Cloud API для Excel операция: удалить область ячейки из форматирования условия"
weight: 60
---
Этот REST API указывает удалить условное форматирование
 
## РСЕТ API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| имя листа| нить| путь||
| индекс| целое число| путь||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.


{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "Code": "200",
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}
 
## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}



{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



{{< /tab >}}

{{< tab tabNum="7" >}}



{{< /tab >}}

{{< tab tabNum="8" >}}



{{< /tab >}}

{{< tab tabNum="9" >}}



{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "fa6aed4b68d309d8de12d91ff7c0111d" >}}

{{< /tab >}}

{{< /tabs >}}
