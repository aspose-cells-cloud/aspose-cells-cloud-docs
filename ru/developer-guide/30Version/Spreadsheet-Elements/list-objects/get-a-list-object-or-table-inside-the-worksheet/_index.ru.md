---
title: "Aspose.Cells Cloud API – Получение объекта списка (таблицы) из рабочего листа"
description: "Получение объекта ListObject (таблицы) из рабочего листа Excel с помощью REST API Aspose.Cells Cloud. Поддержка экспорта в несколько форматов (PDF, CSV, JSON, …)."
keywords:
  - Aspose.Cells
  - Cloud API
  - Excel
  - ListObject
  - Таблица
  - REST
  - SDK
type: docs
slug: /list-objects/get/
weight: 9
---

# Aspose.Cells Cloud API – Получение объекта списка (таблицы) из рабочего листа

Получите **объект списка** (также называемый *таблицей*) из конкретного рабочего листа в книге Excel. Эта конечная точка также позволяет напрямую экспортировать таблицу в выбранный формат с помощью необязательного параметра запроса `format`.

---

## Необходимые условия

| Требование | Подробности |
|-----------|------------|
| **Аутентификация** | Требуется действительный токен **JWT** (Bearer). Получите токен, следуя инструкциям из руководства по **OAuth2** аутентификации, описанному в разделе [Руководство по аутентификации](/authentication/). |
| **Хранилище** | Книга должна храниться в расположении облачного хранилища Aspose. Если файл находится в нестандартном хранилище, укажите параметр запроса `storageName`. |
| **Ограничения частоты запросов** | API следует стандартной политике ограничения частоты запросов Aspose Cloud (по умолчанию — 100 запросов в минуту на аккаунт). |
| **SDK (опционально)** | Использование одного из официальных SDK (C#, Java, Python и др.) упрощает создание запросов и обработку ответов. См. раздел **Примеры SDK** ниже. |

---

## Запрос

### HTTP GET

```
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
```

| Параметр | Тип | Место | Обязательный | Описание |
|----------|-----|-------|-------------|----------|
| **name** | `string` | Путь | ✔️ | Имя файла Excel (включая расширение). |
| **sheetName** | `string` | Путь | ✔️ | Рабочий лист, содержащий объект списка. |
| **listobjectindex** | `integer` | Путь | ✔️ | Нулевой индекс объекта списка, который необходимо получить. |
| **format** | `string` | Запрос | ❌ | Желаемый формат экспорта (например, `pdf`, `csv`, `json`). |
| **folder** | `string` | Запрос | ❌ | Путь к папке, где хранится книга. |
| **storageName** | `string` | Запрос | ❌ | Имя хранилища Aspose Cloud, которое следует использовать. |

#### Примечания

* Все вызовы **должны** выполняться по протоколу HTTPS.  
* При указании параметра `format` тело ответа содержит поток экспортированного файла (например, `application/pdf`).  
* Без параметра `format` API возвращает описание ListObject в формате JSON.

---

## Пример cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1?format=csv" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

*Замените `<your_jwt_token>` действительным JWT, полученным из конечной точки аутентификации.*

---

## Успешный ответ (JSON)

Если параметр **`format` опущен**, API возвращает JSON-данные, описывающие ListObject.

```json
{
  "ListObject": {
    "AutoFilter": {
      "FilterColumns": [],
      "Range": "B2:F11",
      "Sorter": {
        "CaseSensitive": false,
        "HasHeaders": false,
        "KeyList": [],
        "SortLeftToRight": false
      }
    },
    "DisplayName": "Table3",
    "StartColumn": 1,
    "StartRow": 1,
    "EndColumn": 5,
    "EndRow": 10,
    "ListColumns": [
      {
        "Name": "Column1",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 1,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$B$2:$B$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column2",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 2,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$C$2:$C$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column3",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 3,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$D$2:$D$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column4",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 4,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$E$2:$E$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      },
      {
        "Name": "Column5",
        "Range": {
          "ColumnCount": 1,
          "ColumnWidth": 8.5,
          "FirstColumn": 5,
          "FirstRow": 1,
          "RefersTo": "=Sheet1!$F$2:$F$11",
          "RowCount": 10,
          "RowHeight": 13.5,
          "Worksheet": "Sheet1"
        },
        "TotalsCalculation": "None"
      }
    ],
    "ShowHeaderRow": true,
    "ShowTableStyleColumnStripes": false,
    "ShowTableStyleFirstColumn": false,
    "ShowTableStyleLastColumn": false,
    "ShowTableStyleRowStripes": true,
    "ShowTotals": false,
    "TableStyleName": "None",
    "TableStyleType": "None",
    "link": {
      "Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

Если параметр **`format` указан**, тело ответа содержит двоичный поток файла запрошенного типа (например, `Content-Type: text/csv`).

---

## Обработка ошибок

| HTTP-код | Значение | Пример JSON |
|----------|----------|-------------|
| **400** | Неверный запрос — отсутствуют или некорректны параметры. | `{"Code":400,"Message":"Invalid format parameter."}` |
| **401** | Ошибка авторизации — отсутствует или некорректен токен JWT. | `{"Code":401,"Message":"Authentication failed."}` |
| **404** | Не найдено — книга, рабочий лист или объект списка не существуют. | `{"Code":404,"Message":"ListObject not found."}` |
| **500** | Внутренняя ошибка сервера. | `{"Code":500,"Message":"Unexpected server error."}` |

### Распространённые ошибки (примечания)

* **Индексы начинаются с нуля** — `listobjectindex` начинается с **0**. Запрос индекса `1` вернёт вторую таблицу на листе.  
* **Папка и хранилище** — Если книга хранится в подпапке, укажите параметр запроса `folder` (например, `?folder=Reports/2024`).  
* **Формат экспорта** — Допускаются только форматы, поддерживаемые движком преобразования Aspose.Cells (`pdf`, `xlsx`, `csv`, `json`, …). Указание недопустимого значения вызовет ошибку **400**.

---

## Примеры SDK

Ниже приведены фрагменты кода, демонстрирующие вызов конечной точки с использованием официальных SDK Aspose.Cells Cloud. Замените заглушки (`<YOUR_CLIENT>`, `<YOUR_JWT>` и т.д.) на ваши фактические данные конфигурации.

<details>
<summary>💻 C#</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Инициализация клиента API
var apiInstance = new ListObjectsApi();

// Формирование запроса
var request = new GetWorksheetListObjectRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: null,               // например, "csv" для экспорта
    folder: null,
    storageName: null
);

// Выполнение
var response = apiInstance.GetWorksheetListObject(request);
Console.WriteLine(response);
```
</details>

<details>
<summary>☕ Java</summary>

```java
import com.aspose.cells.cloud.api.ListObjectsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetWorksheetListObjectExample {
    public static void main(String[] args) throws ApiException {
        ListObjectsApi apiInstance = new ListObjectsApi();

        GetWorksheetListObjectRequest request = new GetWorksheetListObjectRequest(
                "Book1.xlsx",   // name
                "Sheet1",       // sheetName
                1,              // listobjectindex
                null,           // format
                null,           // folder
                null            // storageName
        );

        ListObjectResponse result = apiInstance.getWorksheetListObject(request);
        System.out.println(result);
    }
}
```
</details>

<details>
<summary>🐍 Python</summary>

```python
from asposecellscloud.apis.list_objects_api import ListObjectsApi
from asposecellscloud.models import GetWorksheetListObjectRequest

api = ListObjectsApi()

request = GetWorksheetListObjectRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    listobjectindex=1,
    format=None,
    folder=None,
    storage_name=None
)

response = api.get_worksheet_list_object(request)
print(response)
```
</details>

<details>
<summary>🟢 Node.js (TypeScript)</summary>

```typescript
import { ListObjectsApi, GetWorksheetListObjectRequest } from "@asposecellscloud/asposecellscloud";

const api = new ListObjectsApi();

const request = new GetWorksheetListObjectRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    listobjectindex: 1,
    format: undefined,
    folder: undefined,
    storageName: undefined
});

api.getWorksheetListObject(request)
   .then(response => console.log(response))
   .catch(err => console.error(err));
```
</details>

<details>
<summary>🐘 PHP</summary>

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

use Aspose\Cells\Cloud\Api\ListObjectsApi;
use Aspose\Cells\Cloud\Model\Requests\GetWorksheetListObjectRequest;

$listObjectsApi = new ListObjectsApi();

$request = new GetWorksheetListObjectRequest(
    "Book1.xlsx",   // name
    "Sheet1",       // sheetName
    1,              // listobjectindex
    null,           // format
    null,           // folder
    null            // storageName
);

$response = $listObjectsApi->getWorksheetListObject($request);
print_r($response);
?>
```
</details>

<details>
<summary>💎 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

api_instance = AsposeCellsCloud::ListObjectsApi.new

request = AsposeCellsCloud::GetWorksheetListObjectRequest.new(
  name: 'Book1.xlsx',
  sheet_name: 'Sheet1',
  listobjectindex: 1,
  format: nil,
  folder: nil,
  storage_name: nil
)

result = api_instance.get_worksheet_list_object(request)
puts result
```
</details>

<details>
<summary>🦪 Go</summary>

```go
package main

import (
    "fmt"
    cells "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AddDefaultHeader("Authorization", "Bearer <your_jwt>")
    client := api.NewAPIClient(cfg)

    request := api.GetWorksheetListObjectRequest{
        Name:            "Book1.xlsx",
        SheetName:       "Sheet1",
        Listobjectindex: 1,
        Format:          nil,
        Folder:          nil,
        StorageName:     nil,
    }

    result, _, err := client.ListObjectsApi.GetWorksheetListObject(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Printf("%+v\n", result)
}
```
</details>

---

## См. также

| Связанная конечная точка | Описание |
|--------------------------|----------|
| **Добавление ListObject** | `POST /cells/{name}/worksheets/{sheetName}/listobjects` — создание новой таблицы. |
| **Обновление ListObject** | `PUT /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` — изменение свойств таблицы. |
| **Удаление ListObject** | `DELETE /cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}` — удаление таблицы. |
| **Получение всех ListObjects** | `GET /cells/{name}/worksheets/{sheetName}/listobjects` — перечисление таблиц на рабочем листе. |

---

## Ссылки

* **Спецификация OpenAPI** – <https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject>  
* **Руководство по аутентификации** – <https://docs.aspose.cloud/cells/authentication/>  
* **Репозиторий на GitHub (SDK)** – <https://github.com/aspose-cells-cloud>  

---
---