---
title: "Расшифровка рабочей книги Excel"
second_title: "Документ"
linktitle: "Расшифровка файла Excel"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, расшифровка Excel, REST API, облачный SDK"
description: "Узнайте, как расшифровать рабочую книгу Excel с помощью Aspose.Cells Cloud REST API. Включены необходимые параметры, пример cURL, примеры кода SDK и подробности об обработке ошибок."
ArticleTitle: "Как расшифровать рабочую книгу Excel с помощью API Aspose.Cells Cloud"
weight: 50
---

**Необходимые условия**

- Действующий JWT-токен доступа.
- Рабочая книга должна быть загружена в облачное хранилище Aspose, а её путь указан в параметре запроса `folder`.

## API DeleteDecryptWorkbook

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип   | Описание                                     |
| -------------- | ------ | ----------------------------------------------- |
| folder         | string | Путь к папке с исходной рабочей книгой.           |
| storageName    | string | Имя хранилища, в котором находится рабочая книга. |

### Параметр тела запроса

| Имя параметра | Тип                      | Описание                                  |
| -------------- | ------------------------- | -------------------------------------------- |
| encryption     | WorkbookEncryptionRequest | Настройки шифрования, необходимые для расшифровки. |

### WorkbookEncryptionRequest

| Имя параметра | Тип    | Описание                                                                                                   |
| -------------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| EncryptionType | string  | Алгоритм шифрования (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength      | integer | Длина ключа шифрования в битах.                                                                         |
| Password       | string  | Пароль, используемый для расшифровки.                                                                                 |

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Примеры ответов об ошибках**

```json
{
  "Code": "400",
  "Message": "Неверные параметры запроса."
}
```

```json
{
  "Code": "401",
  "Message": "Ошибка аутентификации. Неверный или отсутствующий JWT-токен."
}
```

```json
{
  "Code": "413",
  "Message": "Тело запроса слишком большое. Загруженный файл превышает допустимый размер."
}
```

```json
{
  "Code": "500",
  "Message": "Внутренняя ошибка сервера. Повторите попытку позже."
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос)                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано)                | Неверный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой payload)           | Загруженный файл превышает лимит размера. |
| 500  | Internal Server Error (Внутренняя ошибка сервера)       | Непредвиденная ошибка сервера. |
## Как использовать API DeleteDecryptWorkbook с SDK

### Спецификация API DeleteDecryptWorkbook

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}