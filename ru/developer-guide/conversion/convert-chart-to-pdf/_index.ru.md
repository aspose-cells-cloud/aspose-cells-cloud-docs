---
title: Aspose.Cells Cloud Web API — Преобразование таблицы в PDF-файл
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: Преобразовать диаграмму в PD
type: docs
url: /ru/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: Этот API легко преобразует диаграммы из электронных таблиц, расположенных на локальном диске, в файл PDF
weight: 100
kwords: Excel, Office Облако, REST API, Преобразование электронных таблиц, PDF, CSV, JSON, Markdown, Преобразование диаграмм в PDF, Облачное преобразование
---
 Преобразовать диаграмму из локальной электронной таблицы/файла Excel в[PDF](https://docs.fileformat.com/pdf/) файл.

## **Конвертировать диаграмму в PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|-------------- ||--------------------- |--------------------------------------------------- |
| Электронная таблица|Файл| FormData| Загрузите файл электронной таблицы.|
| рабочий лист| Нить| Запрос| Имя рабочего листа, содержащего диаграмму.|
| chartIndex|Целое число| Запрос| Индекс диаграммы для преобразования.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке, где будет сохранён преобразованный файл. Значение по умолчанию — null.|
| outStorageName| Нить| Запрос| Имя хранилища выходного файла.|
| шрифтыРасположение| Нить| Запрос| При необходимости используйте пользовательские шрифты.|
| область| Нить| Запрос| Настройка региона электронной таблицы.|
| пароль| Нить| Запрос| Пароль для открытия файла электронной таблицы.|

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

## Где следует использовать функцию «Конвертировать диаграмму в PDF» API?

- Экспортируйте диаграммы из электронной таблицы в формате PDF.

## Почему вам следует использовать функцию «Конвертировать диаграмму в PDF» API?

- Нет необходимости в облачном хранилище, что снижает нагрузку на облачные ресурсы.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать Convert Chart to PDF API с SDK?

### Конвертировать диаграмму в PDF API Спецификация

 The[Конвертировать диаграмму в PDF API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

## Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет преобразовать диаграмму в PDF-файл с помощью короткого кода.
В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
