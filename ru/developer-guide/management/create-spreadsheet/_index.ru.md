---
title: Aspose.Cells Cloud Web API — Создание новой электронной таблицы с помощью шаблона электронной таблицы
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: Создать электронную таблицу
type: docs
url: /ru/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: Excel API позволяет пользователям создавать новые электронные таблицы с указанным именем, поддерживая дополнительные шаблоны для предопределенного содержимого или форматирования, что повышает производительность пользователей.
weight: 100
kwords: Excel, Office Cloud, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Сопоставление всех пустых ячеек на листе Excel, Создание электронных таблиц, Поддержка шаблонов, Повышение производительности
---
Создайте новую электронную таблицу, которая может быть либо пустой, либо готовой к использованию электронной таблицей, созданной на основе указанного шаблона.

## **Создать электронную таблицу API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|---------- ||----------------------- |----- |
|формат| Нить| Запрос| Указывает имя новой электронной таблицы. Это имя будет использоваться для идентификации таблицы в системе.|
| шаблон| Нить| Запрос| Необязательно. Если указано, новая таблица будет создана на основе указанного шаблона. Это может быть полезно для применения предопределенных макетов и стилей.|
| outPath| Нить| Запрос| (Необязательно) Путь к папке, где хранится книга. Значение по умолчанию — null.|
| outStorageName| Нить| Запрос| Имя хранилища выходного файла.|
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

## Где следует использовать Create Spreadsheet API?

Если вам нужно создать новую электронную таблицу, вы можете использовать этот номер API.

## Почему вам следует использовать Create Spreadsheet API?

- Вы можете создать не только пустую электронную таблицу, но и специальную таблицу на основе шаблона.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать Create Spreadsheet API с SDK

### Создать электронную таблицу API Спецификация

 The[Создать электронную таблицу API Спецификация](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) определяет общедоступный программный интерфейс и обеспечивает взаимодействие REST непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет создавать электронные таблицы с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
