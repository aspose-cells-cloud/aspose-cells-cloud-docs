---
title: "Получение вертикальных разрывов страницы"
second_title: "Документ"
linktitle: "Получение вертикальных разрывов страницы"
type: docs
url: /page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: "Aspose.Cells, вертикальные разрывы страницы, Excel API, облачная электронная таблица, REST API"
description: "Получение вертикальных разрывов страницы из рабочего листа Excel с использованием Aspose.Cells Cloud REST API (версия 3.0). Включает HTTPS-эндпоинт, необходимые параметры, пример cURL, детали ответа, обработку ошибок и примеры SDK."
weight: 20
---

Этот REST API позволяет получить **вертикальные** разрывы страницы из рабочего листа.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Параметры запроса

| Имя параметра   | Тип    | Расположение | Описание                                           | Обязательный |
| --------------- | ------ | ------------ | -------------------------------------------------- | ------------ |
| `name`          | string | path         | Имя файла Excel.                                   | Да           |
| `sheetName`     | string | path         | Имя рабочего листа, из которого требуется считать разрывы. | Да           |
| `folder`        | string | query        | Папка в хранилище, содержащая файл.                | Нет          |
| `storageName`   | string | query        | Имя хранилища Aspose Cloud, которое следует использовать. | Нет          |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Детали ответа

| Поле                    | Тип    | Описание                                                                      |
| ----------------------- | ------ | ----------------------------------------------------------------------------- |
| `VerticalPageBreakList` | array  | Коллекция объектов вертикальных разрывов страницы.                            |
| `Column`                | int    | Индекс столбца (начиная с нуля), в котором происходит разрыв.                 |
| `StartRow`              | int    | Начальная строка диапазона разрыва (начиная с нуля).                          |
| `EndRow`                | int    | Конечная строка диапазона разрыва (начиная с нуля, обычно `1048575` — последняя строка). |
| `link.Href`             | string | Самоуказывающий URL-адрес ресурса (HTTPS).                                    |
| `Code`                  | int    | Код HTTP-статуса, возвращённый сервисом.                                      |
| `Status`                | string | Текстовое описание HTTP-статуса.                                              |

### Обработка ошибок

| Код HTTP | Значение                | Типичная причина                              |
| -------- | ----------------------- | --------------------------------------------- |
| 401      | Unauthorized (Неавторизовано) | Отсутствует или недействителен JWT-токен.    |
| 404      | Not Found (Не найдено)  | Указанный файл или рабочий лист не существует. |
| 400      | Bad Request (Неверный запрос) | Некорректные или неправильно сформированные параметры запроса. |
| 500      | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденное состояние на стороне сервера. |

Проверьте поля `Code` и `Status` в JSON-ответе для получения дополнительных сведений.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки под Aspose.Cells Cloud. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}