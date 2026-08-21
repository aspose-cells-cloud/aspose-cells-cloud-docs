---
title: Отгруппировать столбцы в Excel — Aspose.Cells Cloud API  
description: Удалить группировку столбцов в листе Excel с помощью Aspose.Cells Cloud REST API (v3.0). Включает endpoint, параметры, метод аутентификации, пример cURL, формат ответа и фрагменты кода SDK.  
keywords: Aspose.Cells, отгруппировать, столбцы, Excel, API, REST, облако, SDK  
slug: columns/ungroup  
date: 2026-07-30  
---  

# Отгруппировать столбцы в Excel  

Aspose.Cells Cloud предоставляет операцию **POST**, которая удаляет группировку столбцов из указанного листа. На этой странице описаны формат запроса, требуемые параметры, метод аутентификации, примеры вызовов и использование SDK.

---  

## Необходимые условия  

| Требование | Зачем оно нужно |
|------------|-----------------|
| **Учётная запись Aspose Cloud** | Доступ к сервисам Aspose.Cells Cloud. |
| **JWT-токен доступа** | Все вызовы API должны быть авторизованы с помощью токена типа bearer. Подробности см. в [руководстве по аутентификации JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). |
| **Тетрадь, хранящаяся в облачном хранилище Aspose** | API работает с файлами, расположенными в облачном хранилище (или в подключённом внешнем хранилище). |
| **Имя листа** | Целевой лист должен существовать в тетради. |

---  

## Аутентификация  

Все запросы требуют заголовок **Authorization**, содержащий действительный JWT-токен:

```http
Authorization: Bearer <access_token>
```

Токен получается в рамках OAuth-потока Aspose Cloud. Срок действия токенов ограничен; при необходимости их нужно обновлять.

---  

## Endpoint  

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
```

* `{name}` — **Path** — имя файла тетради (например, `test.xlsx`).  
* `{sheetName}` — **Path** — имя листа (например, `Sheet1`).  

---  

## Параметры  

### Параметры пути  

| Имя | Тип | Обязательный | Описание |
|-----|-----|-------------|----------|
| `name` | string | Да | Имя файла тетради. |
| `sheetName` | string | Да | Имя листа. |

### Параметры запроса  

| Имя | Тип | Обязательный | Описание |
|-----|-----|-------------|----------|
| `firstIndex` | integer | Да | Нулевой индекс первого столбца, подлежащего отгруппировке. |
| `lastIndex` | integer | Да | Нулевой индекс последнего столбца, подлежащего отгруппировке. |
| `folder` | string | Нет | Путь к папке, содержащей тетрадь. |
| `storageName` | string | Нет | Имя сервиса хранилища, где расположен файл. |

---  

## Пример запроса (cURL)  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/ungroup?firstIndex=1&lastIndex=5" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

*Замените `<access_token>` на действительный JWT-токен.*

---  

## Успешный ответ  

```json
{
  "Code": 200,
  "Status": "OK",
  "Columns": {
    "FirstIndex": 1,
    "LastIndex": 5
  }
}
```

Объект ответа (`CellsCloudResponse`) содержит диапазон столбцов, которые были успешно отгруппированы.

### Ответ об ошибке  

В случае сбоя запроса сервис возвращает JSON- payload со следующими полями:

| Поле | Значение |
|------|----------|
| `Code` | Код ошибки в стиле HTTP (например, 400, 401). |
| `Status` | Краткое описание ошибки. |
| `ErrorMessage` | Подробное описание ошибки. |

---  

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                      |
|-----|-----------------------------|-----------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large           | Загружаемый файл превышает лимит размера. |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера. |
---  

## Примеры кода SDK  

Ниже приведены готовые к запуску фрагменты кода для самых популярных SDK. Замените значения-заглушки (`<YourAccessToken>`, `<YourFileName>` и т.д.) на свои данные.

<details><summary>**C# (.NET)**</summary>  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "<YourAccessToken>",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        var response = cellsApi.PostUngroupWorksheetColumns(
            name: "test.xlsx",
            sheetName: "Sheet1",
            firstIndex: 1,
            lastIndex: 5,
            folder: null,
            storageName: null);

        Console.WriteLine($"Ungrouped columns: {response.Columns.FirstIndex} – {response.Columns.LastIndex}");
    }
}
```
</details>

<details><summary>**Java**</summary>  

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.CellsCloudResponse;
import com.aspose.cells.cloud.Configuration;

public class UngroupColumns {
    public static void main(String[] args) throws Exception {
        Configuration config = new Configuration();
        config.setAccessToken("<YourAccessToken>");
        config.setBaseUrl("https://api.aspose.cloud");
        CellsApi api = new CellsApi(config);

        CellsCloudResponse resp = api.postUngroupWorksheetColumns(
            "test.xlsx",
            "Sheet1",
            1,
            5,
            null,
            null);

        System.out.println("Ungrouped columns: " + resp.getColumns().getFirstIndex()
                           + " – " + resp.getColumns().getLastIndex());
    }
}
```
</details>

<details><summary>**Python**</summary>  

```python
from asposecellscloud import CellsApi, Configuration

config = Configuration()
config.access_token = "<YourAccessToken>"
config.base_url = "https://api.aspose.cloud"

api = CellsApi(config)

response = api.post_ungroup_worksheet_columns(
    name="test.xlsx",
    sheet_name="Sheet1",
    first_index=1,
    last_index=5,
    folder=None,
    storage_name=None)

print(f"Ungrouped columns: {response.columns.first_index} – {response.columns.last_index}")
```
</details>

<details><summary>**Node.js**</summary>  

```javascript
const { CellsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    accessToken: "<YourAccessToken>",
    baseUrl: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postUngroupWorksheetColumns("test.xlsx", "Sheet1", 1, 5, null, null)
   .then(resp => {
       console.log(`Ungrouped columns: ${resp.columns.firstIndex} – ${resp.columns.lastIndex}`);
   })
   .catch(err => console.error(err));
```
</details>

<details><summary>**Go**</summary>  

```go
package main

import (
    "fmt"
    "github.com/asposecellscloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AccessToken = "<YourAccessToken>"
    config.BasePath = "https://api.aspose.cloud"

    api := sdk.NewCellsApi(config)

    resp, _, err := api.PostUngroupWorksheetColumns(
        "test.xlsx",
        "Sheet1",
        1,
        5,
        nil,
        nil,
    )
    if err != nil {
        panic(err)
    }
    fmt.Printf("Ungrouped columns: %d – %d\n", resp.Columns.FirstIndex, resp.Columns.LastIndex)
}
```
</details>

> **Примечание:** SDK для PHP, Ruby, Perl и других языков следуют тому же порядку параметров. Полные примеры см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

---  

## Ссылки  

* **Спецификация OpenAPI:** <https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns>  
* **Руководство по аутентификации:** <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>  
* **Репозиторий SDK:** <https://github.com/aspose-cells-cloud>

---  

## История изменений  

| Дата | Автор | Изменения |
|------|--------|-----------|
| 2026‑07‑30 | AI Optimizer | Исправлена кодировка UTF‑8, добавлен раздел «Необходимые условия», очищены мета-ключевые слова, улучшена иерархия заголовков, добавлены фрагменты кода SDK. |
| 2026‑07‑29 | Original | Первоначальный черновик документации. |

---