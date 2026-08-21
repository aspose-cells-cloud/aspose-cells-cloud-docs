---
title: "Получение горизонтальных разрывов страницы"
second_title: "Документ"
linktitle: "Получение горизонтальных разрывов страницы"
type: docs
url: /ru/page-breaks/get-horizontal-page-breaks/
aliases: [  /ru/get-horizontal-page-breaks-inside-worksheet/ ]
keywords: "горизонтальные разрывы страницы, Aspose.Cells Cloud, REST API, рабочая книга Excel, SDK"
description: "Получение горизонтальных разрывов страницы из рабочей книги Excel с помощью API Aspose.Cells Cloud. Включает endpoint, параметры, пример cURL, формат ответа и фрагменты кода SDK для C#, Java, Python и других языков."
ArticleTitle: "Получение горизонтальных разрывов страницы — Документация API Aspose.Cells Cloud"
weight: 10
---

**Горизонтальный разрыв страницы** — это разрыв, основанный на строках, который заставляет рабочий лист начинать новую печатную страницу после указанной строки. Этот REST API позволяет получить такие горизонтальные разрывы страницы.

## Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации с использованием токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### Параметры запроса

| Название параметра | Тип    | Местоположение | Описание                                                         |
| ------------------ | ------ | -------------- | ---------------------------------------------------------------- |
| name               | string | path           | Имя файла Excel.                                                 |
| sheetName          | string | path           | Имя рабочего листа.                                              |
| folder             | string | query          | Путь к папке в хранилище, где расположен файл. _(необязательно)_ |
| storageName        | string | query          | Имя хранилища. _(необязательно)_                                 |

<a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="Спецификация OpenAPI для GetHorizontalPageBreaks">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное API и позволяет выполнять взаимодействие с REST API непосредственно из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки cURL. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## Обработка ошибок

| HTTP-статус | Описание                                                           | Пример JSON                                            |
| ----------- | ------------------------------------------------------------------ | ------------------------------------------------------ |
| 400         | Неверный запрос — отсутствуют или некорректны параметры.          | `{ "Code": 400, "Message": "Invalid parameter." }`     |
| 401         | Неавторизован — отсутствует или некорректен токен JWT.            | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404         | Не найдено — указанный файл или рабочий лист не существуют.       | `{ "Code": 404, "Message": "Resource not found." }`    |
| 500         | Внутренняя ошибка сервера — непредвиденное состояние на сервере.  | `{ "Code": 500, "Message": "Server error." }`          |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}