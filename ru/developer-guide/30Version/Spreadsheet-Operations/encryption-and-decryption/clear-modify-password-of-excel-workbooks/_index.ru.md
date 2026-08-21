---
title: "Удаление защиты от записи (пароля) из рабочей книги Excel"
second_title: "Документ"
linktitle: "Очистка пароля файлов Excel"
type: docs
url: /clear-excel-files-password/
aliases:
  [
    /clear-modify-password-of-excel-workbooks/,
    /workbook/clear-modify-password/, /workbook/password/clear/,
  ]
keywords: "Aspose.Cells, Excel, удаление пароля, защита от записи, REST API, примеры SDK"
description: "Узнайте, как удалить защиту от записи (пароль) из рабочей книги Excel с помощью Aspose.Cells Cloud REST API. Включает пример cURL, шаги аутентификации и примеры кода SDK."
weight: 110
ArticleTitle: "Удаление защиты от записи (пароля) из рабочей книги Excel"
---

Этот REST API удаляет **защиту от записи (пароль)** из рабочей книги Excel, позволяя программно **удалить защиту паролем Excel**.

**Необходимые условия:** Получите действительный JWT-токен, убедитесь, что рабочая книга хранится в поддерживаемом хранилище, и используйте версию API v3.0.

Для добавления защиты см. руководство [Защита Excel](/cells/protect/).

## API DeleteDocumentUnprotectFromChanges

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра  | Тип    | Расположение | Описание                                      |
| -------------- | ------ | ------------ | --------------------------------------------- |
| `name`         | string | path         | Имя рабочей книги Excel.                      |
| `folder`       | string | query        | Папка, содержащая рабочую книгу (необязательно). |
| `storageName`  | string | query        | Имя сервиса хранилища (необязательно).         |

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статусов**

| Код  | Значение                    | Описание                                             |
|------|-----------------------------|------------------------------------------------------|
| 200  | OK                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400  | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Неверный или отсутствующий JWT-токен.                |
| 413  | Payload Too Large           | Загруженный файл превышает лимит размера.            |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                       |

## Как использовать API DeleteDocumentUnprotectFromChanges с SDK

### Спецификация API DeleteDocumentUnprotectFromChanges

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges) определяет общедоступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для лёгкого доступа к сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов REST API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
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


### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}