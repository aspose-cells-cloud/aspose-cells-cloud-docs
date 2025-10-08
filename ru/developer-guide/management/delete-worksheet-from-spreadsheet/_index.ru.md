---
title: Aspose.Cells Cloud Web API — Удаление листа из электронной таблицы
second_title: Documen
ArticleTitle: Delete a worksheet from the Spreadshee
linktitle: Удалить рабочий лист из электронной таблицы
type: docs
url: /ru/delete-worksheet-from-spreadsheet/
keywords: delete worksheet, spreadsheet management, Aspose.Cells Cloud Web API, REST API, workbook structure, remove worksheet
description: Эта конечная точка API позволяет пользователям удалять указанный рабочий лист из рабочей книги, упрощая управление структурами рабочих книг за счет устранения ненужных или избыточных рабочих листов.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, JSON, Markdown, Управление рабочими листами Excel, Удаление ненужных рабочих листов
---
Удалить рабочий лист из электронной таблицы.

## **Удалить лист из таблицы API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:-               |:-     |:-                         |:-           |
| Электронная таблица|Файл| FormData| Загрузите файл электронной таблицы.|
| Имя_листа| Нить| Запрос| Указывает имя или идентификатор удаляемого листа. Этот параметр является обязательным и должен совпадать с именем существующего листа в книге.|
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

## Где следует использовать функцию «Удалить лист из таблицы API»?

Если вам нужно удалить лист из электронных таблиц, вы можете использовать этот код API.

## Почему вам следует использовать функцию удаления листа из таблицы API?

- Быстро удаляйте рабочие листы из электронных таблиц.
- Разработку можно быстро завершить с помощью существующего SDK.

## Как использовать функцию удаления листа из таблицы API с SDK

### Удалить рабочий лист из спецификации электронной таблицы API

 The[Удалить рабочий лист из спецификации электронной таблицы API](https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet) определяет общедоступный программный интерфейс, позволяющий осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — самый быстрый способ разработки, поскольку он абстрагируется от низкоуровневых деталей и позволяет удалять рабочие листы из электронной таблицы с помощью короткого кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
