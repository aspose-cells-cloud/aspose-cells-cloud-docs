---
title: Aspose.Cells Cloud Web API — Преобразование электронной таблицы в изображение
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: Преобразовать диаграмму в изображение
type: docs
url: /ru/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: Преобразуйте диаграмму из локальной электронной таблицы/файла Excel в файл изображения с помощью Cloud Web Aspose.Cells API
weight: 100
kwords: преобразовать диаграмму Excel в изображение, png, svg, tiff, jpg, bmp, электронную таблицу
---
Преобразовать диаграмму из локальной электронной таблицы/файла Excel в файл формата изображения. Поддерживается.**ФОРМАТЫ ИЗОБРАЖЕНИЙ:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Преобразовать диаграмму в изображение API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы, содержащий диаграмму.|
|рабочий лист|Нить|Запрос|Укажите название рабочего листа, если применимо.|
|chartIndex|Целое число|Запрос|Индекс диаграммы для преобразования.|
|формат|Нить|Запрос|(Обязательно) Желаемый тип изображения (например, svg, png, jpg).|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где хранится рабочая книга; по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходного файла.|
|шрифтыРасположение|Нить|Запрос|При необходимости укажите пользовательские шрифты.|
|область|Нить|Запрос|Установите область электронной таблицы.|
|пароль|Нить|Запрос|Пароль для открытия файла электронной таблицы.|

## **Ответ**

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

## Где следует использовать функцию «Преобразовать диаграмму в изображение» API?

- Экспортируйте диаграммы из электронной таблицы как изображения.

## Почему вам следует использовать функцию «Преобразовать диаграмму в изображение» API?

- Нет необходимости в облачном хранилище, что снижает нагрузку на облачные ресурсы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать инструмент «Преобразовать диаграмму в изображение» API с SDK?

### Преобразовать диаграмму в изображение API Спецификация

 The[Преобразовать диаграмму в изображение API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет преобразовать диаграмму в изображение с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
