---
title: "Удаление всех проверок данных листа — Aspose.Cells Cloud API"
second_title: "Документация"
linktitle: "Удалить"
type: docs
url: /ru/validations/clear/
keywords: "Aspose.Cells Cloud, удаление проверок данных листа, Excel, REST API, проверка электронной таблицы, API"
description: "Удалите все правила проверки данных с листа в файле Excel с помощью Aspose.Cells Cloud REST API. Включает шаги аутентификации, детали запроса, пример cURL, схему ответа, обработку ошибок и фрагменты SDK."
weight: 10
---

**Необходимые условия**

- Действующая учетная запись Aspose Cloud.
- JWT-токен доступа, полученный через API аутентификации Aspose Cloud (`/connect/token`).
- Рабочая книга должна храниться в вашем хранилище Aspose Cloud (или должны быть предоставлены соответствующие параметры запроса `folder`/`storageName`).

Этот REST API удаляет все проверки данных листа в листе Excel.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                          |
| ------------- | ------ | ------------ | ------------------------------------------------- |
| name          | string | path         | Имя документа Excel.                              |
| sheetName     | string | path         | Имя листа, содержащего проверки данных.           |
| folder        | string | query        | Папка, в которой хранится документ.               |
| storageName   | string | query        | Имя сервиса хранилища.                            |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) определяет публично доступное программное интерфейсное решение и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать инструмент командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать API с помощью cURL после получения JWT-токена.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Обработка ошибок

| HTTP-статус | Смысл ошибки       | Описание                                                  |
| ----------- | ------------------ | --------------------------------------------------------- |
| 400         | Bad Request        | Запрос некорректно сформирован или отсутствуют обязательные параметры. |
| 401         | Unauthorized       | JWT-токен отсутствует, недействителен или истек.          |
| 404         | Not Found          | Указанная рабочая книга или лист не существуют.           |
| 500         | Internal Server Error | На стороне сервера произошла непредвиденная ошибка.      |

Полезная нагрузка ошибки следует той же структуре JSON с полями `Code` и `Message`, например:

```json
{
  "Code": 401,
  "Message": "Invalid or expired token."
}
```

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает детали низкоуровневой реализации, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}