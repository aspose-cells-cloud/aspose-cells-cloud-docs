---
title: Импор
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API поддерживает импорт данных в файлы Excel. SDK поддерживает различные языки разработки. К ним относятся Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby и Swift.
weight: 31
---
Импорт данных в файл Excel — сложный процесс. Многие факторы усложняют процесс экспорта, и поэтому их следует учитывать в процессе экспорта. Возможность импортировать в файл различные форматы и типы данных с точным профессиональным качеством — главная особенность Aspose.Cells Cloud.

## API-интерфейсы RSET

Предоставляются следующие API-интерфейсы для импорта данных в файл Excel или несколько файлов Excel:

|API|Описание|
|:- |:- |
|[POST/ячейки/импорт](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Импортируйте данные в файлы Excel без использования хранилища.|
|[POST/cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Импортируйте данные в файл Excel с использованием хранилища.|

## Параметры запроса
 
### Без использования хранилища

| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| файл| файл| данные формы| Файл для загрузки|
| ИмпортОпция| Параметры импорта|HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

### С использованием хранилища

| Имя параметра| Тип| Путь/строка запроса/HTTPBody|Описание|
|:- |:- |:- |:- |
| имя| нить| путь||
| папка| нить| запрос||
| имя_хранилища| нить| запрос| имя хранилища.|
| импортдата|| тело||


### Параметр опции импорта данных

**Важные параметры описаны в следующей таблице.**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Пакетные данные</td><td>Список<CellValue></td> <td>данные партии</td> </tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Конвертироватьчисловые данные</td><td>Нить</td> <td>правда/ложь.</td> </tr>
    <tr> <td>Первая строка</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Первая колонка</td><td>интервал</td><td></td></tr>
    <tr><td>РазделительСтрока</td><td> Нить</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>ПользовательскиеПарсеры</td><td>Список<CustomParserConfig></td><td></td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>CSVДанные</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Первая строка</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Первая колонка</td><td>интервал</td><td></td></tr>
    <tr><td>IsVertical</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Данные</td><td> Нить[]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>Картина</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Первая строка</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Первая колонка</td><td>интервал</td><td></td></tr>
    <tr><td>Данные</td><td> Целое число[,]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Первая строка</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Первая колонка</td><td>интервал</td><td></td></tr>
    <tr><td>Данные</td><td> Двойной[,]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>Два измеренияDoubleArray</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Первая строка</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Первая колонка</td><td>интервал</td><td></td></tr>
    <tr><td>Данные</td><td> Нить[,]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Первая строка</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Первая колонка</td><td>интервал</td><td></td></tr>
    <tr><td>IsVertical</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Данные</td><td> Целое число[]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>Целое числоМассив</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Первая строка</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Первая колонка</td><td>интервал</td><td></td></tr>
    <tr><td>IsVertical</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Данные</td><td> Двойной[]</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>ДаблМассив</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr> <td>Верхний левый ряд</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Верхний левый столбец</td><td>интервал</td><td></td></tr>
    <tr> <td>Нижний правый ряд</td><td>интервал</td> <td></td> </tr>
    <tr> <td>Нижний правый столбец</td><td>интервал</td><td></td></tr>
    <tr><td>Имя файла</td><td>Нить</td><td></td></tr>
    <tr><td>Данные</td><td> Нить</td> <td></td></tr>
    <tr> <td>Рабочий лист назначения</td><td> Нить</td><td> Имя рабочего листа назначения.</td></tr>
    <tr><td>IsInsert</td><td>Нить</td><td>правда/ложь.</td></tr>
    <tr><td>Импортдататипе</td><td> Нить</td><td>StringArray</td></tr>
    <tr> <td>Источник</td><td> источник файла</td><td>Указывает позицию файла данных, когда параметр BatchData имеет значение null.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>индекс строки</td><td>интервал</td> <td></td> </tr>
    <tr><td>индекс столбца</td><td>интервал</td><td></td></tr>
    <tr><td>тип</td><td>Нить</td><td>тип данных</td></tr>
    <tr><td>ценить</td><td> Нить</td> <td></td></tr>
    <tr><td>стиль</td><td> Стиль (объект)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Параметр</th><th scope="col">Тип</th> <th scope="col">Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>ТипФайлИсточника</td><td>Нить</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Путь к файлу</td><td>Нить</td><td> позиция файла</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Как вызвать API RSET

В следующих статьях подробно объясняется, как звонить по каждому номеру API, и приводятся примеры cURL и SDK для каждого номера API:

- [Как импортировать данные в файлы Excel без использования хранилища.](/cells/ru/import/without-using-storage)
- [Как импортировать данные в файлы Excel с использованием хранилища.](/cells/ru/import/with-using-storage)
- [Как импортировать пакетные данные в рабочий лист Excel](/cells/ru/import/batch-data/)
- [Как импортировать данные CSV в лист Excel](/cells/ru/import/csv-data/)
- [Как импортировать изображение в рабочий лист Excel](/cells/ru/import/picture/)
- [Как импортировать целочисленный массив в рабочий лист Excel](/cells/ru/import/integer-array/)
- [Как импортировать двойной массив в рабочий лист Excel](/cells/ru/import/double-array/)
- [Как импортировать массив строк в рабочий лист Excel](/cells/ru/import/string-array/)
- [Как импортировать двухмерный целочисленный массив в лист Excel](/cells/ru/import/2dimension-integer-array/)
- [Как импортировать двухмерный двойной массив в лист Excel](/cells/ru/import/2dimension-double-array/)
- [Как импортировать двумерный массив строк в лист Excel](/cells/ru/import/2dimension-string-array/)
