---
title: "Экспорт листа с помощью Aspose.Cells Cloud API — форматы, примеры cURL и SDK"
second_title: "Документ"
linktitle: "Экспорт листа"
type: docs
url: /worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, экспорт листа, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, cloud API"
description: "Узнайте, как экспортировать один лист из файла Excel с помощью Aspose.Cells Cloud REST API. Включает endpoint, параметры, исправленный пример cURL, данные об аутентификации, обработку ошибок и фрагменты кода SDK для C#, Java, Python и других языков."
weight: 10
ArticleTitle: "Экспорт листа с помощью Aspose.Cells Cloud API — форматы, примеры cURL и SDK"
---

Этот REST API позволяет **экспортировать лист** из файла Excel в множество различных форматов файлов.

**Краткое описание** — используйте endpoint **Get Worksheet** для загрузки одного листа из рабочей книги в выбранном вами формате.

Вы можете экспортировать в следующие форматы:

| Формат  | Расширение | MIME-тип                                                          |
| ------- | --------- | ----------------------------------------------------------------- |
| XLS     | .xls      | application/vnd.ms-excel                                          |
| XLSX    | .xlsx     | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb     | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv      | text/csv                                                          |
| TSV     | .tsv      | text/tab-separated-values                                         |
| XLSM    | .xlsm     | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods      | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt      | text/plain                                                        |
| PDF     | .pdf      | application/pdf                                                   |
| OTS     | .ots      | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps      | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif      | application/x-dif                                                 |
| PNG     | .png      | image/png                                                         |
| JPEG    | .jpeg     | image/jpeg                                                        |
| GIF     | .gif      | image/gif                                                         |
| BMP     | .bmp      | image/bmp                                                         |
| WMF     | .wmf      | image/wmf                                                         |
| TIFF    | .tiff     | image/tiff                                                        |
| EMF     | .emf      | image/emf                                                         |
| NUMBERS | .numbers  | application/vnd.apple.numbers                                     |
| FODS    | .fods     | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## Безопасность и аутентификация
Aspose.Cells Cloud API безопасны и требуют [аутентификации по токену JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Параметры запроса**

| Имя параметра            | Тип    | Расположение | Описание                                                                 |
| ------------------------ | ------ | ------------ | ------------------------------------------------------------------------ |
| **name**                 | string | path         | **Обязательный.** Имя файла Excel.                                      |
| **sheetName**            | string | path         | **Обязательный.** Имя листа, который требуется экспортировать.         |
| **format**               | string | query        | Целевой формат файла для экспортируемого листа (например, `pdf`, `png`).|
| **verticalResolution**   | integer| query        | Разрешение изображения в DPI для форматов, поддерживающих разрешение (например, PNG, JPEG). |
| **horizontalResolution** | integer| query        | Разрешение изображения в DPI для форматов, поддерживающих разрешение.   |
| **area**                 | string | query        | Диапазон ячеек для экспорта (например, `A1:D10`).                       |
| **pageIndex**            | integer| query        | Индекс страницы для экспорта, если лист разбит на страницы.             |
| **folder**               | string | query        | Путь к папке в хранилище, где расположен исходный файл.                 |
| **storageName**          | string | query        | Имя хранилища Aspose Cloud.                                             |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как вызвать Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<двоичные данные>
```

{{< /tab >}}

{{< /tabs >}}

## Обработка ошибок

API возвращает стандартные HTTP-коды состояния. Распространённые ответы включают:

| Код состояния | Значение                                                    | Пример JSON-тела ответа                   |
| ------------- | ----------------------------------------------------------- | ----------------------------------------- |
| **200**       | Успех — поток листа возвращён.                              | `{ "stream": "..." }`                     |
| **400**       | Неверный запрос — отсутствующие или некорректные параметры.| `{ "error": "Неверный параметр формата." }`|
| **401**       | Неавторизован — недействительный или отсутствующий токен JWT.| `{ "error": "Ошибка аутентификации." }`   |
| **404**       | Не найдено — указанный файл или лист не существует.         | `{ "error": "Лист не найден." }`          |
| **500**       | Внутренняя ошибка сервера — непредвиденное состояние сервера.| `{ "error": "Непредвиденная ошибка." }`   |

Обрабатывайте эти ответы в клиентском коде, чтобы предоставить пользователям соответствующую обратную связь.

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей и позволяет сосредоточиться на задачах вашего проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a>, чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

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