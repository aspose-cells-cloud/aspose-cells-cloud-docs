---
title: "Получение именованных диапазонов в рабочей книге Excel"
second_title: "Документ"
linktype: "Name"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "именованные диапазоны, Excel, Aspose.Cells, облачный API, рабочие листы"
description: "Получение именованных диапазонов из рабочей книги Excel с помощью облачного REST API Aspose.Cells. Включает детали запроса, примеры команд cURL и примеры SDK для множества языков программирования."
ArticleTitle: "Получение именованных диапазонов в рабочей книге Excel – Aspose.Cells Cloud API"
weight: 10
---

Этот REST API возвращает информацию об именованных диапазонах, определённых внутри рабочих листов.

**Введение** – *Именованный диапазон* — это определяемый пользователем идентификатор, ссылающийся на конкретную ячейку или блок ячеек в рабочем листе. Именованные диапазоны упрощают создание формул, повышают читаемость и обеспечивают программный доступ к часто используемым областям рабочей книги.

**Необходимые условия** – Доступ к облачному API Aspose.Cells требует действительного JWT-токена. Получите токен, пройдя аутентификацию с помощью идентификатора клиента и секрета клиента Aspose Cloud через точку входа OAuth 2.0. Включайте токен в заголовок `Authorization: Bearer <jwt token>` каждого запроса.

## API GetNamedRanges

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по JWT-токену</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                                  |
| -------------- | ------ | ------------ | -------------------------------------------- |
| name           | string | Path         | Имя документа Excel.              |
| folder         | string | Query string | Папка, содержащая документ.       |
| storageName    | string | Query string | Имя хранилища, в котором находится документ. |

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос)                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован)                | Недействительный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой полезный объект)           | Загруженный файл превышает лимит размера. |
| 500  | Internal Server Error (Внутренняя ошибка сервера)       | Непредвиденная ошибка сервера. |

Спецификация [OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) определяет публично доступное программное интерфейсное описание, позволяющее выполнять взаимодействие REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова веб-сервисов Aspose.Cells. Пример ниже демонстрирует, как получить именованные диапазоны с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Модель ответа**

| Поле          | Тип    | Описание                                          |
|----------------|---------|------------------------------------------------------|
| `ColumnCount`  | integer | Количество столбцов в диапазоне.                      |
| `ColumnWidth`  | number  | Ширина каждого столбца (в пунктах).                    |
| `FirstColumn`  | integer | Индекс первого столбца в диапазоне (начиная с 0).   |
| `FirstRow`     | integer | Индекс первой строки в диапазоне (начиная с 0).      |
| `Name`         | string  | Пользовательское имя диапазона.                  |
| `RefersTo`     | string  | Формула, определяющая ссылку на ячейку (например, `=Sheet1!$B$10:$H$10`). |
| `RowCount`     | integer | Количество строк в диапазоне.                         |
| `RowHeight`    | number  | Высота каждой строки (в пунктах).                      |
| `Worksheet`    | string  | Имя рабочего листа, содержащего диапазон.       |

## Семейство облачных SDK

Использование SDK — самый быстрый способ интеграции этой функциональности. SDK обрабатывают детали низкого уровня, позволяя вам сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}