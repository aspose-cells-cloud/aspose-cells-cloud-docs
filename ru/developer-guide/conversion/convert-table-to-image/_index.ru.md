---
title: Aspose.Cells Cloud Web API — Преобразование данных электронной таблицы в изображение
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to an Imag
linktitle: Преобразовать таблицу в изображение
type: docs
url: /ru/convert-table-to-image/
keywords: table to image, Aspose.Cells Cloud Web API, cloud conversion, spreadsheet to image, image format
description: Эффективное преобразование локальной электронной таблицы в файл изображения с помощью Cloud Web Aspose.Cells API
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, преобразование таблицы в изображение, преобразование в облако, форматы файлов изображений, преобразование электронных таблиц
---
 Преобразовать данные локальной электронной таблицы/таблицы Excel в изображение. Поддерживается.**ФОРМАТЫ ИЗОБРАЖЕНИЙ:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Преобразовать таблицу в изображение API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы.|
|рабочий лист|Нить|Запрос|Имя рабочего листа Spreadsheet/Excel|
|имя_таблицы|Нить|Запрос|Имя таблицы для преобразования.|
|формат|Нить|Запрос|Желаемый формат файла изображения (например, png, svg).|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где будет сохранено преобразованное изображение. По умолчанию — null.|
|outStorageName|Нить|Запрос|Укажите имя хранилища выходного файла.|
|шрифтыРасположение|Нить|Запрос|При необходимости используйте пользовательские шрифты.|
|область|Нить|Запрос|Определяет настройки региона электронной таблицы.|
|пароль|Нить|Запрос|Для доступа к файлу электронной таблицы требуется пароль.|

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

## Почему вам следует использовать таблицу преобразования в изображение API?

- Нет необходимости в облачном хранилище, что снижает нагрузку на облачные ресурсы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать таблицу преобразования в изображение API с SDK?

### Преобразовать таблицу в изображение API Спецификация

 The[Преобразовать таблицу в изображение API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToImage) предоставляет общедоступный программный интерфейс для осуществления REST-взаимодействий непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет преобразовать данные электронной таблицы в изображение с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{< /tab >}}
{{< /tabs >}}
