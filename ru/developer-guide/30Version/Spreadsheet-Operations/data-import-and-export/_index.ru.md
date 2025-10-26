---
title: Импорт данных в файлы Excel и экспорт данных из файлов Excel
second_title: Documen
linktitle: Данные импорта и экспорта
type: docs
url: /ru/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: Создавайте новые документы или отчеты, которые могут включать диаграммы, таблицы и другие элементы визуализации данных.
weight: 25
kwords: Excel импорт данных против прямого доступа к базе данных; Пакетный импорт данных против построчной записи данных; Автоматизированный экспорт данных против ручного извлечения данных.
---
Aspose.Cells Cloud API поддерживает импорт данных из различных источников данных и может экспортировать данные из Excel, диаграмм и графиков в различные форматы, включая Excel, CSV, PDF, HTML, PNG и т. д. Это делает управление данными и обмен ими простыми и эффективными.

## Как импортировать данные из различных источников данных

Импорт данных в файл Excel — сложный процесс. Сложность обусловлена множеством факторов, поэтому при экспорте их следует учитывать. Возможность импорта данных различных форматов и типов в файл с профессиональным качеством — главная особенность Aspose.Cells Cloud.

### Информация об API импорта данных

Предоставляются следующие API для импорта данных в файл Excel или несколько файлов Excel:

|API|Описание|
|:- |:- |
|[POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Импорт данных в файлы Excel без использования хранилища.|
|[POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Импортируйте данные в файл Excel с использованием хранилища.|

### Параметры запроса

#### Без использования хранилища

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| файл| файл| formData| Файл для загрузки|
| ImportOption| ImportOptions| HTTPBody| Массив целых чисел/Двойной массив/Строковый массив/Двумерный массив целых чисел/Двумерный массив двойных чисел/Двумерный массив строк/Пакетные данные/CSV-данные/Изображение|

#### С использованием хранилища

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
| importData|| тело||

#### Параметр опции импорта данных

**Важные параметры описаны в следующей таблице.**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Пакетные данные</td><td>Список<CellValue></td> <td>пакетные данные</td> </tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>ConvertNumericData</td><td>Нить</td> <td>верно/ложно.</td> </tr>
    <tr> <td>FirstRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>инт</td><td></td></tr>
    <tr><td>РазделительСтрок</td><td> Нить</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>CustomParsers</td><td>Список<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>CSVData</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>инт</td><td></td></tr>
    <tr><td>IsVertical</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>Данные</td><td> Нить[]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>Картина</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>инт</td><td></td></tr>
    <tr><td>Данные</td><td> Целое число[,]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>инт</td><td></td></tr>
    <tr><td>Данные</td><td> Двойной[,]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>инт</td><td></td></tr>
    <tr><td>Данные</td><td> Нить[,]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>инт</td><td></td></tr>
    <tr><td>IsVertical</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>Данные</td><td> Целое число[]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>IntegerArray</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>FirstRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>FirstColumn</td><td>инт</td><td></td></tr>
    <tr><td>IsVertical</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>Данные</td><td> Двойной[]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>DoubleArray</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>UpperLeftRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>UpperLeftColumn</td><td>инт</td><td></td></tr>
    <tr> <td>LowerRightRow</td><td>инт</td> <td></td> </tr>
    <tr> <td>Нижний правый столбец</td><td>инт</td><td></td></tr>
    <tr><td>Имя файла</td><td>Нить</td><td></td></tr>
    <tr><td>Данные</td><td> Нить</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя конечного рабочего листа.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>верно/ложно.</td></tr>
    <tr><td>ImportDataType</td><td> Нить</td><td>StringArray</td></tr>
    <tr> <td>Источник</td><td> FileSource</td><td>Указывает позицию файла данных, если параметр BatchData равен нулю.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>инт</td> <td></td> </tr>
    <tr><td>columnIndex</td><td>инт</td><td></td></tr>
    <tr><td>тип</td><td>Нить</td><td>тип данных</td></tr>
    <tr><td>ценить</td><td> Нить</td> <td></td></tr>
    <tr><td>стиль</td><td> Стиль(объект)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>Нить</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>FilePath</td><td>Нить</td><td> положение файла</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Как экспортировать объекты Excel в различные форматы файлов

Если вы изначально создали файл Excel в определенном формате, например[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , и[CSV](https://docs.fileformat.com/spreadsheet/csv/)Иногда может возникнуть необходимость преобразовать файл Excel в другой формат, чтобы воспользоваться его специальными функциями. Например, вы можете экспортировать файл Excel в...[PDF](https://docs.fileformat.com/pdf/) для защиты вашего контента от несанкционированных изменений и обеспечения удобства его чтения и распространения одновременно.

Экспорт объекта Excel — сложный процесс. На сложность влияет множество факторов, поэтому при экспорте следует учитывать их. Возможность экспорта объекта Excel в файл одного формата с точным профессиональным качеством — главная особенность Aspose.Cells Cloud.

 Он идеально подходит для экспорта рабочих книг, диаграмм, фигур и изображений из файлов Excel. Поддерживаемые форматы экспорта:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [ТСВ](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ОРВ](https://docs.fileformat.com/spreadsheet/ods/), [ТЕКСТ](https://docs.fileformat.com/word-processing/txt/) Форматы, доступные только для экспорта:[PDF](https://docs.fileformat.com/pdf/), [ОТС](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [ДИФ](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [ЧИСЛА](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Запрос представляет собой HTTP-запрос с составным содержимым (см.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)или[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Первая часть составного содержимого содержит файл данных, а вторая — параметры сохранения.

Рабочая книга REST API `export` и внутренние объекты в файл другого формата.

### Экспорт информации API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

Параметры запроса:

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| файл| файл| formData| Файл для загрузки|
| Тип объекта| нить| запрос| тип объекта (рабочая книга/рабочий лист/диаграмма/фигура/изображение/объект списка/объект ole)|
| формат| нить| запрос|[Формат файла](/cells/ru/supported-file-formats/)  |

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

Вы можете использовать командную строку cURL для лёгкого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как совершать вызовы в облако API с помощью cURL.

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

## Как вызывать API импорта и экспорта

В следующих статьях подробно объясняется, как вызывать каждый номер API, а также содержатся примеры cURL и SDK для каждого номера API:

- [Как импортировать данные в файлы Excel без использования хранилища.](/cells/ru/import/without-using-storage)
- [Как импортировать данные в файлы Excel с использованием хранилища.](/cells/ru/import/with-using-storage)
- [Как импортировать пакетные данные в рабочий лист Excel](/cells/ru/import-batch-data-into-excel-worksheet/)
- [Как импортировать данные CSV в рабочий лист Excel](/cells/ru/import-csv-data-into-excel-worksheet/)
- [Как импортировать изображение в рабочий лист Excel](/cells/ru/import-picture-into-excel-worksheet/)
- [Как импортировать целочисленный массив в рабочий лист Excel](/cells/ru/import-integer-array-into-excel-worksheet/)
- [Как импортировать двойной массив в рабочий лист Excel](/cells/ru/import-double-array-into-excel-worksheet/)
- [Как импортировать массив строк в рабочий лист Excel](/cells/ru/import-string-array-into-excel-worksheet/)
- [Как импортировать 2-мерный целочисленный массив в рабочий лист Excel](/cells/ru/import-a-2D-integer-array-into-excel-worksheet/)
- [Как импортировать двумерный двойной массив в рабочий лист Excel](/cells/ru/import-a-2D-double-array-into-excel-worksheet/)
- [Как импортировать двумерный строковый массив в рабочий лист Excel](/cells/ru/import-a-2D-string-array-into-excel-worksheet/)
- [Экспорт диаграммы Excel в другой формат файла](/cells/ru/export-excel-chart-to-different-formats/)
- [Экспортировать список-объект Excel в другой формат файла](/cells/ru/export-excel-listobject-to-different-formats/)
- [Экспорт Excel ole-object в другой формат файла](/cells/ru/export-excel-ole-object/)
- [Экспортировать изображение Excel в другой формат файла](/cells/ru/export-excel-picture-to-different-formats/)
- [Экспорт формы Excel в другой формат файла](/cells/ru/export-excel-shape-to-different-formats/)
- [Экспорт книги Excel в другой формат файла](/cells/ru/export-excel-to-different-formats/)
- [Экспортировать рабочий лист Excel в другой формат файла](/cells/ru/export-excel-worksheet-to-different-formats//)
