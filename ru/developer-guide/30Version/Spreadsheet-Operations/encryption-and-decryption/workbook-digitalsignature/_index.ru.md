---
title: "Добавление цифровой подписи в рабочую книгу Excel"
ArticleTitle: "Добавление цифровой подписи в рабочую книгу Excel – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Цифровая подпись"
type: docs
url: /ru/excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud, цифровая подпись, рабочая книга Excel, REST API, .pfx, JWT, API для подписи"
description: "Узнайте, как добавить цифровую подпись в рабочую книгу Excel с помощью REST API Aspose.Cells Cloud (версия 4.0). Включает адрес конечной точки, параметры, аутентификацию, схему ответа, обработку ошибок и примеры SDK для нескольких языков."
weight: 35
---


**Необходимые условия:**  
Перед вызовом данной конечной точки убедитесь, что у вас имеются:

- Действующий JWT-токен доступа, полученный в результате аутентификации в Aspose Cloud.  
- Целевая рабочая книга, загруженная в ваше облачное хранилище Aspose Cloud.  
- Файл цифровой подписи в формате `.pfx` или `.p12`, а также его пароль.

Данный REST API добавляет **цифровую подпись** к рабочей книге Excel.

## API PostDigitalSignature

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра            | Тип    | Расположение         | Описание                                               |
| ------------------------ | ------ | -------------------- | ------------------------------------------------------ |
| **name**                 | string | `<code>path</code>`  | Имя рабочей книги.                                     |
| **digitalsignaturefile** | string | `<code>query</code>` | Путь к файлу цифровой подписи (`.pfx` или `.p12`).    |
| **password**             | string | `<code>query</code>` | Пароль к рабочей книге, если она защищена.            |
| **folder**               | string | `<code>query</code>` | Папка, в которой хранится рабочая книга.              |
| **storageName**          | string | `<code>query</code>` | Имя используемого облачного хранилища.                 |

*Примечание: Если имя файла содержит специальные символы, выполните его URL-кодирование перед добавлением в строку запроса.*

### Обработка ошибок

| HTTP-статус | Значение                                               |
| ----------- | ------------------------------------------------------ |
| 200         | Подпись успешно применена.                             |
| 400         | Неверный запрос — отсутствуют или некорректны параметры. |
| 401         | Неавторизован — недействительный или просроченный OAuth-токен. |
| 403         | Доступ запрещён — недостаточно прав или отказ в доступе. |
| 500         | Внутренняя ошибка сервера — непредвиденная ошибка.     |

### Ответы с ошибками по HTTP-статусам

| HTTP-статус | Код ошибки          | Описание                                                |
| ----------- | ------------------- | ------------------------------------------------------- |
| 400         | BadRequest          | Отсутствуют или некорректны параметры.                  |
| 401         | Unauthorized        | Недействительный или отсутствующий токен доступа.      |
| 404         | NotFound            | Указанная рабочая книга не найдена в указанной папке/хранилище. |
| 500         | InternalServerError | Непредвиденная ошибка сервера.                          |


## Как использовать API PostDigitalSignature с SDK

### Спецификация API PostDigitalSignature

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для вызова веб-сервисов Aspose.Cells. Пример ниже демонстрирует запрос к API:

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
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

**Схема ответа**  
API возвращает JSON-объект со следующими полями:

| Поле         | Тип    | Описание                                            |
| ------------ | ------ | --------------------------------------------------- |
| `Code`       | int    | Код HTTP-подобного статуса, указывающий результат.  |
| `Status`     | string | Краткое текстовое описание результата (например, `OK`). |
| `SignatureId`| string | Идентификатор применённой цифровой подписи (опционально). |
| `Message`    | string | Дополнительная информация или детали ошибки (опционально). |

### Использование SDK Aspose.Cells Cloud

Использование SDK упрощает интеграцию и снижает объём шаблонного кода. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}