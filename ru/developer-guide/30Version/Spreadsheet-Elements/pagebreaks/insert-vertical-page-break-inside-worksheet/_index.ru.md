---
title: "Добавление вертикального разрыва страницы"
second_title: "Документ"
linktitle: "Добавление вертикального разрыва страницы"
type: docs
url: /page-breaks/add-vertical-page-break/
aliases: [/insert-vertical-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, вертикальный разрыв страницы, REST API, Excel, SDK, cURL"
description: "Узнайте, как вставить вертикальный разрыв страницы в рабочий лист Excel с помощью Aspose.Cells Cloud REST API (v3.0). Включает синтаксис запроса, пример cURL, примеры SDK, руководство по аутентификации и сведения об обработке ошибок."
weight: 40
ArticleTitle: "Добавление вертикального разрыва страницы – Aspose.Cells Cloud API"
---

Этот REST API вставляет вертикальный разрыв страницы в рабочий лист.

## Безопасность и аутентификация
Aspose.Cells Cloud API являются защищёнными и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                                 |
|---------------|--------|-------------|--------------------------------------------------------------------------|
| name          | string | path        | Имя рабочей книги Excel.                                                 |
| sheetName     | string | path        | Имя рабочего листа, в который будет добавлен разрыв страницы.           |
| cellname      | string | query       | Ссылка на ячейку (например, **A1**), определяющая положение разрыва.     |
| column        | integer| query       | Индекс столбца (начиная с нуля), в котором начинается разрыв страницы.   |
| row           | integer| query       | Индекс строки (начиная с нуля), в которой начинается разрыв страницы.    |
| startRow      | integer| query       | Первая строка диапазона разрыва.                                          |
| endRow        | integer| query       | Последняя строка диапазона разрыва.                                       |
| folder        | string | query       | Путь к папке в хранилище, где расположена рабочая книга.                 |
| storageName   | string | query       | Имя сервиса хранилища.                                                   |

**Обязательные параметры** – должен быть указан либо `cellname`, либо `column`. При использовании `column` можно также указать `row`, `startRow` и `endRow` для задания диапазона. Все остальные поля являются необязательными.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Пример cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Ответ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции.                |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован)| Недействительный или отсутствующий JWT-токен.                           |
| 413 | Payload Too Large (Слишком большой заголовок)| Загружаемый файл превышает допустимый размер.                        |
| 500 | Internal Server Error (Внутренняя ошибка сервера)| Непредвиденная ошибка сервера.                                     |

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Посетите [репозиторий GitHub](https://github.com/aspose-cells-cloud), чтобы ознакомиться со полным списком SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}