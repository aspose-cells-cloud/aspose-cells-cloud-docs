---
title: "Получить все фигуры на листе Excel"
second_title: "Документ"
linktitle: "Получить-все"
type: docs
url: /ru/shapes/get-all/
aliases: [  /ru/get-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells, облачный API, фигуры Excel, получить фигуры, REST, SDK"
description: "Получить все фигуры (диаграммы, изображения, текстовые поля) с листа Excel с использованием облачного REST API Aspose.Cells. Включает пример cURL, фрагменты кода SDK, шаги аутентификации и обработку ошибок."
ArticleTitle: "Получить все фигуры на листе Excel"
weight: 10
---

Этот REST API позволяет получить все фигуры на листе Excel.

## Безопасность и аутентификация
API облачной платформы Aspose.Cells защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### Параметры запроса

| Имя параметра  | Тип    | Расположение | Описание                                                                                               |
| --------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------ |
| **name**        | string | path         | Имя файла Excel.                                                                                       |
| **sheetName**   | string | path         | Имя листа.                                                                                             |
| **folder**      | string | query        | Папка, содержащая документ.                                                                            |
| **storageName** | string | query        | Имя используемого облачного хранилища.                                                                 |
| **include**     | string | query        | Установите значение `details`, чтобы вернуть полные свойства фигур; иначе возвращаются только объекты `link`. |

> **Необязательно**: параметры `folder`, `storageName` и `include` можно опустить, если файл находится в корневом хранилище.

Для доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. Пример ниже демонстрирует запрос с необязательными параметрами запроса.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Поля ответа

Объект `Shapes` содержит список элементов `Shape`. Каждая фигура включает следующие свойства (если используется флаг `include=details`; иначе возвращается только объект `link`).

| Свойство   | Тип    | Описание                                                             |
| ---------- | ------ | -------------------------------------------------------------------- |
| **Name**   | string | Имя, присвоенное фигуре (например, «Chart 1»).                       |
| **Type**   | string | Тип фигуры (например, `Chart`, `Picture`, `TextBox`).               |
| **Top**    | number | Расстояние в пунктах от верхнего края листа до фигуры.               |
| **Left**   | number | Расстояние в пунктах от левого края листа до фигуры.                 |
| **Width**  | number | Ширина фигуры в пунктах.                                             |
| **Height** | number | Высота фигуры в пунктах.                                             |
| **Link**   | object | Информация о гиперссылке (`Href`, `Rel`, `Type`, `Title`).           |

## Обработка ошибок

| HTTP-статус | Описание                                              | Пример тела ошибки                                                |
| ----------- | ----------------------------------------------------- | ----------------------------------------------------------------- |
| **400**     | Неверный запрос — некорректные параметры.             | `{ "Code": 400, "Message": "Некорректное значение параметра." }` |
| **401**     | Неавторизован — отсутствует или недействителен токен.| `{ "Code": 401, "Message": "Отсутствует или недействителен токен доступа." }` |
| **404**     | Не найдено — рабочая книга или лист не существуют.    | `{ "Code": 404, "Message": "Файл или лист не найден." }`          |
| **500**     | Внутренняя ошибка сервера — непредвиденное условие.   | `{ "Code": 500, "Message": "Произошла непредвиденная ошибка." }`  |

Успешный запрос возвращает **HTTP 200** с объектом `Shapes`, содержащим список фигур, как показано в примере ответа выше.

API ограничивает количество запросов до **150 запросов в минуту на один JWT-токен**. Превышение этого лимита возвращает **HTTP 429** с заголовком `Retry-After`, указывающим, когда можно повторить запрос.

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список SDK облачной платформы Aspose.Cells представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}
---