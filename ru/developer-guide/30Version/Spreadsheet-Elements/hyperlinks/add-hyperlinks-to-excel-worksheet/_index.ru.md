---
title: "Добавление гиперссылки в рабочий лист"
type: docs
url: /ru/hyperlinks/add/
aliases: [  /ru/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells, добавить гиперссылку, Excel REST API, облачный SDK"
description: "Узнайте, как добавить гиперссылку в рабочий лист Excel с помощью Aspose.Cells Cloud REST API v3.0. Включает адрес конечной точки, полное руководство по параметрам, пример cURL и фрагменты кода SDK для C#, Java, Python и других языков."
weight: 20
---

Этот REST API добавляет гиперссылку в рабочий лист Excel.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                                       |
| ------------- | ------ | ------------ | ---------------------------------------------------------------------------------------------- |
| name          | string | path         | Имя документа.                                                                                 |
| sheetName     | string | path         | Имя рабочего листа.                                                                            |
| firstRow      | integer | query       | Индекс первой строки диапазона (отсчитывается от нуля), к которому будет применена гиперссылка. |
| firstColumn   | integer | query       | Индекс первого столбца диапазона (отсчитывается от нуля), к которому будет применена гиперссылка. |
| totalRows     | integer | query       | Количество строк, охватываемых диапазоном гиперссылки.                                         |
| totalColumns  | integer | query       | Количество столбцов, охватываемых диапазоном гиперссылки.                                      |
| address       | string | query        | Целевой URL, на который указывает гиперссылка (в URL-кодировке).                              |
| folder        | string | query        | Папка документа.                                                                               |
| storageName   | string | query        | Имя хранилища.                                                                                 |

Запрос также может включать JSON-тело, содержащее те же поля (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Указание тела полезно, если вы предпочитаете передавать параметры через полезную нагрузку, а не через строку запроса.

### Ответы об ошибках

| HTTP-код | Причина                                               | Пример тела ответа                                                 |
| -------- | ----------------------------------------------------- | ------------------------------------------------------------------ |
| **400**  | Неверный запрос — отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Invalid parameter value." }`          |
| **401**  | Неавторизован — отсутствует или недействителен JWT-токен. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Не найдено — рабочая книга или рабочий лист не существуют. | `{ "Code":"404", "Message":"File not found." }`                   |
| **500**  | Внутренняя ошибка сервера — непредвиденная ошибка сервера. | `{ "Code":"500", "Message":"An unexpected error occurred." }`     |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST API напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
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

Если запрос завершается с ошибкой, API возвращает стандартные HTTP-коды ошибок (например, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error), а также JSON-тело, содержащее сообщение об ошибке и её код.

## Семейство облачных SDK

Использование SDK — это самый быстрый способ разработки. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}