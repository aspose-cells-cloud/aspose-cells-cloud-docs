---
title: "Удаление фильтра по дате – Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Удаление фильтра по дате"
type: docs
url: /ru/autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, удаление фильтра по дате, автофильтр Excel, REST API, SDK"
description: "Узнайте, как удалить фильтр по дате из рабочего листа Excel с помощью Aspose.Cells Cloud REST API. Приведены endpoint, параметры, пример HTTPS cURL, полезная нагрузка ответа и примеры кода SDK."
ArticleTitle: "Удаление фильтра по дате – документация API Aspose.Cells Cloud"
---

Этот REST API удаляет фильтр по дате на рабочем листе Excel.

**Необходимые условия:** Убедитесь, что у вас есть действительный JWT-токен, книга хранится в облачном хранилище Aspose и у вас есть соответствующие права на изменение рабочего листа.

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра        | Тип    | Расположение | Описание                                                                                     |
|----------------------|--------|-------------|----------------------------------------------------------------------------------------------|
| name                 | string | path        | Имя файла Excel.                                                                             |
| sheetName            | string | path        | Имя рабочего листа.                                                                          |
| fieldIndex           | integer | query      | Индекс столбца (начиная с 0), к которому применяется фильтр.                                 |
| dateTimeGroupingType | string  | query      | Тип группировки даты для фильтра (например, Year, Month, Day).                               |
| year                 | integer | query      | Компонент года фильтра (по умолчанию 0).                                                     |
| month                | integer | query      | Компонент месяца фильтра (по умолчанию 0).                                                   |
| day                  | integer | query      | Компонент дня фильтра (по умолчанию 0).                                                      |
| hour                 | integer | query      | Компонент часа фильтра (по умолчанию 0).                                                     |
| minute               | integer | query      | Компонент минуты фильтра (по умолчанию 0).                                                   |
| second               | integer | query      | Компонент секунды фильтра (по умолчанию 0).                                                  |
| folder               | string  | query      | Путь к папке в хранилище, где расположен файл.                                               |
| storageName          | string  | query      | Имя облачного хранилища Aspose.                                                              |

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK (OK)                     | Фильтр успешно применён; ответ содержит сведения об операции.           |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.                            |
| 413  | Payload Too Large (Слишком большой payload) | Загружаемый файл превышает допустимый размер.                            |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                           |

API возвращает стандартные HTTP-коды состояния, указывающие результат операции удаления.

| Код  | Значение                    | Описание                                                                 |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK (OK)                     | Фильтр по дате успешно удалён; ответ содержит состояние операции.        |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.                            |
| 413  | Payload Too Large (Слишком большой payload) | Загружаемый файл превышает допустимый размер.                            |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                           |

## Как использовать API DeleteWorksheetDateFilter с SDK

### Спецификация API DeleteWorksheetDateFilter

Спецификация <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Примеры кода ниже демонстрируют вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}