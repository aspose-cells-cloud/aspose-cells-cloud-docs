---
title: "Поиск текста в листе Excel"
second_title: "Документ"
linktitle: "Поиск в листе"
type: docs
url: /ru/worksheets/find-text/
aliases: [  /ru/find-text-in-a-worksheet/ ]
weight: 40
keywords: "Excel, Aspose.Cells Cloud, REST API, поиск текста, лист, электронная таблица, поиск"
description: "Используйте REST API Aspose.Cells Cloud для поиска текста в листе Excel. API доступно через множество SDK и языков программирования."
---

Этот REST API позволяет искать текст в листе Excel.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/findText
```


### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.


### Параметры запроса

| Имя параметра | Тип   | Местоположение | Описание                 |
| ------------- | ----- | -------------- | ------------------------- |
| name          | string | path          | Имя документа.           |
| sheetName     | string | path          | Имя листа.               |
| text          | string | query         | Искомый текст.           |
| folder        | string | query         | Папка документа.         |
| storageName   | string | query         | Имя хранилища.           |

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

| Код | Значение                    | Описание                                                   |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK (Успешно)               | Фильтр применён успешно; ответ содержит детали операции.  |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.             |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает допустимый размер.             |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                            |

## Как использовать API PostWorksheetTextSearch с SDK

### Спецификация API PostWorksheetTextSearch

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetTextSearch) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для удобного доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как вызвать Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/findText?text=a" -H "accept: application/json"
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

### Использование SDK Aspose.Cells Cloud

Использование SDK — это самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}