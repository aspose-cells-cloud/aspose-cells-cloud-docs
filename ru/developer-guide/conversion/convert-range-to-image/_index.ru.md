---
title: Aspose.Cells Cloud Web API — Преобразование данных диапазона электронной таблицы в изображение
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to an Imag
linktitle: Преобразовать диапазон в изображение
type: docs
url: /ru/convert-range-to-image/
keywords: Aspose.Cells Cloud Web API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Format
description: Преобразовать диапазон данных из локальной электронной таблицы/файла Excel в файл изображения
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, Преобразование изображений, PNG, SVG, TIFF, JSON, Markdown
---
Преобразовать диапазон данных из локальной электронной таблицы/файла Excel в файл изображения. Поддерживается**ФОРМАТЫ ИЗОБРАЖЕНИЙ:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Преобразовать диапазон в изображение API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы для конвертации.|
|рабочий лист|Нить|Запрос|Имя рабочего листа Spreadsheet/Excel|
|диапазон|Нить|Запрос|Определите область ячейки для преобразования (например, A1:C10).|
|формат|Нить|Запрос|Укажите формат выходного файла (например, png, svg, tiff).|
|printHeadings|Булевое значение|Запрос|Укажите, следует ли печатать заголовки строк и столбцов.|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где хранится рабочая книга; по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходных файлов.|
|шрифтыРасположение|Нить|Запрос|Пользовательские шрифты, используемые для преобразования.|
|regoin|Нить|Запрос|Определите настройки региона электронной таблицы.|
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

## Почему вам следует использовать функцию «Преобразовать диапазон в изображение» API?

- Нет необходимости в облачном хранилище, что снижает нагрузку на облачные ресурсы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать функцию преобразования диапазона в изображение API с SDK?

### Преобразовать диапазон в изображение API Спецификация

 The[Преобразовать диапазон в изображение API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) предоставляет общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из вашего веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет преобразовать диапазон данных в изображение с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
