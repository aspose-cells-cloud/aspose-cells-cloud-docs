---
title: Aspose.Cells Cloud Web API — Преобразование электронной таблицы в файл другого формата
second_title: Documen
ArticleTitle: Convert a Spreadsheet to another format file
linktitle: Преобразовать электронную таблицу
type: docs
url: /ru/convert-spreadsheet/
keywords: spreadsheet conversion, convert spreadsheet, cloud conversion, REST API, XLSX, PDF, CSV, JSON, Markdown, convert local file
description: Легко конвертирует электронную таблицу с локального диска в различные указанные форматы с помощью Excel API
weight: 100
kwords: Excel, Office Cloud, REST API, Преобразование электронных таблиц, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel
---
Конвертируйте локальную электронную таблицу/файл Excel в файл другого формата с помощью Aspose.Cells Cloud Web API.

|**Формат вывода**|**Описание**|
|:- |:- |
|[XLS](https://docs.fileformat.com/spreadsheet/xls/)|Excel 95/5.0 - 2003 Рабочая тетрадь.|
|[XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)|Формат файла Open XML SpreadsheetML Office.|
|[XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)|Excel Двоичная рабочая книга.|
|[XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)|Excel Книга с поддержкой макросов.|
|[XLT](https://docs.fileformat.com/spreadsheet/xlt/)|Excel 97 - Excel 2003 Шаблон.|
|[XLTX](https://docs.fileformat.com/spreadsheet/xltx/)|Excel Шаблон.|
|[XLTM](https://docs.fileformat.com/spreadsheet/xltm/)|Excel Шаблон с поддержкой макросов.|
|[XLAM](https://docs.fileformat.com/spreadsheet/xlam/)|Файл надстройки с поддержкой макросов Excel, который используется для добавления новых функций в Excel.|
|[CSV](https://docs.fileformat.com/spreadsheet/csv/)|Файл CSV (значения, разделенные запятыми).|
|[ТСВ](https://docs.fileformat.com/spreadsheet/tsv/)|Файл TSV (значения, разделенные табуляцией).|
|[ТЕКСТ](https://docs.fileformat.com/word-processing/txt/)|Файл с разделителями в виде простого текста.|
|[HTML](https://docs.fileformat.com/web/html/)|Формат HTML.|
|[MHTML](https://docs.fileformat.com/web/mhtml/)|MHTML-файл.|
|[ОРВ](https://docs.fileformat.com/spreadsheet/ods/)|ODS (электронные таблицы OpenDocument).|
|Электронная таблицаML|Excel 2003 XML-файл.|
|[Числа](https://docs.fileformat.com/spreadsheet/numbers/)|Документ создан с помощью приложения «Numbers» от Apple, которое входит в пакет Apple iWork office — набор приложений, работающих в операционных системах Mac OS X и iOS.|
|[JSON](https://docs.fileformat.com/web/json/)|Нотация объектов JavaScript|
|[ДИФ](https://docs.fileformat.com/spreadsheet/dif/)|Формат обмена данными.|
|[ДБФ](https://docs.fileformat.com/database/dbf/)|Файл с расширением .dbf — это файл базы данных, используемый приложением системы управления базами данных под названием dBASE.|
|[PDF](https://docs.fileformat.com/pdf/)|Формат переносимых документов Adobe.|
|[XPS](https://docs.fileformat.com/page-description-language/xps/)|Формат спецификации бумаги XML.|
|[SVG](https://docs.fileformat.com/page-description-language/svg/)|Масштабируемый формат векторной графики.|
|[TIFF](https://docs.fileformat.com/image/tiff/)|Формат файла изображения с тегами|
|[PNG](https://docs.fileformat.com/image/png/)|Формат переносимой сетевой графики|
|[BMP](https://docs.fileformat.com/image/bmp/)|Формат растрового изображения|
|[EMF](https://docs.fileformat.com/image/emf/)|Расширенный формат метафайла|
|[JPEG](https://docs.fileformat.com/image/jpeg/)|JPEG — это тип формата изображения, сохраняемый с использованием метода сжатия с потерями.|
|[GIF](https://docs.fileformat.com/image/gif/)|Формат графического обмена|
|[УЦЕНКА](https://docs.fileformat.com/word-processing/md/)|Представляет собой документ с уценкой.|
|[SXC](https://docs.fileformat.com/spreadsheet/sxc/)|Формат на основе XML, используемый OpenOffice и StarOffice.|
|[FODS](https://docs.fileformat.com/spreadsheet/fods/)|Это формат открытого документа, хранящийся в виде простого XML.|
|[DOCX](https://docs.fileformat.com/word-processing/docx/)|Известный формат документов Word Microsoft, представляющий собой комбинацию XML и двоичных файлов.|
|[ППТХ](https://docs.fileformat.com/presentation/pptx/)|Формат PPTX основан на формате файла презентации Open XML Microsoft PowerPoint.|
|[SQLScript](https://docs.fileformat.com/database/sql/)|Язык структурированных запросов.|
|[XHtml](https://docs.fileformat.com/web/xhtml/)|XHTML — это текстовый формат файла с разметкой в XML, использующий переформулировку HTML 4.0.|
|[Epub](https://docs.fileformat.com/ebook/epub/)|Файлы с расширением .epub представляют собой формат файлов электронных книг, предоставляющий издателям и потребителям стандартный формат цифровой публикации.|
|[XML](https://docs.fileformat.com/web/xml/)|XML означает расширяемый язык разметки, который похож на HTML, но отличается использованием тегов для определения объектов.|
|[Отс](https://docs.fileformat.com/spreadsheet/ots/)|Откройте файл шаблона документа (OTS).|
|[AZW3](https://docs.fileformat.com/ebook/azw3/)|AZW — это формат файла цифровой электронной книги, разработанный Amazon для устройств Kindle. AZW3, также известный как Kindle Format 8 (KF8).|

## **Преобразовать электронную таблицу API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы, который необходимо преобразовать.|
|формат|Нить|Запрос|(Обязательно) Желаемый формат вывода (например, «Xlsx», «Pdf», «Csv»).|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, в которой будет сохранена преобразованная книга. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Укажите имя хранилища выходных файлов.|
|шрифтыРасположение|Нить|Запрос|Используйте пользовательские шрифты для электронной таблицы.|
|область|Нить|Запрос|Укажите настройку региона электронной таблицы.|
|пароль|Нить|Запрос|Пароль для открытия файла электронной таблицы, если он защищен.|

### **Ответ**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Коды ошибок

- **400 Неверный запрос**: Неверный URI Apose.Cells Cloud API.
- **401 Неавторизованный**: Недействительный токен доступа. Или недействительный идентификатор клиента и секретный ключ.
- **404 Не найдено**: Файл электронной таблицы недоступен.
- **500 Ошибка сервера**: В электронной таблице обнаружена аномалия при получении расчетных данных.

## Почему вам следует использовать Convert Spreadsheet API?

- Нет необходимости в облачном хранилище, что снижает нагрузку на облачные ресурсы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать таблицу Convert API с SDK?

### Конвертировать электронную таблицу API Спецификация

 The[Конвертировать электронную таблицу API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ConvertSpreadsheet) определяет общедоступный программный интерфейс, позволяющий выполнять REST-взаимодействия непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет преобразовать файл электронной таблицы в файл другого формата с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{< /tab >}}
{{< /tabs >}}
