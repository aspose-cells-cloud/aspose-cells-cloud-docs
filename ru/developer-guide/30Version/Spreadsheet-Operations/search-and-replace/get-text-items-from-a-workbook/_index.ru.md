---
title: "Получение текстовых элементов из книги Excel"
ArticleTitle: "Получение текстовых элементов из книги Excel с помощью API Aspose.Cells Cloud"
second_title: "Документ"
linktype: "docs"
url: /workbook/get-text-items/
aliases: [/get-text-items-from-a-workbook/]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, Таблица, Получение текстовых элементов, Книга"
description: "Получение текстовых элементов из книги Excel с помощью REST API Aspose.Cells Cloud. Доступно через SDK для C#, Java, Python, PHP, Ruby, Go, Node.js, Perl и Swift."
---


## REST API

Этот REST API извлекает **текстовые элементы** книги из файла Excel.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе JWT-токена</a>.


### Параметры запроса

| Имя параметра | Тип   | Местоположение | Описание                                                  |
|---------------|-------|----------------|-----------------------------------------------------------|
| name          | string | путь           | Имя файла книги.                                          |
| folder        | string | запрос         | Путь к папке в хранилище, где находится книга.           |
| storageName   | string | запрос         | Имя сервиса хранилища.                                    |

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

| Код | Значение                    | Описание                                                       |
|-----|-----------------------------|----------------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр успешно применён; ответ содержит детали операции.      |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                         |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера.                    |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                                |

## Как использовать API GetWorkbookTextItems с помощью SDK

### Спецификация API GetWorkbookTextItems

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) определяет открытый программный интерфейс, позволяющий выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как сделать вызов в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
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

Типичные коды HTTP-статуса ответа:

| Код | Описание                                          |
|-----|---------------------------------------------------|
| 200 | Запрос выполнен успешно; возвращены текстовые элементы. |
| 401 | Неавторизовано — отсутствует или недопустим токен. |
| 403 | Запрещено — недостаточно прав.                    |
| 404 | Не найдено — книга или ресурс не найдены.         |
| 500 | Внутренняя ошибка сервера — непредвиденный сбой.   |

### Использование SDK Aspose.Cells Cloud

Пример использует версию API **v3.0**; для более новых версий обращайтесь к списку изменений. Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}