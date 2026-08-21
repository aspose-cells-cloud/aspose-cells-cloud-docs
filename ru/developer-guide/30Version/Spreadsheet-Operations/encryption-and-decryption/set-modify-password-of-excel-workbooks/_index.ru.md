---
title: "Изменение пароля защиты рабочей книги Excel"
second_title: "Документ"
linktitle: "Изменение пароля файла Excel"
type: docs
url: /ru/workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "пароль Excel, Aspose.Cells Cloud, защита от записи, REST API, изменение пароля рабочей книги"
description: "Изменение пароля защиты от записи для рабочей книги Excel с использованием Aspose.Cells Cloud REST API (v3.0). Включает примеры cURL и SDK."
weight: 100
ArticleTitle: "Изменение защиты паролем рабочей книги Excel — Aspose.Cells Cloud"
---

Этот REST API **изменяет пароль защиты от записи** существующей рабочей книги Excel.

Программное обновление пароля защиты от записи позволяет заменять или обновлять пароли без скачивания файла. Это особенно удобно при управлении защищёнными рабочими книгами, хранящимися в облачном хранилище Aspose.Cells Cloud.


## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Параметры запроса

| Имя параметра   | Тип    | Местоположение | Описание                                      |
| --------------- | ------ | -------------- | --------------------------------------------- |
| **name**        | string | путь           | Имя рабочей книги Excel (обязательно).        |
| **password**    | string | тело (JSON)    | Новый пароль защиты от записи (обязательно).   |
| **folder**      | string | запрос         | Необязательная папка, в которой хранится книга. |
| **storageName** | string | запрос         | Необязательное имя сервиса хранилища.          |

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                      |
|-----|-----------------------------|-----------------------------------------------|
| 200 | OK (ОК)                    | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий токен JWT.         |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера.     |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                |

## Как использовать API PutDocumentProtectFromChanges с SDK

### Спецификация API PutDocumentProtectFromChanges

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) определяет публично доступное программное интерфейсное описание, позволяющее выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать командную утилиту **cURL** для лёгкого доступа к веб-сервисам Aspose.Cells. Приведённая ниже команда cURL показывает, как вызвать облачный API.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
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

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}