---
title: Aspose.Cells Cloud Web API — Переименование листа в электронной таблице
second_title: Documen
ArticleTitle: Rename worksheet in Spreadshee
linktitle: Переименовать рабочий лист в электронной таблице
type: docs
url: /ru/rename-worksheet-in-spreadsheet/
keywords: Excel API, Rename Worksheet, Workbook Management, REST API, Spreadsheet Organizatio
description: Конечная точка Web API позволяет пользователям переименовывать указанный рабочий лист в рабочей книге, улучшая организацию и удобочитаемость.
weight: 100
kwords: Excel API, Переименование листа, Управление рабочими книгами, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel
---
Переименовать имя листа в электронной таблице.

## **Переименовать имя листа в электронной таблице API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы.|
|sourceName|Нить|Запрос|Текущее имя переименовываемого листа.|
|targetName|Нить|Запрос|Новое имя для рабочего листа.|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходного файла.|
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

## Где следует использовать функцию «Переименовать рабочий лист» в электронной таблице API?

Если вам необходимо переименовать рабочий лист в электронных таблицах, вы можете использовать этот код API.

## Почему следует использовать функцию «Переименовать рабочий лист» в электронной таблице API?

- Быстро переименовывайте рабочие листы из электронных таблиц.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать функцию «Переименовать рабочий лист» в электронной таблице API с SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet)описывает общедоступный программный интерфейс, позволяющий взаимодействовать с REST непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя всю необходимую информацию, позволяя вам легко реализовать переименование листов в ячейках электронных таблиц с минимальным количеством кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
