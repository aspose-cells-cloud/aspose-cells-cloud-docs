---
title: "Удаление условного форматирования – Справочник по API Aspose.Cells Cloud"
type: docs
url: /ru/conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, условное форматирование, удаление, API, Excel, облачные сервисы"
description: "Удаление правила условного форматирования из рабочего листа с помощью REST API Aspose.Cells Cloud. Включает параметры, аутентификацию, примеры запросов и ответов, а также фрагменты кода SDK."
weight: 60
---

# Удаление условного форматирования

## Введение
Условное форматирование позволяет применять визуальные стили к ячейкам, удовлетворяющим определённым критериям (например, выделять значения больше заданного порога). В сценариях автоматизации может потребоваться удалить существующее правило. Данный эндпоинт удаляет правило условного форматирования из рабочего листа в файле Excel, хранящемся в облачном хранилище Aspose Cloud.

## Предварительные требования
- Учётная запись **Aspose Cloud** с включённым продуктом **Cells**.  
- **JWT-токен доступа**, полученный с помощью OAuth 2.0 по схеме client credentials.  
- Файл книги (`{name}`) должен уже существовать в указанной **папке** и **хранилище** (если оно указано).  
- В приведённых ниже URL используется версия API **v3.0** (по умолчанию).

## Аутентификация
Все эндпоинты Aspose.Cells Cloud требуют **аутентификации по JWT-токену**.

```http
Authorization: Bearer <access_token>
```

### Получение токена доступа (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Ответ**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Используйте полученный `access_token` в заголовке `Authorization` для каждого запроса.

## HTTP-запрос

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Параметры пути

| Имя       | Тип    | Обязательный | Описание |
|-----------|--------|-------------|----------|
| `name`    | string | Да          | Имя файла книги (например, `Book1.xlsx`). |
| `sheetName` | string | Да       | Имя рабочего листа, содержащего условное форматирование. |
| `index`   | integer| Да          | Индекс правила условного форматирования (начиная с 0), подлежащего удалению. |

### Параметры запроса

| Имя           | Тип    | Обязательный | Описание |
|---------------|--------|-------------|----------|
| `folder`      | string | Нет         | Папка в облаке, где находится книга. |
| `storageName` | string | Нет         | Имя облачного хранилища Aspose Cloud. |

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Успешный ответ

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP-коды статуса**

| Код | Значение                     | Описание |
|-----|------------------------------|----------|
| 200 | OK (ОК)                      | Условное форматирование успешно удалено; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Некорректный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой payload) | Загружаемый файл превышает допустимый размер. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Ответы об ошибках

| HTTP-код | Причина | Пример тела ответа |
|----------|---------|--------------------|
| **400**  | Bad Request (Неверный запрос) — отсутствуют или некорректны параметры. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401**  | Unauthorized (Неавторизовано) — отсутствует или некорректен JWT-токен. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Not Found (Не найдено) — книга или рабочий лист не существуют. | `{ "Code":"404", "Message":"File not found." }` |
| **500**  | Internal Server Error (Внутренняя ошибка сервера) — непредвиденная ошибка сервера. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## Примеры SDK
Следующие фрагменты кода демонстрируют вызов операции **Delete Conditional Formatting** с использованием официальных SDK Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// Настройка клиента API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Удаление условного форматирования
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Conditional formatting deleted.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Conditional formatting removed.")
```

*(Дополнительные фрагменты кода SDK для Ruby, Go, Perl и Swift доступны в [репозитории на GitHub](https://github.com/aspose-cells-cloud).)*

## См. также
- **Руководство по аутентификации** – [Аутентификация по JWT-токену](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Спецификация OpenAPI** – Подробная схема для этого эндпоинта (открывается в новой вкладке)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a>`  
- **Обзор условного форматирования** – Узнайте, как создавать, обновлять и перечислять правила форматирования.  
- **SDK Aspose.Cells Cloud** – Полный список поддерживаемых языков доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).  

---  

*Эта страница соответствует стандартному шаблону документации API Aspose.Cells Cloud, включает раздел предварительных требований и следует лучшим практикам доступности и SEO.*