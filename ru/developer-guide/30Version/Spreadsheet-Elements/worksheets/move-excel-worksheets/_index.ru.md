---
title: "Перемещение листа Excel — Aspose.Cells Cloud API (v3.0)"
second_title: "Документ"
linktitle: "Переместить"
type: docs
url: /ru/worksheets/move/
aliases: [  /ru/move-excel-worksheets/ ]
keywords: "Aspose.Cells Cloud, перемещение листа, Excel, REST API, SDK, C#, Java, Python, Node.js, PHP, Ruby, Go, Android, Swift, Perl, v3.0"
description: "Узнайте, как переместить лист Excel в новую позицию с помощью Aspose.Cells Cloud API (v3.0). Приведены endpoint, необходимые параметры, пример cURL и код SDK на C#, Java, Python и других языках."
weight: 20
ArticleTitle: "Как переместить лист Excel с помощью Aspose.Cells Cloud API v3.0"
---

Этот REST API позволяет перемещать лист внутри книги Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/position
```

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                                                                                                           |
| ------------- | ----- | ------------ | ------------------------------------------------------------------------------------------------------------------ |
| name          | string | путь        | Имя файла Excel.                                                                                                   |
| sheetName     | string | путь        | Имя листа, который нужно переместить.                                                                              |
| moving        | object | тело         | JSON-объект, задающий целевой лист (`DestinationWorksheet`) и относительную позицию (`Position`).                 |
| folder        | string | query        | Путь к папке, где хранится рабочая книга.                                                                          |
| storageName   | string | query        | Имя сервиса хранилища.                                                                                             |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostMoveWorksheet) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова веб-сервисов Aspose.Cells. Пример ниже показывает, как переместить лист за один запрос.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/position" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"DestinationWorksheet":"Sheet5","Position":"after"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                                      |
|-----|-----------------------------|-------------------------------------------------------------------------------|
| 200 | OK (ОК)                    | Фильтр применён успешно; ответ содержит детали операции.                     |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недопустимый или отсутствующий JWT-токен.                                    |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера.                                    |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                               |

**Пример ошибочного payload**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Missing required parameter 'moving'."
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostMoveWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostMoveWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-move_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "MoveExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-MoveWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-MoveWorksheet-move-excel-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-MoveWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1f9b294ef1cfb23e3775c193f15ff660" >}}

{{< /tab >}}

{{< /tabs >}}