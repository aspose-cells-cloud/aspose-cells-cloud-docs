---
title: Aspose.Cells Cloud WEb API — Разделить электронную таблицу на отдельные файлы
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: Разделенная электронная таблица
type: docs
url: /ru/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: Разделите локальную электронную таблицу на несколько файлов в различных форматах без необходимости использования облачного хранилища.
weight: 100
kwords: Excel API, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Разделение локальной электронной таблицы, Облачная обработка, Управление файлами, Обработка ошибок
---
Разделите локальную электронную таблицу на отдельные файлы с 30 форматами выходных файлов без необходимости использования облачного хранилища.

## **Разделенная таблица API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| Электронная таблица| Файл| FormData| Загрузите файл электронной таблицы, который необходимо разделить.|
| от| Целое число| Запрос| Укажите начальный индекс рабочего листа.|
| к| Целое число| Запрос| Укажите конечный индекс рабочего листа.|
| outFormat| Нить| Запрос| Определите формат выходного файла.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке для сохранения выходной книги. Значение по умолчанию — null.|
|outStorageName| Нить| Запрос| Определите имя хранилища выходных файлов.|
| шрифтыРасположение| Нить| Запрос| При необходимости укажите пользовательские шрифты.|
| regoin| Нить| Запрос| Установите область электронной таблицы.|
| пароль| Нить| Запрос| Укажите пароль для доступа к файлу электронной таблицы.|

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

## Где следует использовать таблицу разделения API?

Если вам нужно разделить электронную таблицу на несколько файлов, вы можете использовать этот код API.

## Почему вам следует использовать Split Spreadsheet API?

- Не нужно место для хранения в облаке, просто разделяйте напрямую.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать разделенную электронную таблицу API с SDK

### Спецификация разделенной таблицы API

 The[Спецификация разделенной таблицы API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) предоставляет общедоступный программный интерфейс для выполнения REST-взаимодействий непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет разделить электронную таблицу на отдельные файлы с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
