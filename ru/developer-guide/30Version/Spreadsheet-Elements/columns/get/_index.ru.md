---
title: Получить сведения о столбце – Справочник по API Aspose.Cells Cloud (v4.0)
description: Получите подробную информацию о столбце рабочего листа (индекс, ширина, стиль, состояние скрытия) с помощью Aspose.Cells Cloud REST API.
keywords: Aspose.Cells, облачный API, столбец Excel, получить столбец, REST API, JWT, рабочий лист
date: 2026-07-30
---

# Получить сведения о столбце  

Получите подробную информацию о конкретном столбце рабочего листа (индекс, ширина, стиль, состояние скрытия) из файла рабочей книги Excel, хранящегося в Aspose Cloud.

## Оглавление
1. [Необходимые условия](#prerequisites)  
2. [Аутентификация](#authentication)  
3. [Конечная точка](#endpoint)  
4. [Параметры запроса](#request-parameters)  
5. [Пример cURL](#curl-example)  
6. [Пример ответа](#response-example)  
7. [Схема ответа](#response-schema)  
8. [Возможные ошибки](#possible-errors)  
9. [Примеры SDK](#sdk-examples)  
10. [Дополнительные ресурсы](#additional-resources)  

---

## Необходимые условия
- Действующий **JWT-токен доступа**, полученный с помощью аутентификации Aspose Cloud.  
- Файл рабочей книги должен храниться в облачном хранилище Aspose Cloud (или в другом поддерживаемом хранилище), и путь к папке (если есть) должен быть известен.  

---

## Аутентификация
Все API Aspose.Cells Cloud используют **аутентификацию на основе JWT-токенов**. Включите токен в заголовок `Authorization`:

```http
Authorization: Bearer <access_token>
```

Дополнительные сведения о получении токена см. в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Конечная точка
```
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}
```

- **{name}** – имя файла рабочей книги (например, `test.xlsx`).  
- **{sheetName}** – имя рабочего листа (например, `Sheet1`).  
- **{columnIndex}** – индекс столбца (начиная с 0) для получения данных.

---

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токенов</a>.

## Параметры запроса

| Название          | Расположение | Тип    | Обязательный | Описание |
|-------------------|--------------|--------|-------------|----------|
| **name**          | путь         | string | Да          | Имя файла рабочей книги. |
| **sheetName**     | путь         | string | Да          | Рабочий лист, содержащий столбец. |
| **columnIndex**   | путь         | integer| Да          | Индекс столбца (начиная с 0) для получения данных. |
| **folder**        | запрос       | string | Нет         | Папка хранилища, в которой находится рабочая книга. |
| **storageName**   | запрос       | string | Нет         | Имя службы хранилища (например, Aspose Cloud Storage). |

---

## Пример cURL
```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0?folder=MyFolder&storageName=MyStorage" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

---

## Пример ответа
```json
{
  "Column": {
    "GroupLevel": 0,
    "Index": 0,
    "IsHidden": false,
    "Width": 8.5,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v4.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

---

## Схема ответа
| Поле                 | Тип     | Описание |
|----------------------|---------|----------|
| `Column.GroupLevel`  | integer | Уровень свертки столбца (используется для группировки). |
| `Column.Index`       | integer | Индекс столбца (начиная с 0). |
| `Column.IsHidden`    | boolean | `true`, если столбец скрыт; иначе `false`. |
| `Column.Width`       | number  | Ширина столбца, выраженная в символах. |
| `Column.Style`       | object  | Содержит `ссылку` на ресурс стиля столбца. |
| `Column.link`        | object  | Самоссылка на ресурс столбца. |
| `Code`               | integer | Код HTTP-статуса ответа. |
| `Status`             | string  | Текстовое описание статуса (например, **OK**). |

---

## Возможные ошибки
| HTTP-статус | Код | Сообщение              | Когда возникает |
|-------------|-----|------------------------|-----------------|
| 400         | 400 | Bad Request (Неверный запрос) | Отсутствуют или имеют неверный формат обязательные параметры. |
| 401         | 401 | Unauthorized (Неавторизованный доступ) | Отсутствует или недействителен заголовок `Authorization`. |
| 404         | 404 | Not Found (Не найдено) | Рабочая книга, рабочий лист или столбец не существует. |
| 500         | 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная проблема на стороне сервера. |

### Пример – 404 Not Found
```json
{
  "Code": 404,
  "Message": "Column index out of range."
}
```

### Пример – 401 Unauthorized
```json
{
  "Code": 401,
  "Message": "Invalid or missing authentication token."
}
```

---

## Примеры SDK
Следующие фрагменты кода демонстрируют вызов операции **Get Worksheet Columns** с использованием официальных SDK Aspose.Cells Cloud. Если Gist станет недоступен, пример кода также предоставляется встроенными.

<details><summary>**C#**</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

// Настройка клиента API
var apiInstance = new CellsApi("client_id", "client_secret");

// Установка обязательных параметров
string name = "test.xlsx";
string sheetName = "Sheet1";
int columnIndex = 0;
string folder = "MyFolder";          // необязательно
string storageName = "MyStorage";    // необязательно

try
{
    var response = apiInstance.GetWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
    Console.WriteLine("Column Index: " + response.Column.Index);
    Console.WriteLine("Width: " + response.Column.Width);
}
catch (Exception e)
{
    Console.WriteLine("Exception when calling CellsApi.GetWorksheetColumns: " + e.Message );
}
```

</details>

<details><summary>**Java**</summary>

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.ColumnsResponse;

public class GetWorksheetColumnsExample {
    public static void main(String[] args) {
        CellsApi apiInstance = new CellsApi("client_id", "client_secret");

        String name = "test.xlsx";
        String sheetName = "Sheet1";
        Integer columnIndex = 0;
        String folder = "MyFolder";          // необязательно
        String storageName = "MyStorage";    // необязательно

        try {
            ColumnsResponse result = apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName);
            System.out.println("Column index: " + result.getColumn().getIndex());
            System.out.println("Width: " + result.getColumn().getWidth());
        } catch (Exception e) {
            System.err.println("Exception while calling CellsApi#getWorksheetColumns");
            e.printStackTrace();
        }
    }
}
```

</details>

<details><summary>**Python**</summary>

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "client_id"
config.client_secret = "client_secret"

api_instance = CellsApi(ApiClient(config))

name = "test.xlsx"
sheet_name = "Sheet1"
column_index = 0
folder = "MyFolder"       # необязательно
storage_name = "MyStorage"  # необязательно

try:
    response = api_instance.get_worksheet_columns(name, sheet_name, column_index, folder, storage_name)
    print("Column index:", response.column.index)
    print("Width:", response.column.width)
except Exception as e:
    print("Exception when calling CellsApi->get_worksheet_columns:", e)
```

</details>

<details><summary>**Node.js (TypeScript)**</summary>

```typescript
import { CellsApi, Configuration } from "@asposecloud/cells-sdk";

const config = new Configuration({
    clientId: "client_id",
    clientSecret: "client_secret"
});
const apiInstance = new CellsApi(config);

const name = "test.xlsx";
const sheetName = "Sheet1";
const columnIndex = 0;
const folder = "MyFolder";       // необязательно
const storageName = "MyStorage"; // необязательно

apiInstance.getWorksheetColumns(name, sheetName, columnIndex, folder, storageName)
    .then((result) => {
        console.log("Column index:", result.column?.index);
        console.log("Width:", result.column?.width);
    })
    .catch((error) => {
        console.error("Error calling getWorksheetColumns:", error);
    });
```

</details>

> **Примечание:** Все SDK автоматически обрабатывают заголовок `Authorization` после предоставления `client_id` и `client_secret`.

---

## Дополнительные ресурсы
- **Спецификация OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetColumns>  
- **Руководство по аутентификации:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
- **Репозиторий GitHub (SDK и примеры):** <https://github.com/aspose-cells-cloud>  

---

*Документ последний раз обновлен 2026‑07‑30.*