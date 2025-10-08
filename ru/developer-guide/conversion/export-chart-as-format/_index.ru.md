---
title: Aspose.Cells Cloud Web API — экспорт диаграммы электронной таблицы в виде файла формата
second_title: Documen
ArticleTitle: Export a Spreadsheet Chart as a Format fil
linktitle: Экспортировать диаграмму как форму
type: docs
url: /ru/export-chart-as-format/
keywords: Export Chart, Aspose.Cells Cloud Web API, Spreadsheet Conversion, PDF Export, Image Export, REST, Excel, CSV, JSO
description: Эффективно преобразует диаграммы из электронных таблиц, хранящихся в облаке, в указанные форматы, например PDF, или изображения напрямую, без загрузки.
weight: 100
kwords: Экспорт диаграммы, REST, преобразование в электронную таблицу, PDF, CSV, JSON, Markdown, Excel, формат изображения
---
Экспортируйте облачную таблицу/диаграмму Excel в файл другого формата с помощью Aspose.Cells Cloud Web API.

## **Экспортировать диаграмму в формате API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| имя| Нить| Путь| (Обязательно) Имя файла рабочей книги, который требуется извлечь.|
| рабочий лист| Нить| Путь| Имя рабочего листа|
| chartIndex| Целое число| Путь| Индекс диаграммы|
| формат| Нить| Запрос| (Обязательно) Желаемый выходной формат (например, «png», «pdf», «svg»).|
| папка| Нить| Запрос| (Необязательно) Путь к папке, где хранится рабочая книга; по умолчанию — null.|
| имя_хранилища| Нить| Запрос|(Необязательно) Имя хранилища, если используется пользовательское облачное хранилище; если не указано, используйте хранилище по умолчанию.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке, где хранится рабочая книга; по умолчанию — null.|
|outStorageName| Нить| Запрос| Имя хранилища выходного файла.|
| шрифтыРасположение| Нить| Запрос| Используйте пользовательские шрифты.|
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

## Почему следует использовать экспорт электронной таблицы в формате API?

- Вы можете конвертировать облачные файлы в различные форматы в любое время и в любом месте.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать экспорт электронной таблицы в формате API с SDK?

### Экспортировать диаграмму в формате API Спецификация

 The[Экспортировать диаграмму в формате API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat) определяет общедоступный программный интерфейс, позволяющий осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет экспортировать данные диаграммы электронной таблицы в файл формата с коротким кодом.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.
В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
