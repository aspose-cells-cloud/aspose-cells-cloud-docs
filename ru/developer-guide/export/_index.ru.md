---
title: Экспорт книги и внутренних объектов в различные формы.
second_title: Aspose.Cells Cloud Documen
linktitle: Экспорт
type: docs
url: /ru/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API поддерживает экспорт Excel файлов и внутренних объектов в различные форматы файлов. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 31
kwords: Excel, Office Cloud, REST API, электронная таблица, PDF, CSV, Json, Markdwon, экспорт рабочей книги и внутренних объектов в различные форматы.
---
 Если вы изначально создали файл Excel в определенном формате, например[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , и[CSV-файл](https://docs.fileformat.com/spreadsheet/csv/) иногда может оказаться полезным преобразовать файл Excel в другой формат, чтобы можно было воспользоваться его специальными функциями. Например, вы можете экспортировать файл Excel в[PDF](https://docs.fileformat.com/pdf/) чтобы защитить ваш контент от любых несанкционированных изменений и упростить его одновременное чтение и обмен.

 Экспорт объекта Excel — сложный процесс. Многие факторы усложняют процесс экспорта, и поэтому их следует учитывать в процессе экспорта. Возможность экспортировать объект Excel в один файл формата с точным профессиональным качеством — главная особенность Aspose.Cells Cloud.

 Он отлично работает для книг, диаграмм, фигур и изображений, экспортированных из файла Excel. Вы можете экспортировать форматы:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV-файл](https://docs.fileformat.com/spreadsheet/csv/), [ТСВ](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ОРВ](https://docs.fileformat.com/spreadsheet/ods/), [ТЕКСТ](https://docs.fileformat.com/word-processing/txt/) . Форматы только для экспорта:[PDF](https://docs.fileformat.com/pdf/), [ОТС](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [ДИФ](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [ЦИФРЫ](https://docs.fileformat.com/spreadsheet/numbers/), [ПОД](https://docs.fileformat.com/spreadsheet/fods/).

Запрос представляет собой HTTP-запрос с составным содержимым (см.[РФК 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит файл данных, а вторая — параметры сохранения.

Книга REST API `export` и внутренние объекты в файл другого формата.

## РСЕТ API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 Параметры запроса:
 
| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| файл| файл| данные формы| Файл для загрузки|
| тип объекта| нить| запрос| тип объекта (книга/лист/диаграмма/фигура/изображение/список объектов/олеобъект)|
| формат| нить| запрос|[Формат файла](/cells/ru/supported-file-formats/)  |
 
[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.
 
Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Семейство облачных SDK


 Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Пожалуйста, ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для получения полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export.php" >}}


{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


Следующие статьи подробно объясняют каждый номер API и содержат cURL и примеры SDK для каждого API:


1. [Экспорт диаграммы Excel в другой формат файла.](/cells/ru/export/excel-chart-to-different-formats/)
2. [Экспортировать объект списка Excel в другой формат файла.](/cells/ru/export/excel-listobject-to-different-formats/)
3. [Экспортировать оле-объект Excel в другой формат файла.](/cells/ru/export/excel-ole-object/)
4. [Экспорт изображения Excel в другой формат файла.](/cells/ru/export/excel-picture-to-different-formats/)
5. [Экспортировать фигуру Excel в другой формат файла.](/cells/ru/export/excel-shape-to-different-formats/)
6. [Экспортируйте книгу Excel в другой формат файла.](/cells/ru/export/excel-to-different-formats/)
7. [Экспортировать лист Excel в другой формат файла.](/cells/ru/export/excel-worksheet-to-different-formats//)
