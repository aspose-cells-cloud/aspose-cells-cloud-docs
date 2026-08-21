---
title: "Получение имен из рабочей книги Excel"
second_title: "Документ"
linktitle: "Имена"
type: docs
url: /ru/get-names-from-an-excel-file/
aliases:
  [
    "/ru/get-names-count-from-excel-workbooks/",
    "/ru/workbook/names/",
    "/ru/workbook/get/names/",
  ]
keywords: "Aspose.Cells, Cloud, Excel, Workbook, Names, REST API, SDK"
description: "Получение всех определенных имен из рабочей книги Excel с помощью Aspose.Cells Cloud REST API. Включает руководство по аутентификации, пример cURL, схему ответа, обработку ошибок и примеры SDK."
weight: 120
ArticleTitle: "Получение имен из рабочей книги Excel – Aspose.Cells Cloud API"
---

Этот REST API позволяет получить определенные имена из рабочей книги Excel.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются безопасными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

## API GetWorkbookNames

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

Параметры запроса:

| Имя параметра | Тип    | Расположение | Описание                                |
|---------------|--------|--------------|-----------------------------------------|
| name          | string | path         | Имя файла рабочей книги.                |
| folder        | string | query        | Папка, содержащая рабочую книгу.        |
| storageName   | string | query        | Имя используемого хранилища.            |

Запрос должен включать следующие HTTP-заголовки:

| Заголовок     | Тип    | Описание                                      |
|---------------|--------|-----------------------------------------------|
| Authorization | string | Bearer JWT-токен (обязательный)               |
| Accept        | string | `application/json`                            |
| Content-Type  | string | `application/json` (для запросов с телом)     |

**Аутентификация** – API требует OAuth2/JWT bearer-токен. Получите токен по адресу `https://api.aspose.cloud/connect/token`, используя ваш client-id и client-secret, затем включайте заголовок `Authorization: Bearer <jwt token>` в каждый запрос.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует, как вызвать API Aspose.Cells Cloud с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_Поля ответа_

- **Status** _(string)_ – Сообщение о статусе выполнения операции.
- **Names.link** _(object)_ – Информация о гиперссылке на коллекцию.
- **Names.Count** _(integer)_ – Общее количество возвращённых определённых имён.
- **Names.NameList** _(array)_ – Список объектов имён; каждый объект содержит объект **link** с информацией для навигации.

**Обработка ошибок** – Сервис может возвращать следующие HTTP-коды статуса:

| Код | Значение                    | Рекомендуемое действие                                         |
|-----|-----------------------------|---------------------------------------------------------------|
| 401 | Неавторизовано              | Убедитесь, что предоставлен корректный JWT-токен.             |
| 404 | Не найдено                  | Проверьте правильность имени рабочей книги, папки и хранилища. |
| 500 | Внутренняя ошибка сервера   | Повторите запрос позже или свяжитесь со службой поддержки Aspose, если проблема сохраняется. |

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на вашем проекте. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}