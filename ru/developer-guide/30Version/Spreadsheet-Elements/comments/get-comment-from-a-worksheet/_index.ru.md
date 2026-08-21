---
title: "Получить комментарий листа – Документация API Aspose.Cells Cloud"
type: docs
url: /ru/comments/get/
aliases: [  /ru/get-comment-from-a-worksheet/ ]
keywords: "Aspose.Cells, комментарий листа, API, GET, Excel"
description: "Узнайте, как извлечь комментарий листа по имени ячейки с помощью API Aspose.Cells Cloud (v3.0). Включает URL-адрес запроса, параметры, пример cURL, данные ответа и фрагменты кода SDK."
weight: 10
ArticleTitle: "Получить комментарий листа – Документация API Aspose.Cells Cloud"
---

Этот REST API извлекает комментарий листа по имени ячейки с использованием **Aspose.Cells Cloud**.

**Необходимые условия:** Для вызова данной операции необходимо включить действительный JWT-токен доступа в заголовке `Authorization` (`Bearer <jwt token>`). Токены можно получить в рамках процесса аутентификации Aspose.Cells Cloud, описанного в [Руководстве по аутентификации](/cells/authentication/).

## API GetWorksheetComment

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение (путь URL / строка запроса) | Описание                                                                 |
| ------------- | ----- | ---------------------------------------- | ------------------------------------------------------------------------ |
| name          | string| Путь URL                                 | Имя файла Excel.                                                         |
| sheetName     | string| Путь URL                                 | Имя листа, содержащего комментарий.                                      |
| cellName      | string| Путь URL                                 | Адрес ячейки (например, **A1**), комментарий которой извлекается.       |
| folder        | string| Строка запроса                           | Путь к папке, в которой хранится документ.                              |
| storageName   | string| Строка запроса                           | Имя службы хранения.                                                     |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Ответ:** API возвращает JSON-объект, содержащий объект `Comment` со следующими полями:

| Поле                       | Тип     | Описание                                                     |
| -------------------------- | ------- | ------------------------------------------------------------ |
| `CellName`                 | string  | Адрес ячейки (например, **A1**).                             |
| `Author`                   | string  | Имя автора комментария.                                      |
| `HtmlNote`                 | string  | Содержимое комментария в формате HTML (если имеется).       |
| `Note`                     | string  | Текстовое представление комментария в обычном тексте.       |
| `AutoSize`                 | boolean | Указывает, включено ли автоматическое изменение размера поля комментария. |
| `IsVisible`                | boolean | Определяет, отображается ли комментарий.                    |
| `Width`                    | integer | Ширина поля комментария (в символах).                        |
| `Height`                   | integer | Высота поля комментария (в символах).                        |
| `TextHorizontalAlignment` | string  | Горизонтальное выравнивание текста (например, **Bottom**).  |
| `TextOrientationType`      | string  | Ориентация текста (например, **TopToBottom**).              |
| `TextVerticalAlignment`    | string  | Вертикальное выравнивание текста (например, **Bottom**).    |

## Типичные ошибки

- **401 Unauthorized (Неавторизован)** – Убедитесь, что JWT-токен действителен, не истёк и правильно указан в заголовке `Authorization`.
- **404 Not Found (Не найдено)** – Убедитесь, что имя файла, имя листа и адрес ячейки указаны корректно и что файл существует в указанной папке/хранилище.
- **500 Internal Server Error (Внутренняя ошибка сервера)** – Проверьте тело запроса на наличие некорректных данных и убедитесь, что сервис функционирует корректно.

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                                    |
|-----|-----------------------------|-------------------------------------------------------------|
| 200 | OK (ОК)                    | Фильтр применён успешно; ответ содержит детали операции.   |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий JWT-токен.              |
| 413 | Payload Too Large (Слишком большой объём данных) | Загруженный файл превышает допустимый размер.              |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                             |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}