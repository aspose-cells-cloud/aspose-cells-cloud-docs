---
title: "Удаление конкретного свойства документа"
second_title: "Документ"
linktitle: "Удалить"
type: docs
url: /document-properties/delete/
aliases: [/remove-a-particular-document-property/]
keywords: "Aspose.Cells, удаление свойства документа, API метаданных Excel, REST, облачный SDK, пример cURL"
description: "Удаление конкретного свойства документа из рабочей книги Excel с использованием Aspose.Cells Cloud REST API v3.0. Включает примеры cURL и SDK для C#, Java, Python и других языков."
weight: 50
---

Этот REST API удаляет свойство документа из рабочей книги.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Параметры запроса

| Имя параметра  | Тип    | Расположение | Обязательный | Описание                                        |
| -------------- | ------ | ------------ | ------------ | ----------------------------------------------- |
| name           | string | путь         | Да           | Имя рабочей книги Excel.                        |
| propertyName   | string | путь         | Да           | Имя удаляемого свойства документа.              |
| folder         | string | параметр запроса | Нет     | Путь к папке, где хранится рабочая книга.      |
| storageName    | string | параметр запроса | Нет     | Имя службы хранения.                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как делать вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Ответы об ошибках

| HTTP-статус | Описание                                                                 | Пример JSON                                                  |
| ----------- | ------------------------------------------------------------------------ | ------------------------------------------------------------ |
| 400         | Неверный запрос — отсутствуют обязательные параметры или недопустимые значения. | `{"Code":400,"Message":"Отсутствует обязательный параметр 'name'."}` |
| 401         | Неавторизовано — недействительный или отсутствующий JWT-токен.          | `{"Code":401,"Message":"Недействительный токен доступа."}`  |
| 404         | Не найдено — рабочая книга или указанное свойство не существует.         | `{"Code":404,"Message":"Свойство документа не найдено."}`    |
| 500         | Внутренняя ошибка сервера — возникло непредвиденное условие на сервере.  | `{"Code":500,"Message":"Произошла непредвиденная ошибка."}`  |

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берет на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells представлен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}