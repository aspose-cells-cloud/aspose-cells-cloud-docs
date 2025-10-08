---
title: Aspose.Cells Cloud Web API — объединение нескольких электронных таблиц в одну
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: Объединение таблиц
type: docs
url: /ru/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: Легко объединяйте локальные файлы электронных таблиц в различные форматы (XLSX, CSV, PDF) с помощью Excel API
weight: 100
kwords: Excel API, Объединение электронных таблиц, Office Облако, REST API, Объединение электронных таблиц, формат CSV, JSON, Markdow
---
Объединяйте несколько локальных файлов электронных таблиц в один файл, поддерживая вывод в более чем 30 форматах файлов.

## **Объединение таблиц API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
| Электронная таблица| Файл| FormData| Загрузите файл электронной таблицы.|
| outFormat| Нить| Запрос| Укажите формат выходного файла.|
| mergeInOneSheet| Булевое значение| Запрос| Укажите, следует ли объединить все данные на одном листе.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке для выходной книги. Значение по умолчанию — null.|
|outStorageName| Нить| Запрос| Укажите имя хранилища выходного файла.|
| шрифтыРасположение| Нить| Запрос| Определите пользовательские шрифты, которые будут использоваться.|
| область| Нить| Запрос| Установите область электронной таблицы.|
| пароль| Нить| Запрос| Укажите пароль для открытия файла электронной таблицы.|

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

## Где следует использовать таблицу Merge Local Spreadsheet API?

Если вам необходимо объединить несколько файлов данных, вы можете использовать этот код API.

## Почему вам следует использовать Объединение локальных таблиц API?

- Не нужно место для хранения в облаке, просто объединяйте напрямую.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать объединенную локальную таблицу API с SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)предоставляет общедоступный программный интерфейс, позволяющий пользователям выполнять REST-взаимодействия непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет объединять несколько электронных таблиц в одну с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
