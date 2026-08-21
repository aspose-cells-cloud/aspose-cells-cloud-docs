---
title: "Получить описание строки из рабочего листа Excel"
second_title: "Document"
linktitle: "Row"
type: docs
url: /rows/get/row/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, API строк Excel, получить строку рабочего листа, REST API, .NET SDK, Java SDK, Python SDK"
description: "Получить подробную информацию (высоту, стиль, состояние скрытия и т.д.) для конкретной строки в рабочем листе Excel с использованием Aspose.Cells Cloud REST API. Включает пример curl, фрагменты кода SDK и обработку ошибок."
weight: 10
ArticleTitle: "Получить описание строки из рабочего листа Excel – API Aspose.Cells Cloud"
---

**Необходимые условия:**  
- Получить действительный JWT-токен доступа и включить его в заголовок `Authorization: Bearer <jwt token>`.  
- Убедиться, что книга сохранена в облачном хранилище Aspose, либо указать путь к папке, где она расположена.  
- Использовать версию API **v3.0**, как показано в URL-адресе конечной точки.

Этот REST API извлекает данные строки по её индексу в рабочем листе Excel.

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются безопасными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                              |
|---------------|--------|-------------|-------------------------------------------------------|
| name          | string | path        | Имя файла книги.                                      |
| sheetName     | string | path        | Имя рабочего листа в книге.                          |
| rowIndex      | integer| path        | Индекс строки для извлечения (начинается с 0).        |
| folder        | string | query       | Папка, содержащая книгу.                             |
| storageName   | string | query       | Имя хранилища, в котором находится книга.            |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) определяет общедоступное программное API-интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL. Включите заголовок `Authorization: Bearer <jwt token>` для аутентификации запроса.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Схема ответа**

| Свойство          | Тип     | Описание                                                               |
|-------------------|---------|------------------------------------------------------------------------|
| `GroupLevel`      | integer | Уровень свертывания строки (используется для группировки).              |
| `Height`          | number  | Высота строки в пунктах.                                               |
| `Index`           | integer | Индекс возвращённой строки (начинается с 0).                           |
| `IsBlank`         | boolean | Указывает, содержит ли строка какие-либо данные.                      |
| `IsHeightMatched`| boolean | `true`, если высота строки совпадает с высотой строки по умолчанию.   |
| `IsHidden`        | boolean | `true`, если строка скрыта.                                            |
| `Style`           | object  | Объект, содержащий информацию о стиле строки.                          |
| `link`            | object  | Ссылка (гиперссылка) на ресурс строки.                                 |
| `Code`            | integer | Код HTTP-статуса ответа.                                              |
| `Status`          | string  | Текстовое описание статуса (например, «OK»).                          |

{{< /tab >}}

{{< /tabs >}}

**Примечания / Обработка ошибок:** API может возвращать следующие HTTP-коды состояния:

- **200** – Успех; данные строки возвращены.  
- **401** – Неавторизовано; JWT-токен отсутствует или недействителен.  
- **404** – Не найдено; указанная книга, рабочий лист или строка не существует.  
- **500** – Внутренняя ошибка сервера; возникло непредвиденное состояние.

| Код | Описание                                      | Устранение проблемы                     |
|-----|-----------------------------------------------|----------------------------------------|
| 200 | Успех – данные строки возвращены.             | —                                      |
| 401 | Неавторизовано – отсутствует или недействителен JWT-токен. | Предоставьте действительный JWT-токен. |
| 404 | Не найдено – книга, рабочий лист или строка отсутствуют. | Проверьте имена и индекс строки.        |
| 500 | Внутренняя ошибка сервера – непредвиденное состояние. | Обратитесь в службу поддержки Aspose.   |

Полный список кодов ошибок см. в документации Aspose.Cells Cloud по [кодам ошибок](https://docs.aspose.cloud/cells/).

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}