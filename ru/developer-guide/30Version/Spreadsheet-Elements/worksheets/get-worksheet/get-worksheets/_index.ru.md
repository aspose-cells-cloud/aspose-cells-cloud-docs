---
title: "Получить все листы"
second_title: "Документ"
linktitle: "Все"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, облачный API, получить листы, Excel, REST, SDK"
description: "Получить список листов в книге Excel через облачный REST API Aspose.Cells (версия 3.0). Содержит пример cURL, фрагменты кода SDK и формат ответа."
weight: 10
---

Этот REST API возвращает информацию о листах, содержащихся в книге.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Параметры запроса**

| Имя параметра | Тип    | Местоположение | Описание                              |
| ------------- | ------ | -------------- | ------------------------------------- |
| name          | string | path           | Имя документа Excel.                  |
| folder        | string | query          | Папка, содержащая документ.           |
| storageName   | string | query          | Имя используемого хранилища.          |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие по протоколу REST непосредственно из веб-браузера.

Для доступа к службам Aspose.Cells Cloud можно использовать утилиту командной строки cURL. В приведённом ниже примере показан GET-запрос на получение списка листов.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Обработка ошибок

Типичные HTTP-коды состояния, возвращаемые этой конечной точкой:

| Код | Значение                | Описание                                        |
| --- | ----------------------- | ----------------------------------------------- |
| 400 | Неверный запрос         | Отсутствует обязательный параметр (например, `name`). |
| 401 | Неавторизован           | Неверный или отсутствующий токен JWT.           |
| 404 | Не найдено              | Указанная книга не существует.                 |
| 500 | Внутренняя ошибка сервера | Непредвиденное состояние сервера.              |

Ответы об ошибках возвращаются в формате JSON, например:

```json
{
  "Code": "401",
  "Message": "Неверный токен доступа."
}
```

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud представлен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}