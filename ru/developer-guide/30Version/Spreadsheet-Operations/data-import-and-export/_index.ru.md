---
title: "Импорт данных в файлы Excel и экспорт данных из файлов Excel"
second_title: "Документ"
linktitle: "Импорт и экспорт данных"
type: docs
url: /ru/data-import-and-export/
keywords: "Aspose.Cells Cloud, импорт данных, экспорт Excel, API, CSV, JSON, изображение, массив"
description: "Узнайте, как импортировать данные из CSV, JSON, массивов и изображений в файлы Excel, а также как экспортировать рабочие книги, диаграммы и фигуры в PDF, PNG и другие форматы с использованием API Aspose.Cells Cloud (v3.0)."
weight: 25
---

API Aspose.Cells Cloud поддерживает импорт данных из различных источников и позволяет экспортировать рабочие книги Excel, диаграммы и другие объекты в различные форматы, включая **XLSX**, **CSV**, **PDF**, **HTML**, **PNG** и другие. Это делает управление данными и их обмен простыми и эффективными.

**Версия API:** **v3.0** – Последнее обновление: **2024‑03‑15**

### Краткое руководство по началу работы

1. **Подготовьте полезную нагрузку** – Создайте JSON-тело, описывающее параметры импорта или экспорта (например, `ImportCSVDataOption`, `ExportOptions`).
2. **Отправьте запрос** – Используйте `curl`, Postman или SDK для вызова соответствующего конечного узла (`POST /cells/import` или `POST /cells/export`).
3. **Обработайте ответ** – При успешном выполнении вы получите обработанный файл (двоичный или в формате Base64). В случае ошибки проанализируйте код состояния HTTP и сообщение об ошибке, возвращённое в JSON-теле.

#### Необходимые условия

- Активная учётная запись Aspose Cloud и действующий JWT-токен.
- Целевая рабочая книга должна существовать в указанном месте хранения (для API, использующих хранилище).
- Правильные заголовки `Content-Type` (`multipart/form-data` для загрузки файлов, `application/json` для JSON-тел).

## Как импортировать данные из различных источников данных

Импорт данных в файл Excel предполагает решение нескольких задач, которые необходимо учесть в процессе. Возможность импорта данных различных форматов и типов с профессиональным качеством — ключевая функция Aspose.Cells Cloud.

### Сведения об API импорта данных

Для импорта данных в один или несколько файлов Excel доступны следующие API:

| API                                                                                                | Описание                                                         |
| :------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | Импорт данных в файлы Excel без использования хранилища.         |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Импорт данных в файл Excel, хранящийся в облаке.                 |

### Параметры запроса

#### Без использования хранилища

| Имя параметра | Тип    | Расположение | Описание                              |
| :------------ | :----- | :----------- | :------------------------------------ |
| file          | файл   | formData     | Файл для загрузки                     |
| ImportOption  | ImportOptions | body     | Указывает формат импорта (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### С использованием хранилища

| Имя параметра | Тип    | Расположение | Описание                          |
| :------------ | :----- | :----------- | :-------------------------------- |
| name          | string | path         | Имя файла Excel                   |
| folder        | string | query        | Путь к папке в хранилище          |
| storageName   | string | query        | Имя хранилища                    |
| importData    | ImportOptions | body     | Полезная нагрузка для импорта данных |

#### Параметры опции импорта данных

**Важные параметры описаны в следующих таблицах:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>Пакетные данные для импорта</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>Нужно ли преобразовывать числовые данные (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>Индекс первой строки</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Индекс первого столбца</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>Разделитель столбцов</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Настройки пользовательских парсеров</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Индекс первой строки</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Индекс первого столбца</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Размещать ли изображение вертикально (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>Данные изображения (строки Base64)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Индекс первой строки</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Индекс первого столбца</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>Двумерный целочисленный массив</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Индекс первой строки</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Индекс первого столбца</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>Двумерный массив чисел с плавающей точкой двойной точности</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Индекс первой строки</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Индекс первого столбца</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>Двумерный строковый массив</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Индекс первой строки</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Индекс первого столбца</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Расположен ли массив вертикально (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>Одномерный целочисленный массив</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Индекс первой строки</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Индекс первого столбца</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Расположен ли массив вертикально (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>Одномерный массив чисел с плавающей точкой двойной точности</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Индекс верхней левой строки</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Индекс верхнего левого столбца</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>Индекс нижней правой строки</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Индекс нижнего правого столбца</td></tr>
    <tr><td>Filename</td><td>string</td><td>Имя исходного файла</td></tr>
    <tr><td>Data</td><td>string</td><td>Строковые данные для импорта</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Имя целевого рабочего листа</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Нужно ли вставлять данные (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Расположение файла данных при отсутствии BatchData</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Индекс строки ячейки</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Индекс столбца ячейки</td></tr>
    <tr><td>type</td><td>string</td><td>Тип данных значения ячейки</td></tr>
    <tr><td>value</td><td>string</td><td>Значение ячейки</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>Определение стиля ячейки</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Параметр</th><th>Тип</th><th>Описание</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem или RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>Путь к исходному файлу</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Как экспортировать объекты Excel в различные форматы файлов

Если вы изначально создали файл Excel в формате **XLS**, **XLSX**, **XLSB** или **CSV**, вам может понадобиться преобразовать его в другой формат для использования конкретных возможностей. Например, экспорт в **PDF** защищает содержимое от неавторизованных изменений и облегчает чтение и обмен файлами.

Экспорт объектов Excel предполагает учёт ряда факторов. Aspose.Cells Cloud обеспечивает высококачественный экспорт рабочих книг, диаграмм, фигур и изображений в широкий спектр форматов:

_Форматы только для экспорта_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
_Форматы для импорта и экспорта_: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

Запрос использует составное содержимое, как определено в [RFC 2046] и [RFC 1341]. Первая часть содержит файл данных; вторая часть — параметры сохранения.

### Сведения об API экспорта

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                                          |
| :------------ | :----- | :----------- | :------------------------------------------------------------------------------------------------ |
| file          | файл   | formData     | Файл для загрузки                                                                                |
| objectType    | string | query        | Тип объекта (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`)    |
| format        | string | query        | Желаемый выходной формат файла (см. [Поддерживаемые форматы файлов](/cells/supported-file-formats/)) |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет публично доступное программное интерфейсное определение, позволяющее выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова API. В приведённом ниже примере показан запрос и его JSON-ответ.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### Распространённые HTTP-коды состояния

| Код | Значение                                                  | Рекомендуемое действие                                 |
| --- | --------------------------------------------------------- | ------------------------------------------------------- |
| 200 | Успех — файл успешно экспортирован                        | Обработать полученный(е) файл(ы)                        |
| 400 | Неверный запрос — отсутствуют или некорректны параметры   | Проверьте полезную нагрузку запроса и строки запроса    |
| 401 | Неавторизован — недействительный или истёкший JWT-токен  | Обновите токен и повторите попытку                     |
| 404 | Не найдено — указанная рабочая книга или лист не существуют | Проверьте имя файла и путь к хранилищу                 |
| 500 | Внутренняя ошибка сервера — неожиданное состояние сервера | Свяжитесь со службой поддержки Aspose, указав ID запроса |

## Как вызывать API импорта и экспорта

В следующих статьях подробно описаны каждый API и содержат примеры с использованием cURL и SDK:

- [Как импортировать данные в файлы Excel без использования хранилища.](/ru/cells/import/without-using-storage)
- [Как импортировать данные в файлы Excel с использованием хранилища.](/ru/cells/import/with-using-storage)
- [Как импортировать пакетные данные в рабочий лист Excel](/ru/cells/import-batch-data-into-excel-worksheet/)
- [Как импортировать данные CSV в рабочий лист Excel](/ru/cells/import-CSV-data-into-excel-worksheet/)
- [Как импортировать изображение в рабочий лист Excel](/ru/cells/import-picture-into-excel-worksheet/)
- [Как импортировать целочисленный массив в рабочий лист Excel](/ru/cells/import-integer-array-into-excel-worksheet/)
- [Как импортировать массив чисел с плавающей точкой двойной точности в рабочий лист Excel](/ru/cells/import-double-array-into-excel-worksheet/)
- [Как импортировать строковый массив в рабочий лист Excel](/ru/cells/import-string-array-into-excel-worksheet/)
- [Как импортировать двумерный целочисленный массив в рабочий лист Excel](/ru/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [Как импортировать двумерный массив чисел с плавающей точкой двойной точности в рабочий лист Excel](/ru/cells/import-a-2D-double-array-into-excel-worksheet/)
- [Как импортировать двумерный строковый массив в рабочий лист Excel](/ru/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Как экспортировать диаграмму Excel в другой формат файла](/ru/cells/export-excel-chart-to-different-formats/)
- [Как экспортировать объект списка Excel в другой формат файла](/ru/cells/export-excel-listobject-to-different-formats/)
- [Как экспортировать объект OLE Excel в другой формат файла](/ru/cells/export-excel-ole-object/)
- [Как экспортировать изображение Excel в другой формат файла](/ru/cells/export-excel-picture-to-different-formats/)
- [Как экспортировать фигуру Excel в другой формат файла](/ru/cells/export-excel-shape-to-different-formats/)
- [Как экспортировать рабочую книгу Excel в другой формат файла](/ru/cells/export-excel-to-different-formats/)
- [Как экспортировать рабочий лист Excel в другой формат файла](/ru/cells/export-excel-worksheet-to-different-formats/)

---