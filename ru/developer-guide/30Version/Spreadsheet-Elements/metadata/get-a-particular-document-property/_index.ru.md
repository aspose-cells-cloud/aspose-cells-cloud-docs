---
title: "Получение конкретного свойства документа"
second_title: "Документ"
linktitle: "Получить"
type: docs
url: /ru/document-properties/get/
aliases: [  /ru/get-a-particular-document-property/ ]
keywords: "Aspose.Cells, облачный API, получение свойства документа, метаданные Excel, REST GET, примеры SDK"
description: "Получение именованного свойства документа (например, Автор, Заголовок) из файла Excel с использованием облачного REST API Aspose.Cells. Включает пример cURL, фрагменты кода SDK и схему ответа."
weight: 20
---

Этот REST API позволяет получить свойство документа по его имени.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Параметры запроса

| Имя параметра  | Тип    | Расположение | Описание                                           |
| -------------- | ------ | ------------ | -------------------------------------------------- |
| name           | string | path         | Имя файла Excel.                                   |
| propertyName   | string | path         | Имя свойства документа, которое необходимо получить. |
| folder         | string | query        | Папка, содержащая файл (необязательно).            |
| storageName    | string | query        | Имя хранилища (необязательно).                     |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Подробности ответа

JSON-объект, возвращаемый API, содержит следующие поля:

| Поле                            | Тип     | Описание                                                     |
| ------------------------------- | ------- | ------------------------------------------------------------ |
| **DocumentProperty.Name**       | string  | Имя свойства (например, `Author`).                            |
| **DocumentProperty.Value**      | string  | Значение свойства. Может быть пустым, если оно не задано.     |
| **DocumentProperty.BuiltIn**    | boolean | Указывает, является ли свойство встроенным свойством Excel.  |
| **DocumentProperty.link.Href**  | string  | Относительный URL ресурса свойства.                           |
| **DocumentProperty.link.Rel**   | string  | Тип связи, обычно `self`.                                     |
| **DocumentProperty.link.Title** | string  | Человекочитаемое название (может быть `null`).               |
| **DocumentProperty.link.Type**  | string  | MIME-тип связанного ресурса (может быть `null`).             |
| **Code**                        | integer | Код HTTP-статуса, возвращаемый сервисом.                      |
| **Status**                      | string  | Текстовое описание статуса (например, `OK`).                  |

### Ответы об ошибках

| HTTP-статус | Код                    | Описание                                                   |
| ----------- | ---------------------- | ---------------------------------------------------------- |
| 400         | `InvalidParameter`     | Один или несколько параметров запроса недопустимы.        |
| 401         | `AuthenticationFailed` | Отсутствует или недействителен JWT-токен.                 |
| 404         | `PropertyNotFound`     | Указанное свойство документа не существует.                |
| 500         | `InternalError`        | На сервере произошла непредвиденная ошибка.                |

Типовое тело ошибки выглядит следующим образом:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Терминология

| Термин                | Определение                                                                                     |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| **Свойство документа** | Часть метаданных, связанная с рабочей книгой Excel (например, Автор, Заголовок, Создано).      |
| **Метаданные**        | Общий термин для данных, описывающих другие данные; в данном контексте означает свойства документа. |
| **Пользовательское свойство** | Свойство, определённое пользователем и не входящее в набор встроенных свойств.              |

### Часто задаваемые вопросы

**В:** _Как получить свойство Автор файла Excel, хранящегося в Aspose Cloud?_  
**О:** Отправьте GET-запрос по адресу `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` с действующим Bearer-токеном. JSON-ответ будет содержать `DocumentProperty.Name = "Author"` и его `Value`.

**В:** _Какая ошибка возвращается, если запрошенное свойство не существует?_  
**О:** API возвращает HTTP 404 с JSON-телом, содержащим `Code: 404` и `Status: "Property not found"`.

**В:** _Нужно ли указывать `storageName`, если файл находится в хранилище по умолчанию?_  
**О:** Нет. Параметр запроса `storageName` является необязательным; пропустите его, чтобы использовать хранилище по умолчанию, настроенное для вашей учётной записи.