---
title: "Как получить содержимое диапазона из рабочего листа Excel"
second_title: "Документ"
linktitle: "Получить"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, получить, диапазон, электронная таблица, REST"
description: "Узнайте, как получить содержимое диапазона из рабочего листа Excel с использованием Aspose.Cells Cloud REST API. Включает синтаксис запроса и примеры кода."
weight: 20
ArticleTitle: "Как получить содержимое диапазона из рабочего листа Excel — API Aspose.Cells Cloud"
---

## Работа с получением содержимого диапазона в рабочем листе Excel

- [Как получить данные ячеек на основе именованного диапазона](/cells/ranges/get/values/)
- [Как получить именованный диапазон из книги Excel](/cells/ranges/get/name/)

**Необходимые условия**

- Действующий токен доступа Aspose Cloud (или `client_id`/`client_secret` для OAuth).
- Файл Excel должен быть загружен в целевую папку хранилища.
- Aspose.Cells Cloud SDK версии 3.0 или выше.

Операция **Get Range** («Получить диапазон») возвращает содержимое указанного диапазона рабочего листа.  
Это простой запрос `GET`, возвращающий данные диапазона в формате JSON (или другом формате по запросу).

**Обзор запроса**

| Элемент | Значение |
|---------|----------|
| **Метод HTTP** | `GET` |
| **Конечная точка** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Параметры пути** | `fileName` – имя файла Excel (с расширением) <br> `sheetName` – имя рабочего листа <br> `rangeName` – имя диапазона (например, `A1:B10`) |
| **Параметры запроса** (необязательные) | `folder` – папка хранилища <br> `storage` – имя хранилища <br> `outFormat` – формат ответа (например, `json`, `xml`) |
| **Заголовки** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Пример cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**Пример на C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Пример на Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Пример на Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Схема ответа (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|-----|------------------------------|-----------------------------------------------|
| 200 | OK (OK)                      | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

- `200 OK` – диапазон успешно получен.  
- `400 Bad Request` – отсутствуют или недопустимы параметры.  
- `401 Unauthorized` – недействительный или отсутствующий токен доступа.  
- `404 Not Found` – указанный файл, рабочий лист или диапазон не найдены.  
- `500 Internal Server Error` – непредвиденная ошибка сервера.

**Примеры ответов об ошибках**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "Параметры запроса недействительны или отсутствуют."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Токен доступа недействителен или отсутствует."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "Указанный файл, рабочий лист или диапазон не найдены."
}
```

**См. также**

- [Как получить данные ячеек на основе именованного диапазона](/cells/ranges/get/values/)  
- [Как получить именованный диапазон из книги Excel](/cells/ranges/get/name/)  
- [Обновить содержимое диапазона](/cells/ranges/update/)  
- [Удалить диапазон](/cells/ranges/delete/)  
---