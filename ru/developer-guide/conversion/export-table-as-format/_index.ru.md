---
title: Aspose.Cells Cloud Web API — Экспорт данных электронной таблицы в файл формата
second_title: Documen
ArticleTitle: Export a Spreadsheet Table data as a Format file
linktitle: Экспортировать таблицу в указанный формат
type: docs
url: /ru/export-table-as-format/
keywords: Spreadsheet Conversion, Aspose.Cells Cloud Web API, Export Table, RESTI, PDF, CSV, Excel, JSON, Markdow
description: Эффективно конвертирует таблицы из электронных таблиц в облачном хранилище в различные заданные форматы.
weight: 100
kwords: Преобразование электронных таблиц, PDF, CSV, Excel, JSON, Markdown, экспорт таблицы
---
Экспортируйте облачную таблицу/таблицу Excel в файл другого формата.

## **Экспортировать таблицу в формате API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя|Нить|Путь|(Обязательно) Имя файла рабочей книги, который требуется извлечь.|
|рабочий лист|Нить|Путь|Название рабочего листа.|
|имя_таблицы|Нить|Путь|Название таблицы.|
|формат|Нить|Запрос|(Обязательно) Желаемый формат (например, «png», «pdf», «svg»).|
|папка|Нить|Запрос|(Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
|имя_хранилища|Нить|Запрос|(Необязательно) Имя хранилища, если используется пользовательское облачное хранилище. Если не указано, используйте хранилище по умолчанию.|
|outPath|Нить|Запрос|(Необязательно) Путь к папке для хранения выходных данных. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходных файлов.|
|шрифтыРасположение|Нить|Запрос|Расположение пользовательских шрифтов.|
|область|Нить|Запрос|Настройка региона электронной таблицы.|
|пароль|Нить|Запрос|Пароль для открытия файла электронной таблицы.|

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

### Экспортировать таблицу в формате API Спецификация

 The[Экспортировать таблицу в формате API Спецификация](https://reference.aspose.cloud/cells/#/ConversionController/ExportTableAsFormat) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет экспортировать данные электронной таблицы в файл формата с коротким кодом.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{< /tab >}}
{{< tab tabtabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
