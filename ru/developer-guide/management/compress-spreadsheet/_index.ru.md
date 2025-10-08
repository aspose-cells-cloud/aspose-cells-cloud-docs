---
title: Aspose.Cells Cloud Web API — Сжатие размера электронной таблицы
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: Сжать электронную таблицу
type: docs
url: /ru/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: Сжатие электронных таблиц API позволяет пользователям эффективно уменьшать размер файлов электронных таблиц, применяя заданные уровни сжатия, оптимизируя хранилище и повышая производительность.
weight: 100
kwords: Excel, Office Облако, REST, Сжатие электронных таблиц, Оптимизация размера файла, PDF, CSV, Json, Markdow
---
Уменьшить размер электронной таблицы.

## **Сжать электронную таблицу API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
|Электронная таблица|Файл|FormData|Загрузите файл электронной таблицы, который необходимо сжать.|
|уровень|Целое число|Запрос|Задает уровень сжатия, который будет применяться: от 0 (без сжатия) до 9 (максимальное сжатие).|
|outPath|Нить|Запрос|(Необязательно) Путь к папке, где будет сохранена сжатая книга. Значение по умолчанию — null.|
|outStorageName|Нить|Запрос|Имя хранилища выходного файла.|
|область|Нить|Запрос|Настройка региона электронной таблицы.|
|пароль|Нить|Запрос|Пароль, необходимый для открытия файла электронной таблицы.|

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

## Где следует использовать Compress Spreadsheet API?

Если вам необходимо уменьшить размер электронных таблиц, вы можете использовать этот код API.

## Почему вам следует использовать Compress Spreadsheet API?

- Таблица слишком большая, необходимо уменьшить размер файла.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать сжатую электронную таблицу API с SDK

### Сжатие электронной таблицы API Спецификация

 The[Сжатие электронной таблицы API Спецификация](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) предоставляет общедоступный интерфейс для взаимодействия REST, позволяющий осуществлять прямые вызовы API из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей, позволяя сжимать размер электронной таблицы с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как взаимодействовать с веб-сервисами Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
