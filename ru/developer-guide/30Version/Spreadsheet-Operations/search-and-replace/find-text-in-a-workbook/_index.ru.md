---
title: "Поиск текста в рабочей книге Excel"
second_title: "Документ"
linktitle: "Поиск в рабочей книге"
type: docs
url: /ru/workbook/find-text/
aliases: [  /ru/find-text-in-a-workbook/ ]
weight: 30
keywords: "Aspose.Cells, поиск текста, Excel API, поиск в рабочей книге"
description: "Узнайте, как использовать Aspose.Cells Cloud API для **поиска текста** в рабочих книгах Excel (XLS‑X, ODS). Приведены примеры cURL, фрагменты кода SDK и схема ответа. Начните работу уже сегодня."
ArticleTitle: "Поиск текста в рабочей книге Excel с помощью Aspose.Cells Cloud API"
---

Этот REST API выполняет поиск текста в рабочей книге Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/findText
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.


### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                                                |
| -------------- | ------ | -------- | ---------------------------------------------------------- |
| name           | string | path     | Имя рабочей книги Excel.                                |
| text           | string | query    | Искомая строка текста.                                 |
| folder         | string | query    | Папка, содержащая рабочую книгу (необязательно).              |
| storageName    | string | query    | Имя хранилища, в котором находится рабочая книга (необязательно). |

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

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                          | Фильтр применён успешно; ответ содержит данные об операции. |
| 400  | Bad Request (Неверный запрос)                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано)                | Неверный или отсутствующий токен JWT. |
| 413  | Payload Too Large (Слишком большой полезный груз)           | Размер загруженного файла превышает ограничение. |
| 500  | Internal Server Error (Внутренняя ошибка сервера)       | Непредвиденная ошибка сервера. |
## Как использовать API PostWorkbooksTextSearch с SDK

### Спецификация API PostWorkbooksTextSearch

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksTextSearch" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступное программное интерфейсное API и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки cURL. В следующем примере показано, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/findText?text=a" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <your_access_token>"
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

Использование SDK — это самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на вашем проекте. Полный список SDK Aspose.Cells Cloud приведён в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории на GitHub</a>.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}
---