---
title: Добавление фигуры на рабочий лист Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Объявление
type: docs
url: /ru/shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: Add shape on an Excel workshee
description: Aspose.Cells Cloud REST API поддерживает добавление формы на лист Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 30
---
Этот REST API указывает на добавление формы на рабочий лист Excel.
 
## РСЕТ API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь| название документа.|
| имя листа| нить| путь| имя рабочего листа.|
| формаDTO|| тело||
| рисунокТип| нить| запрос| тип объекта формы|
| верхний левый ряд| целое число| запрос| Индекс верхней левой строки.|
| верхний левый столбец| целое число| запрос| Индекс левого верхнего столбца.|
| вершина| целое число| запрос| Представляет вертикальное смещение Spinner от его левой строки в единицах пикселя.|
| левый| целое число| запрос| Представляет горизонтальное смещение Spinner от его левого столбца в единицах пикселя.|
| ширина| целое число| запрос| Представляет высоту счетчика в пикселях.|
| высота| целое число| запрос| Представляет ширину счетчика в пикселях.|
| папка| нить| запрос| Папка документа.|
| имя_хранилища| нить| запрос| имя хранилища.|
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
-X PUT \
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
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.
 
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-PutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "34f478cae8c02848db0e376bd592a087" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PutWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}
