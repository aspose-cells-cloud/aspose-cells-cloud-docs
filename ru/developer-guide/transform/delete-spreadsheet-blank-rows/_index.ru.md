---
title: Aspose.Cells Cloud Web API — Удаление пустых строк в электронной таблице
second_title: Documen
ArticleTitle: Delete Blank Rows in a Spreadshee
linktitle: Удалить пустую строку
type: docs
url: /ru/delete-spreadsheet-blank-rows/
keywords: Delete blank rows, Excel API, Spreadsheet cleaning, Aspose.Cells Cloud Web API, Remove empty row
description: Эффективно удаляйте все пустые строки в электронной таблице, не содержащие никаких данных или объектов, улучшая организацию данных.
weight: 100
kwords: Excel, REST, Электронная таблица, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel, Удаление пустых строк
---
Удалите все пустые строки, не содержащие никаких данных или других объектов, из электронной таблицы Excel.

## **Удалить пустые строки таблицы AP**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы.|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходных файлов.|
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

## Где следует использовать функцию «Удалить пустые строки электронной таблицы» API?

Если вам необходимо преобразовать данные, вы можете использовать этот код API.

## Почему следует использовать функцию удаления пустых строк электронной таблицы API?

- Быстро удалите все пустые строки, не содержащие никаких данных или других объектов, из электронной таблицы Excel.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать функцию удаления пустых строк электронной таблицы API с SDK

### Удалить пустые строки электронной таблицы API Спецификация

 The[Удалить пустые строки электронной таблицы API Спецификация](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет удалять пустые строки в электронных таблицах с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}
{{< /tab >}}
{{< /tabs >}}
