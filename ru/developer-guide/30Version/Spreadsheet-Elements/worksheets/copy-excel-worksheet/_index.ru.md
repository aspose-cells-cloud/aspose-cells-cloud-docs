---
title: "Копирование содержимого и форматов из другого рабочего листа."
second_title: "Документ"
linktype: "Copy"
type: docs
url: /ru/worksheets/copy/
aliases: [  /ru/copy-excel-worksheet/ ]
keywords: "API Aspose Cells для копирования рабочего листа, REST API копирования листа Excel, копирование с помощью Aspose Cloud SDK, копирование рабочего листа в электронной таблице"
description: "Узнайте, как скопировать рабочий лист и его форматы в новый лист с помощью REST API Aspose.Cells Cloud. Приведены примеры эндпоинта, параметров, cURL и SDK для C#, Java, Python и других языков."
weight: 20
---

Этот REST API копирует рабочий лист и его форматы в новый лист внутри той же рабочей книги.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/copy
```

Параметры запроса перечислены ниже:

| Имя параметра   | Тип    | Местоположение | Описание                                                                 |
| ---------------- | ------ | -------------- | ------------------------------------------------------------------------ |
| `name`           | string | path           | Имя файла рабочей книги.                                                 |
| `sheetName`      | string | path           | Имя целевого рабочего листа (нового листа).                              |
| `sourceSheet`    | string | query          | Имя копируемого рабочего листа.                                          |
| `options`        | object | body           | JSON-объект с параметрами копирования (например, ширина столбцов, формулы). |
| `sourceWorkbook` | string | query          | Имя исходной рабочей книги, если она отличается от текущей.              |
| `sourceFolder`   | string | query          | Путь к папке, где хранится исходная рабочая книга.                       |
| `folder`         | string | query          | Путь к папке, куда будет сохранена целевая рабочая книга.               |
| `storageName`    | string | query          | Имя используемого сервиса хранилища.                                      |

### Примеры запроса и ответа

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostCopyWorksheet) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует, как выполнять вызовы Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/NewSheet/copy?sourceSheet=Sheet3X" \
  -X POST \
  -d '{ "ColumnCharacterWidth": true, "CopyInvalidFormulasAsValues": true, "CopyNames": true, "ExtendToAdjacentRange": true, "ReferToDestinationSheet": true, "ReferToSheetWithSameName": true}' \
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

### Обработка ошибок

API возвращает стандартные HTTP-коды состояния вместе с JSON-телом ошибки. Типичные ответы включают:

| HTTP-код | Описание                                                         | Пример JSON-тела ошибки                                      |
| -------- | ---------------------------------------------------------------- | ------------------------------------------------------------ |
| 400      | Неверный запрос — отсутствуют или некорректны параметры.         | `{ "Code": 400, "Message": "Invalid request parameters." }`   |
| 401      | Неавторизованный доступ — отсутствует или неверен токен.         | `{ "Code": 401, "Message": "Authentication failed." }`        |
| 404      | Не найдено — рабочая книга, рабочий лист или папка не существуют. | `{ "Code": 404, "Message": "Resource not found." }`           |
| 500      | Внутренняя ошибка сервера — непредвиденное состояние.             | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже показывают, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}