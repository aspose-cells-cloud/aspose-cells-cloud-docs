---
title: Aspose.Cells Cloud Web API — Преобразование данных диапазона электронной таблицы в CSV-файл
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to a CSV file.
linktitle: Преобразовать диапазон в CS
type: docs
url: /ru/convert-range-to-csv/
keywords: Convert range to csv, convert spreadsheet to csv, Aspose Cloud Web API, cloud conversion, Excel to cs
description: Конвертируйте указанный диапазон из локального файла электронной таблицы в формат CSV с помощью Excel API, обеспечивая бесперебойное выполнение в облаке.
weight: 100
kwords: диапазон в CSV, преобразование электронной таблицы в CSV, Aspose Cloud Web API, преобразование в облако, Excel в CSV
---
 Преобразовать диапазон данных из локальной электронной таблицы/файла Excel в[CSV](https://docs.fileformat.com/spreadsheet/csv/) файл.

## **Преобразовать диапазон в CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы.|
|рабочий лист|Нить|Запрос|Имя рабочего листа Spreadsheet/Excel|
|диапазон|Нить|Запрос|Укажите площадь ячейки (например, A1:C10).|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где будет сохранена рабочая книга. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходных файлов.|
|шрифтыРасположение|Нить|Запрос|При необходимости укажите пользовательские шрифты.|
|область|Нить|Запрос|Определяет настройки региона электронной таблицы.|
|пароль|Нить|Запрос|Для открытия файла электронной таблицы требуется пароль.|

### **Ответ**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream",
        }
    }
]
```

### Коды ошибок

- **400 Неверный запрос**: Неверный URI Apose.Cells Cloud API.
- **401 Неавторизованный**: Недействительный токен доступа. Или недействительный идентификатор клиента и секретный ключ.
- **404 Не найдено**: Файл электронной таблицы недоступен.
- **500 Ошибка сервера**: В электронной таблице обнаружена аномалия при получении расчетных данных.

## Почему вам следует использовать функцию «Конвертировать диаграмму в CSV» API?

- Нет необходимости в облачном хранилище, что снижает нагрузку на облачные ресурсы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать функцию «Конвертировать диаграмму в CSV API» с SDK?

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) описывает общедоступный API, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

## Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет преобразовать диапазон данных в CSV-файл с помощью короткого кода.
 Ознакомьтесь с полным списком облачных SDK Aspose.Cells в нашем[Репозиторий GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
