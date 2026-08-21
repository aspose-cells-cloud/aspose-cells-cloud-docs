---
title: "Экспорт страницы рабочего листа – Справочник по API Aspose.Cells Cloud"
articleTitle: "Экспорт страницы рабочего листа – Справочник по API Aspose.Cells Cloud"
secondTitle: "Документ"
linkTitle: "Страница"
type: docs
url: /ru/worksheets/page-to-different-formats/
aliases: [  /ru/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, экспорт страницы рабочего листа, PDF, PNG, CSV, REST API, аутентификация JWT, форматы файлов"
description: "Узнайте, как экспортировать конкретную страницу рабочего листа в форматы PDF, PNG, CSV и другие с помощью REST API Aspose.Cells Cloud. Включает примеры cURL-запросов, руководство по параметрам и примеры SDK для различных языков программирования."
weight: 240
---

Экспорт конкретной страницы рабочего листа полезен, когда вам нужен печатный снимок отчета, изображения графика или выдержки из данных без загрузки всей книги. Этот endpoint позволяет получить отдельную страницу в формате, наилучшим образом соответствующем вашему последующему рабочему процессу.

API [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) позволяет преобразовать указанную страницу рабочего листа в различные форматы файлов. Поддерживаемые форматы: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие REST напрямую из веб-браузера.

> **Необходимые условия** – У вас должен быть действующий токен аутентификации JWT и книга, сохранённая в облачной папке, указанной с помощью параметра `folder`.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Ответ** – Сервис возвращает запрошенную страницу в выбранном формате. Для графических форматов (png, jpeg, gif и т.д.) тело ответа содержит двоичные данные изображения; для документных форматов (pdf, xls, csv и т.д.) тело ответа содержит содержимое файла. Успешный вызов возвращает код HTTP 200.

*Пример ответа в формате PNG (сокращённый фрагмент base64):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Параметры**

| Параметр               | Тип     | Описание                                                             | По умолчанию |
| ---------------------- | ------- | -------------------------------------------------------------------- | ------------ |
| `format`               | string  | Выходной формат файла (например, `pdf`, `png`, `csv`).              | `pdf`        |
| `verticalResolution`   | integer | Вертикальное разрешение рендеримого изображения в DPI.              | `100`        |
| `horizontalResolution` | integer | Горизонтальное разрешение рендеримого изображения в DPI.            | `100`        |
| `pageIndex`            | integer | Индекс страницы рабочего листа для экспорта (начиная с нуля; `0` — первая страница). | `0`          |
| `folder`               | string  | Папка облачного хранилища, где находится исходная рабочая книга.    | —            |

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр успешно применён; ответ содержит детали операции.                |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий токен JWT.                           |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.                             |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка на стороне сервера.                            |

**Возможные ошибки**

- **401 Unauthorized (Неавторизован)** – Недействительный или отсутствующий токен JWT.
- **404 Not Found (Не найдено)** – Указанная рабочая книга или рабочий лист не существует.
- **400 Bad Request (Неверный запрос)** – Недопустимое значение параметра (например, неподдерживаемое значение `format`).
- **500 Internal Server Error (Внутренняя ошибка сервера)** – Непредвиденная проблема на стороне сервера.

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}