---
title: "Заморозка панелей на листе Excel"
second_title: "Документ"
linktitle: "Заморозка"
type: docs
url: /ru/worksheets/panes/freeze/
aliases: [  /ru/freeze-panes-in-excel-worksheet/ , /ru/worksheets/freeze-panes/ ]
keywords: "Aspose.Cells Cloud, Заморозка панелей, Excel, REST API, Лист"
description: "Узнайте, как заморозить строки и столбцы на листе Excel с помощью REST API Aspose.Cells Cloud. Включает синтаксис конечной точки, обязательные параметры, пример cURL, рекомендации по аутентификации, подробности об ошибках и примеры кода SDK для нескольких языков."
weight: 190
---

Этот REST API **устанавливает** заморозку панелей на листе Excel.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

Параметры запроса:

| Имя параметра | Тип    | Расположение | Описание                                               |
| ------------- | ------ | ------------ | ------------------------------------------------------ |
| name          | string | path         | Имя файла рабочей книги.                               |
| sheetName     | string | path         | Имя листа, на котором выполняется заморозка панелей.   |
| row           | integer | query       | Индекс первой **незамороженной** строки (начиная с 0). |
| column        | integer | query       | Индекс первого **незамороженного** столбца (начиная с 0). |
| frozenRows    | integer | query       | Количество строк, подлежащих заморозке сверху.         |
| frozenColumns | integer | query       | Количество столбцов, подлежащих заморозке слева.       |
| folder        | string  | query       | Путь к папке в хранилище, где находится рабочая книга. |
| storageName   | string  | query       | Имя сервиса хранилища.                                 |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### Ответ об ошибке

| HTTP-статус               | Код | Сообщение                            | Пример                                                    |
| ------------------------- | --- | ------------------------------------ | --------------------------------------------------------- |
| 400 Bad Request           | 400 | Неверные параметры                   | `{ "Code": 400, "Message": "Неверное значение frozenRows" }` |
| 401 Unauthorized          | 401 | Отсутствует или недействителен JWT  | `{ "Code": 401, "Message": "Неверный токен доступа" }`    |
| 404 Not Found             | 404 | Рабочая книга или лист не найдены    | `{ "Code": 404, "Message": "Файл не найден" }`           |
| 500 Internal Server Error | 500 | Непредвиденная ошибка сервера        | `{ "Code": 500, "Message": "Внутренняя ошибка сервера" }` |

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}