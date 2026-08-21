---
title: "Сортировка данных диапазона на листе Excel"
second_title: "Документ"
linktitle: "Сортировка"
type: docs
url: /ru/worksheets/sort-data/
aliases: [  /ru/sort-worksheet-data/ ]
keywords: "Aspose.Cells Cloud, API сортировки Excel, сортировка диапазона на листе, REST API, dataSorter"
description: "Сортировка конкретного диапазона на листе Excel с помощью REST API Aspose.Cells Cloud. Включает эндпоинт, необходимые параметры, шаги аутентификации, обработку ошибок и примеры SDK."
weight: 20
---

REST API позволяет отсортировать данные внутри указанного диапазона на листе Excel.

## REST API

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### Параметры запроса

| Имя параметра | Тип   | Расположение | Обязательный | Описание                                                       |
| -------------- | ------ | -------- | -------- | ----------------------------------------------------------------- |
| name           | string | path     | Да      | Имя рабочей книги.                                                |
| sheetName      | string | path     | Да      | Имя листа.                                               |
| cellArea       | string | query    | Да      | Диапазон ячеек, подлежащий сортировке (например, `A5:A10`).                     |
| dataSorter     | object | body     | Да      | JSON-объект, определяющий параметры сортировки (см. схему ниже). |
| folder         | string | query    | Нет       | Папка, содержащая рабочую книгу.                            |
| storageName    | string | query    | Нет       | Имя хранилища, в котором находится рабочая книга.            |

**Схема объекта `dataSorter`** — в теле запроса должен содержаться JSON-объект со следующими свойствами:

- `CaseSensitive` _(boolean, required)_ — определяет, учитывается ли регистр при сортировке.
- `HasHeaders` _(boolean, required)_ — указывает, содержит ли диапазон строку заголовков.
- `KeyList` _(array, required)_ — коллекция ключей сортировки. Каждый ключ представляет собой объект со следующими полями:
  - `Key` _(integer)_ — индекс столбца (начиная с 0).
  - `SortOrder` _(string)_ — `"ascending"` (по возрастанию) или `"descending"` (по убыванию).
- `SortLeftToRight` _(boolean, required)_ — если `true`, сортировка выполняется слева направо; в противном случае — сверху вниз.
- Дополнительно могут быть указаны параметры `CaseOrder`, `SortLeftToRight` и другие в соответствии со спецификацией OpenAPI.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) предоставляет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Обработка ошибок** — API может возвращать стандартные HTTP-коды ошибок. Типичные ответы включают:

| HTTP-статус | Код | Сообщение                                           |
| ----------- | ---- | ------------------------------------------------- |
| 400         | 400  | Неверный запрос — отсутствуют или недопустимы параметры.      |
| 401         | 401  | Неавторизован — недопустимый или отсутствует JWT-токен.       |
| 404         | 404  | Не найдено — рабочая книга или лист не существуют. |
| 500         | 500  | Внутренняя ошибка сервера.                            |

В случае ошибки тело ответа имеет следующий формат: `{ "Code": <статус>, "Message": "<описание>", "Status": "Error" }`.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}