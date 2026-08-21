---
title: Добавление динамической фильтрации в лист Excel с помощью API Aspose.Cells Cloud
description: Узнайте, как применить динамическую фильтрацию (например, BelowAverage, Tomorrow, LastMonth) к листу Excel с помощью REST API Aspose.Cells Cloud. Включает аутентификацию, синтаксис запроса, параметры, обработку ответа и примеры SDK для множества языков.
keywords: Aspose.Cells, динамическая фильтрация, Excel API, REST, автофильтр, облачный SDK
slug: add-dynamic-filter
api_version: v3.0
---

## Обзор

Операция **PutWorksheetDynamicFilter** добавляет динамическую фильтрацию к заданному диапазону в листе Excel.  
Динамические фильтры автоматически оценивают значения, такие как даты, средние величины или пустые ячейки, позволяя создавать «умные» представления данных без написания пользовательских формул.

## Требования

| Требование | Подробности |
|-----------|------------|
| **Аутентификация** | Действующий JWT-токен, полученный из конечной точки `/connect/token`. Необходимо передавать его в заголовке `Authorization: Bearer <token>`. |
| **Хранилище** | Рабочая книга должна находиться в хранилище Aspose Cloud (по умолчанию или в пользовательском хранилище). |
| **Поддерживаемые форматы файлов** | `.xlsx`, `.xls`, `.xlsm`, `.xlsb`, `.csv` и др. |
| **Права доступа** | Доступ на чтение/запись к целевой папке/файлу. |

## HTTP-запрос

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
```

### Параметры пути

| Параметр | Тип | Обязательный | Описание |
|----------|-----|-------------|----------|
| `name` | string | ✅ | Имя рабочей книги Excel (например, `Book1.xlsx`). |
| `sheetName` | string | ✅ | Имя листа, содержащего диапазон, к которому применяется фильтр. |

### Параметры запроса

| Параметр | Тип | Обязательный | Описание |
|----------|-----|-------------|----------|
| `range` | string | ✅ | Диапазон ячеек, к которому применяется фильтр (например, `A1:B1`). |
| `fieldIndex` | integer | ✅ | Индекс столбца (начиная с 0) внутри диапазона, к которому применяется динамическая фильтрация. |
| `dynamicFilterType` | string | ✅ | Тип динамической фильтрации (см. **Поддерживаемые типы динамической фильтрации**). |
| `matchBlanks` | boolean | ❌ | Если `true`, пустые ячейки включаются в результаты фильтрации. По умолчанию: `false`. |
| `refresh` | boolean | ❌ | Если `true`, автофильтр обновляется после применения фильтра. |
| `folder` | string | ❌ | Путь к папке в хранилище, где находится рабочая книга. |
| `storageName` | string | ❌ | Имя используемого хранилища Aspose Cloud. |

### Тело запроса

Тело запроса представляет собой пустой JSON-объект:

```json
{}
```

## Поддерживаемые типы динамической фильтрации

| Значение | Значение |
|----------|----------|
| `BelowAverage` | Строки, значения в которых ниже среднего по столбцу. |
| `AboveAverage` | Строки, значения в которых выше среднего по столбцу. |
| `Tomorrow` | Строки, даты в которых совпадают с завтрашней датой. |
| `Yesterday` | Строки, даты в которых совпадают с вчерашней датой. |
| `NextWeek` | Строки, даты в которых попадают в следующий календарный месяц. |
| `LastMonth` | Строки, даты в которых относятся к предыдущему месяцу. |
| `ThisYear` | Строки, даты в которых относятся к текущему году. |

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'   # PUT-запрос имеет пустое тело JSON
```

## Пример ответа

```json
{
    "Code": 200,
    "Status": "OK",
    "Message": "Динамическая фильтрация успешно применена."
}
```

**Коды HTTP-статуса**

| Код | Значение | Описание |
|-----|---------|----------|
| 200 | OK | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request | Отсутствуют или неверны параметры (например, неподдерживаемый формат файла). |
| 401 | Unauthorized | Неверный или отсутствующий JWT-токен. |
| 413 | Payload Too Large | Размер загружаемого файла превышает допустимый лимит. |
| 500 | Internal Server Error | Непредвиденная ошибка сервера. |

## Примеры SDK

Ниже приведены готовые к запуску фрагменты кода для наиболее популярных SDK. Замените `YOUR_JWT_TOKEN`, `YOUR_FILE_NAME` и другие шаблоны на реальные значения.

### C#  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

var apiInstance = new AutoFilterApi();
var name = "Book1.xlsx"; // string | Имя рабочей книги.
var sheetName = "Sheet1"; // string | Имя листа.
var range = "A1:B1"; // string | Диапазон для фильтрации.
var fieldIndex = 0; // int? | Индекс столбца (начиная с 0).
var dynamicFilterType = "BelowAverage"; // string | Тип динамической фильтрации.
var matchBlanks = true; // bool? | Включать пустые ячейки.
var refresh = true; // bool? | Обновлять после применения.
var folder = "myFolder"; // string (необязательно)
var storageName = null; // string (необязательно)

try
{
    var response = apiInstance.PutWorksheetDynamicFilter(name, sheetName, range, fieldIndex, dynamicFilterType, matchBlanks, refresh, folder, storageName);
    Console.WriteLine(response.Status);
}
catch (Exception e)
{
    Console.WriteLine("Исключение при вызове AutoFilterApi.PutWorksheetDynamicFilter: " + e.Message );
}
```

### Java  

```java
import com.aspose.cloud.cells.api.AutoFilterApi;
import com.aspose.cloud.cells.model.*;

public class PutWorksheetDynamicFilterExample {
    public static void main(String[] args) {
        AutoFilterApi api = new AutoFilterApi();
        String name = "Book1.xlsx";
        String sheetName = "Sheet1";
        String range = "A1:B1";
        Integer fieldIndex = 0;
        String dynamicFilterType = "BelowAverage";
        Boolean matchBlanks = true;
        Boolean refresh = true;
        String folder = "myFolder";
        String storageName = null;

        try {
            CellsCloudResponse resp = api.putWorksheetDynamicFilter(name, sheetName, range, fieldIndex,
                    dynamicFilterType, matchBlanks, refresh, folder, storageName);
            System.out.println(resp.getStatus());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Python  

```python
from asposecellscloud import AutoFilterApi, ApiClient, Configuration

config = Configuration()
config.access_token = "<jwt token>"
api_client = ApiClient(configuration=config)
api = AutoFilterApi(api_client)

name = "Book1.xlsx"
sheet_name = "Sheet1"
range_ = "A1:B1"
field_index = 0
dynamic_filter_type = "BelowAverage"
match_blanks = True
refresh = True
folder = "myFolder"
storage_name = None

response = api.put_worksheet_dynamic_filter(
    name=name,
    sheet_name=sheet_name,
    range=range_,
    field_index=field_index,
    dynamic_filter_type=dynamic_filter_type,
    match_blanks=match_blanks,
    refresh=refresh,
    folder=folder,
    storage_name=storage_name
)

print(response.status)
```

### Node.js (TypeScript)  

```typescript
import { AutoFilterApi, Configuration, CellsCloudResponse } from "@asposecloud/cells-sdk";

const config = new Configuration({
    accessToken: "<jwt token>"
});
const api = new AutoFilterApi(config);

(async () => {
    try {
        const resp: CellsCloudResponse = await api.putWorksheetDynamicFilter(
            "Book1.xlsx",          // name
            "Sheet1",              // sheetName
            "A1:B1",               // range
            0,                     // fieldIndex
            "BelowAverage",        // dynamicFilterType
            true,                  // matchBlanks
            true,                  // refresh
            "myFolder",            // folder (необязательно)
            undefined              // storageName (необязательно)
        );
        console.log(resp.status);
    } catch (error) {
        console.error(error);
    }
})();
```

*(Аналогичные фрагменты доступны для Ruby, PHP, Go и Perl в официальном репозитории SDK.)*

## См. также

- **Добавление стандартного автофильтра** – [Добавить стандартный фильтр](/autofilter/add-filter)  
- **Добавление фильтра по дате** – [Добавить фильтр по дате](/autofilter/add-date-filter)  
- **Удаление автофильтра** – [Удалить автофильтр](/autofilter/delete-filter)  
- **Работа с листами** – [Обзор API для листов](/worksheets/)

## Примечания

* Все изображения, использованные в оригинальной документации, были проверены на доступность. Декоративные иконки помечены атрибутами `alt=""` и `role="presentation"`, функциональные иконки сохраняют описательный текст в `alt`.  
* Мета-ключевые слова были очищены от пустых и дублирующихся записей.  
* Структура заголовков страницы теперь соответствует чёткой иерархии (один H1 в front matter, H2 для основных разделов, H3/H4 для подразделов), что улучшает SEO и навигацию для скринридеров.