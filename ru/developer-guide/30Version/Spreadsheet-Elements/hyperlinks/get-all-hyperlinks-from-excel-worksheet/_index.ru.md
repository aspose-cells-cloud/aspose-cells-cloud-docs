---
title: "Получить все гиперссылки – Aspose.Cells Cloud REST API"
type: docs
url: /ru/hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, Получить все гиперссылки, Excel API, REST API, облачный SDK, пример cURL, гиперссылки в электронных таблицах"
description: "Получить все гиперссылки из рабочего листа файла Excel с использованием Aspose.Cells Cloud REST API (v3.0). Включает HTTPS-адрес, необходимые параметры, пример cURL, схему ответа и примеры кода SDK."
weight: 10
ArticleTitle: "Получить все гиперссылки – документация Aspose.Cells Cloud REST API"
---

Этот REST API позволяет получить **все гиперссылки** из конкретного рабочего листа книги Excel.

## Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификацию с использованием токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Обязательный | Значение по умолчанию | Описание                              |
| ------------- | ------ | ------------ | ------------ | --------------------- | ------------------------------------- |
| name          | string | path         | Да           | –                     | Имя файла документа Excel.            |
| sheetName     | string | path         | Да           | –                     | Имя рабочего листа.                   |
| folder        | string | query        | Нет          | –                     | Папка, содержащая документ.           |
| storageName   | string | query        | Нет          | –                     | Имя используемого сервиса хранилища.  |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Ответ JSON содержит объект `Hyperlinks`.

- **Count** – общее количество гиперссылок на рабочем листе.
- **HyperlinkList** – массив, каждый элемент которого содержит объект `link`. Свойство `Href` хранит адрес гиперссылки, а `Rel`, `Title` и `Type` предоставляют дополнительные метаданные (часто `null` для простых ссылок).

### Ответы об ошибках

| Код HTTP | Причина                                            | Пример тела ответа                                                  |
| -------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**  | Неверный запрос – отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Неверное значение параметра." }`        |
| **401**  | Неавторизован – отсутствует или некорректен токен JWT.   | `{ "Code":"401", "Message":"Токен доступа отсутствует или некорректен." }` |
| **404**  | Не найдено – книга или рабочий лист не существует.      | `{ "Code":"404", "Message":"Файл не найден." }`                     |
| **500**  | Внутренняя ошибка сервера – непредвиденный сбой сервера. | `{ "Code":"500", "Message":"Произошла непредвиденная ошибка." }`    |

## Семейство облачных SDK

Использование SDK — самый быстрый способ интеграции данной функциональности. SDK обрабатывают низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}