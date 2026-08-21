---
title: "Скрытие столбцов в рабочей таблице Excel"
second_title: "Документ"
linktitle: "Скрыть"
type: docs
url: /columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, API для скрытия столбцов, скрытие столбцов в Excel, REST API для скрытия столбцов, Aspose.Cells SDK, автоматизация электронных таблиц"
description: "Узнайте, как скрыть один или несколько столбцов в рабочей таблице Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает описание конечной точки, параметры запроса, пример cURL, примеры кода SDK и обработку ошибок."
weight: 40
---

Этот REST API скрывает столбцы в рабочей таблице.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### Параметры запроса

| Имя параметра  | Тип    | Расположение | Описание                                                                 |
| -------------- | ------ | ------------- | ------------------------------------------------------------------------ |
| name           | string | path          | Имя файла рабочей книги.                                                 |
| sheetName      | string | path          | Имя рабочей таблицы, в которой будут скрыты столбцы.                    |
| startColumn    | integer | query       | Индекс первого скрываемого столбца (начинается с 0).                     |
| totalColumns   | integer | query       | Количество последовательных столбцов для скрытия, начиная с **startColumn**. |
| folder         | string | query         | Путь к папке, содержащей рабочую книгу.                                 |
| storageName    | string | query         | Имя службы хранилища, в которой расположен файл.                        |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого вызова веб-сервисов Aspose.Cells. Пример ниже показывает, как с помощью cURL скрыть столбец.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Возможные коды ответа**

| HTTP-код | Значение                                 | Пример JSON (ошибка)                                |
| -------- | ---------------------------------------- | --------------------------------------------------- |
| 200      | Успех                                    | `{ "Code": 200, "Status": "OK" }`                   |
| 400      | Неверный запрос (например, некорректные параметры) | `{ "Code": 400, "Message": "Недопустимый диапазон столбцов." }` |
| 401      | Неавторизованный запрос (отсутствующий/некорректный токен) | `{ "Code": 401, "Message": "Некорректный токен доступа." }` |
| 404      | Не найдено (рабочая книга или рабочая таблица) | `{ "Code": 404, "Message": "Файл не найден." }`     |
| 500      | Внутренняя ошибка сервера                | `{ "Code": 500, "Message": "Непредвиденная ошибка." }` |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK абстрагирует низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}