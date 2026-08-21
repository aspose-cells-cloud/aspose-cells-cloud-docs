---
title: "Получение одной строки из рабочего листа Excel с использованием API Aspose.Cells Cloud"
description: "Узнайте, как получить определённую строку из рабочего листа Excel, хранящегося в облачном хранилище Aspose Cloud, с использованием REST API Aspose.Cells Cloud. Включает синтаксис запроса, параметры, схему ответа, пример cURL и код SDK (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, получение строки, Excel API, spreadsheet REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# Получение одной строки из рабочего листа Excel

**Конечная точка**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Получает строку из рабочего листа, хранящегося в облачном хранилище Aspose Cloud. Для выполнения операции требуется действующий токен доступа OAuth 2.0 с областью **Read** (Чтение).

---

## Содержание
1. [Необходимые условия](#prerequisites)  
2. [HTTP-запрос](#http-request)  
3. [Параметры](#parameters)  
   - [Параметры пути](#path-parameters)  
   - [Параметры запроса](#query-parameters)  
4. [Пример cURL](#curl-example)  
5. [Ответ](#response)  
   - [Схема успешного ответа](#success-schema)  
   - [Коды статусов](#status-codes)  
6. [Примеры кода SDK](#sdk-code-samples)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [Связанные операции](#related-operations)  
8. [Примечания и ограничения](#notes--limits)  

---

## Необходимые условия
- **Учётная запись Aspose Cloud** с активной подпиской.  
- **Токен доступа OAuth 2.0** с областью **Read** (Чтение).  
- Целевая рабочая книга должна уже существовать в облачном хранилище Aspose Cloud.  

---

## HTTP-запрос
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*Базовый URL*: `https://api.aspose.cloud/v3.0`

---

## Параметры

### Параметры пути
| Имя       | Тип    | Обязательный | Описание                                      |
|-----------|--------|-------------|-----------------------------------------------|
| `name`    | string | ✅          | Имя файла рабочей книги (например, `MyWorkbook.xlsx`). |
| `sheetName`| string | ✅         | Имя рабочего листа (например, `Sheet1`).     |
| `rowIndex`| integer| ✅          | Индекс строки (начиная с 0), которую нужно получить. |

### Параметры запроса *(необязательные)*
| Имя            | Тип    | Обязательный | Описание                                               |
|----------------|--------|-------------|--------------------------------------------------------|
| `folder`       | string | ❌          | Путь к папке в облачном хранилище, где хранится рабочая книга. |
| `storageName`  | string | ❌          | Имя сервиса хранилища (если используется пользовательское хранилище). |

---

## Пример cURL
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Ответ

### Схема успешного ответа (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* объект стиля */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...дополнительные ячейки... */
    ]
  }
}
```

### Коды статусов
| Код | Значение |
|-----|----------|
| **200** | Строка успешно получена. |
| **401** | Неавторизован — отсутствует или недействителен токен доступа. |
| **404** | Рабочая книга, рабочий лист или строка не найдены. |
| **500** | Внутренняя ошибка сервера. |

### Пример ошибки (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Access token is missing or invalid."
}
```

---

## Примеры кода SDK

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // необязательно
);

Console.WriteLine($"Row {response.Row.Index} retrieved with {response.Row.Cells.Count} cells.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – необязательно
);

System.out.println("Row index: " + response.getRow().getIndex());
System.out.println("Cells count: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Row {response.row.index} retrieved with {len(response.row.cells)} cells.")
except ApiException as e:
    print("Exception when calling CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## Связанные операции
| Операция | Описание |
|---------|----------|
| **Добавить строку** | `POST /cells/{name}/worksheets/{sheetName}/rows` – вставить новую строку в рабочий лист. |
| **Удалить строку** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – удалить существующую строку. |
| **Получить несколько строк** | `GET /cells/{name}/worksheets/{sheetName}/rows` – получить набор строк. |
| **Обзор строк** | `/cells/rows/` – общая документация по конечным точкам, связанным со строками. |

---

## Примечания и ограничения
- **Ограничение частоты запросов**: 100 запросов в минуту на одну учётную запись.  
- **Поддерживаемые форматы**: XLS, XLSX, CSV, ODS.  
- Индекс строки — **нулевой** (первый индекс — `0`).  
- Убедитесь, что рабочая книга загружена в указанную папку `folder` до вызова данной конечной точки.  

---