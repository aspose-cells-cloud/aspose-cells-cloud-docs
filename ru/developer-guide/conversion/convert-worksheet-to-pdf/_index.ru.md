---
title: Aspose.Cells Cloud Web API — Преобразование электронных таблиц в PDF
second_title: Documen
ArticleTitle: Convert Spreadsheet Worksheet to Pd
linktitle: Преобразовать рабочий лист в Pd
type: docs
url: /ru/convert-worksheet-to-pdf/
keywords: worksheet to pdf, Excel PDF conversion, REST API, cloud-based conversion, spreadsheet to PD
description: Конвертируйте рабочий лист из электронной таблицы на локальном диске в файл PDF с помощью нашего облачного сервиса API
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, преобразование листа в PDF, преобразование в облако, преобразование локального файла
---
Конвертируйте локальную электронную таблицу/рабочий лист Excel в файл PDF с помощью Aspose.Cells Cloud Web API.

## **Конвертировать рабочий лист в PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|-----------------|-|-----------------------|------------------------------------|
| Электронная таблица| Файл| FormData| Загрузите файл электронной таблицы.|
| рабочий лист|Нить| Запрос|Имя рабочего листа в электронной таблице.|
| outPath|Нить| Запрос|(Необязательно) Путь к папке для сохранения рабочей книги; по умолчанию — null.|
| outStorageName|Нить| Запрос| Имя хранилища выходного файла.|
| шрифтыРасположение|Нить| Запрос| Укажите пользовательские шрифты.|
| область|Нить| Запрос| Определите настройки региона электронной таблицы.|
|пароль|Нить| Запрос|Пароль, необходимый для открытия файла электронной таблицы.|

### **Ответ**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Коды ошибок

- **400 Неверный запрос**: Неверный URI Apose.Cells Cloud API.
- **401 Неавторизованный**: Недействительный токен доступа. Или недействительный идентификатор клиента и секретный ключ.
- **404 Не найдено**: Файл электронной таблицы недоступен.
- **500 Ошибка сервера**: В электронной таблице обнаружена аномалия при получении расчетных данных.

## Почему вам следует использовать функцию «Конвертировать таблицу в PDF» API?

- Нет необходимости в облачном хранилище, что снижает нагрузку на облачные ресурсы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать Convert Table to PDF API с SDK?

### Конвертировать таблицу в PDF API Спецификация

 The[Конвертировать таблицу в PDF API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToPdf) предоставляет общедоступный программный интерфейс и позволяет взаимодействовать с REST непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет преобразовать данные электронной таблицы в PDF-файл с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
