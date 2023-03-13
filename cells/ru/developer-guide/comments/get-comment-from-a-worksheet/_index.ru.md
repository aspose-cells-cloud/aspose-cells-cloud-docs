---
title: Ge
type: docs
url: /ru/comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: REST API, spreadsheets, excel, get commen
description: "Cells.Cloud API для работы Excel: получить комментарий"
weight: 10
---
Этот REST API указывает получить комментарий к рабочему листу по имени ячейки.
 
## РСЕТ API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| Название документа.|
| имя листа| нить| путь| Имя рабочего листа.|
| имя_ячейки| нить| путь| Имя ячейки|
| папка| нить| запрос| Папка с документами.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
    "Comment":{

    "CellName":"A1",

    "Author":"roy.wang",

    "HtmlNote": "",

    "Note": "Aspose.Cells Cloud.",

    "AutoSize": "True",

    "IsVisible": "True",

    "Width": 30,

    "Height": 10,

    "TextHorizontalAlignment": "Bottom",

    "TextOrientationType": "TopToBottom",

    "TextVerticalAlignment": "Bottom"

    },
 
   "Code": 200,

   "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0f1e96858d650d16d9c09ca61723c335" >}}

{{< /tab >}}

{{< /tabs >}}
