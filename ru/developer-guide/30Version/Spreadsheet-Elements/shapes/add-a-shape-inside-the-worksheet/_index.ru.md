---
title: "Добавление фигуры в рабочий лист Excel"
second_title: "Документ"
linktype: "Добавить"
type: docs
url: /shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: "Aspose.Cells, добавление фигуры, Excel, REST API, облачный SDK, shapeDTO, тип рисования"
description: "Узнайте, как добавлять фигуры (дуги, линии, прямоугольники и т.д.) в рабочий лист Excel с помощью Aspose.Cells Cloud REST API версии 3.0. Приведён синтаксис запроса, обязательные параметры, шаги аутентификации и примеры кода SDK."
weight: 30
ArticleTitle: "Добавление фигуры в рабочий лист Excel с использованием Aspose.Cells Cloud API"
---

Этот REST API добавляет фигуру в рабочий лист Excel.  
Конечная точка относится к **версии API v3.0**; убедитесь, что вы используете JWT-токен доступа, получённый через OAuth2-поток Aspose Cloud (client‑id/client‑secret), и включаете его в заголовок `Authorization: Bearer <token>`.

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Параметры запроса**

| Имя параметра  | Тип    | Расположение | Описание                                                                                               |
| --------------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------ |
| name            | string | path         | Имя документа.                                                                                         |
| sheetName       | string | path         | Имя рабочего листа.                                                                                    |
| shapeDTO        | object | body         | JSON-объект, описывающий добавляемую фигуру (полная схема указана в спецификации OpenAPI).             |
| drawingType     | string | query        | Тип объекта фигуры (например, `arc`, `line`, `rectangle`).                                            |
| upperLeftRow    | integer | query       | Индекс верхней левой строки фигуры.                                                                    |
| upperLeftColumn | integer | query       | Индекс верхнего левого столбца фигуры.                                                                 |
| top             | integer | query       | Вертикальное смещение фигуры от её верхнего края в пикселях.                                          |
| left            | integer | query       | Горизонтальное смещение фигуры от её левого края в пикселях.                                          |
| width           | integer | query       | Ширина фигуры в пикселях.                                                                              |
| height          | integer | query       | Высота фигуры в пикселях.                                                                              |
| folder          | string | query        | Папка, содержащая документ.                                                                            |
| storageName     | string | query        | Имя хранилища.                                                                                         |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для лёгкого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

_В случае успешного ответа возвращаются HTTP-код статуса, текстовое описание статуса и идентификатор newly created shape (`ShapeId`)._

{{< /tab >}}

{{< /tabs >}}

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции.                |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недопустимый или отсутствующий JWT-токен.                               |
| 413 | Payload Too Large           | Загружаемый файл превышает допустимый размер.                           |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                          |

Типичные ответы об ошибках включают:

- **400 Bad Request** — отсутствуют или недопустимы параметры.  
- **401 Unauthorized** — недопустимый или отсутствующий JWT-токен.  
- **404 Not Found** — указанный рабочий лист или документ не существует.

Каждая ошибка возвращается в виде JSON-объекта, содержащего поля `Code` и `Message`.

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}