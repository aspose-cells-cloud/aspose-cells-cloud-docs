---
title: "Получение текстовых элементов из рабочего листа Excel"
second_title: "Документ"
linktitle: "Получение текстовых элементов в рабочем листе"
type: docs
url: /ru/worksheets/get-text-items/
aliases: [  /ru/get-text-items-from-a-worksheet/ ]
weight: 20
keywords: "Aspose.Cells, облачный API, Excel, рабочий лист, текстовые элементы, REST"
description: "Получение всех текстовых элементов из конкретного рабочего листа файла Excel с использованием облачного API Aspose.Cells REST. Включает примеры cURL, код SDK, шаги аутентификации и схему ответа."
ArticleTitle: "Получение текстовых элементов из рабочего листа Excel"
---

## REST API

Этот REST API считывает текстовые элементы рабочего листа в файле Excel.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### Безопасность и аутентификация

Облачные API Aspose.Cells защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Параметры запроса


| Имя параметра | Тип   | Расположение | Обязательный | Описание                                         |
|---------------|-------|--------------|-------------|--------------------------------------------------|
| name          | string | path         | Да          | Имя файла рабочей книги.                         |
| sheetName     | string | path         | Да          | Имя рабочего листа.                              |
| folder        | string | query        | Нет         | Путь к папке, содержащей рабочую книгу.         |
| storageName   | string | query        | Нет         | Имя облачного хранилища Aspose.                  |

### **Ответ**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недопустимый или отсутствующий JWT-токен.         |
| 413 | Payload Too Large (Слишком большой запрос) | Загружаемый файл превышает лимит размера.         |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                   |

## Как использовать API GetWorksheetTextItems с SDK

### Спецификация API GetWorksheetTextItems

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK облачной платформы Aspose.Cells

SDK упрощает интеграцию, скрывая детали низкоуровневой работы и позволяя сосредоточиться на задачах вашего проекта. Полный список SDK облачной платформы Aspose.Cells доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"}.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}