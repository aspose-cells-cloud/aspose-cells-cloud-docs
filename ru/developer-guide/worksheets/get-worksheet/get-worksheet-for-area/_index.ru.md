﻿---
title: Экспорт области из рабочей таблицы Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Являются
type: docs
url: /ru/worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: Get area to different format content from an Excel worksheet
description: Aspose.Cells Cloud REST API поддерживает получение области содержимого другого формата из рабочего листа Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и swift.
weight: 230
---
[ПОЛУЧИТЬ /ячейки/{имя}/рабочие листы/{имя листа}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API позволяет преобразовать указанную область рабочего листа в формат файла. Поддерживаемые форматы:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [ТСВ](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ОРВ](https://docs.fileformat.com/spreadsheet/ods/), [ТЕКСТ](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [ОТС](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [ДИФ](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/),[гифка](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/),[TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [НОМЕРА](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).


## ОТДЫХ API

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorkshee) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для простого доступа к веб-службам Aspose.Cells. В следующем примере показано, как звонить в Cloud API с номером cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

Converted Image 

```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK
 
 Использование SDK — лучший способ ускорить разработку. SDK позаботится о низкоуровневых деталях и позволит вам сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) полный список Aspose.Cells Cloud SDK.
 
В следующих примерах кода показано, как выполнять вызовы веб-служб Aspose.Cells с помощью различных SDK.

{{< tabs tabTotal="7" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Ruby" tabName6="PHP" tabName7="Node.js" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "9550c8e96c1d39b03fdf58053a5e79e2" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "9031223dee8a678505878e887533df4a" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "16dee84a0846f649727b066f20732da0" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "b36476d85ae21a2368ee4eed6fe478e9" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "cbb9cd7b55aa4264f994658831fb8e77" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "b261f08e109d3d64e4ffc9ffe128e3f3" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "638d99f44813b9d6139967bc6fb43ecd" >}}

{{< /tab >}}

{{< /tabs >}}
