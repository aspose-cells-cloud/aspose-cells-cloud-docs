---
title: "Добавление фильтра по дате в лист Excel"
second_title: "Документ"
linktitle: "Добавление фильтра по дате"
type: docs
url: /autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "Узнайте, как добавить фильтр по дате в лист Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Примеры cURL, фрагменты кода SDK (C#, Java, Python и др.), параметры и обработка ошибок."
weight: 65
ArticleTitle: "Добавление фильтра по дате в лист Excel | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, фильтр по дате в Excel, API автофильтра, REST API, облачный SDK, cURL, автоматизация электронных таблиц"
---

Этот REST API добавляет **фильтр по дате** в лист Excel.

**Необходимые условия:** У вас должен быть действительный JWT-токен, а целевая рабочая книга уже должна существовать в указанном месте хранения. Запрос не требует JSON-тела.

## API PutWorksheetDateFilter

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию по токену JWT</a>.

### Параметры запроса


| Имя параметра          | Тип    | Расположение | Описание                                                                                                                                                              |
| ---------------------- | ------ | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**               | string | Path         | Имя рабочей книги.                                                                                                                                                    |
| **sheetName**          | string | Path         | Имя листа.                                                                                                                                                            |
| **range**              | string | Query        | Диапазон Excel, к которому применяется фильтр (например, `A1:B1`).                                                                                                   |
| **fieldIndex**         | integer| Query        | Индекс столбца для фильтрации (начиная с нуля).                                                                                                                       |
| **dateTimeGroupingType**| string| Query        | Тип группировки даты/времени. Допустимые значения: `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. Значения чувствительны к регистру; значение по умолчанию — `Day`. |
| **year**               | integer| Query        | Компонент года фильтруемого значения.                                                                                                                                  |
| **month**              | integer| Query        | Компонент месяца фильтруемого значения.                                                                                                                                |
| **day**                | integer| Query        | Компонент дня фильтруемого значения.                                                                                                                                   |
| **hour**               | integer| Query        | Компонент часа фильтруемого значения.                                                                                                                                  |
| **minute**             | integer| Query        | Компонент минуты фильтруемого значения.                                                                                                                                |
| **second**             | integer| Query        | Компонент секунды фильтруемого значения.                                                                                                                               |
| **matchBlanks**        | boolean| Query        | Включать пустые ячейки (`true` или `false`).                                                                                                                          |
| **refresh**            | boolean| Query        | Обновлять фильтр после применения (`true` или `false`).                                                                                                               |
| **folder**             | string | Query        | Путь к папке исходной рабочей книги.                                                                                                                                  |
| **storageName**        | string | Query        | Имя службы хранения.                                                                                                                                                  |

*Запрос PUT не требует тела запроса; все параметры передаются через строку запроса.*

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; в ответе содержатся детали операции.            |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера.                               |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                          |

## Как использовать API PutWorksheetDateFilter с SDK

### Спецификация API PutWorksheetDateFilter

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}