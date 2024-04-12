---
title: Получите фигуру по индексу на листе Excel.
second_title: Aspose.Cells Cloud Documen
linktitle: Ге
type: docs
url: /ru/shapes/get/
aliases: [/get-a-shape-by-index-inside-the-worksheet/]
keywords: Get a shape on an Excel workshee
description: Aspose.Cells Cloud REST API поддерживает получение фигуры на листе Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 20
---
Этот REST API указывает на получение фигуры с форматом изображения или информации о форме на листе Excel.
 
## РСЕТ API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| название документа.|
| имя листа| нить| путь| имя рабочего листа.|
| индекс формы| целое число| путь| Индекс формы в фигурах рабочего листа.|
| папка| нить| запрос| Папка документа.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/autoshapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash

{

  "Status": "string",

  "Shape": {

    "link": {

      "Href": "string",

      "Rel": "string",

      "Title": "string",

      "Type": "string"

    },

    "Name": "string",

    "MsoDrawingType": "string",

    "AutoShapeType": "string",

    "Placement": "string",

    "UpperLeftRow": 0,

    "Top": 0,

    "UpperLeftColumn": 0,

    "Left": 0,

    "LowerRightRow": 0,

    "Bottom": 0,

    "LowerRightColumn": 0,

    "Right": 0,

    "Width": 0,

    "Height": 0,

    "X": 0,

    "Y": 0,

    "RotationAngle": 0,

    "HtmlText": "string",

    "Text": "string",

    "AlternativeText": "string",

    "TextHorizontalAlignment": "string",

    "TextHorizontalOverflow": "string",

    "TextOrientationType": "string",

    "TextVerticalAlignment": "string",

    "TextVerticalOverflow": "string",

    "IsGroup": true,

    "IsHidden": true,

    "IsLockAspectRatio": true,

    "IsLocked": true,

    "IsPrintable": true,

    "IsTextWrapped": true,

    "IsWordArt": true,

    "LinkedCell": "string",

    "ZOrderPosition": 0

  }

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.
 
Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-GetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "dd6d8ac9aacd9be6085356c07dbbadd0" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-GetWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}

