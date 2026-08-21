---
title: Добавление CellArea в условное форматирование
description: Добавьте диапазон ячеек к правилу условного форматирования в листе Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает эндпоинт, параметры, примеры cURL и SDK, схему ответа и обработку ошибок.
keywords: Aspose.Cells, условное форматирование, CellArea, REST API, Excel, облачный SDK
weight: 30
aliases:
  - /add-a-cell-area-for-format-condition/
---

# Добавление CellArea в условное форматирование

**Краткое описание** – Добавляет диапазон ячеек к существующему правилу условного форматирования в листе.

---

## Предварительные требования

1. **Аккаунт Aspose.Cells Cloud** – получите свои **App SID** и **App Key**.  
2. **JWT-токен** – сгенерируйте JWT-токен с использованием App SID/Key (см. [Руководство по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)).  
3. Целевой файл Excel уже должен существовать в указанном хранилище/папке.

---

## Аутентификация

Все вызовы требуют **аутентификации на основе JWT-токена**. Передайте токен в заголовке `Authorization`:

```http
Authorization: Bearer <jwt token>
```

---

## HTTP-запрос

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```

### Параметры пути

| Имя         | Тип    | Описание                                      |
|-------------|--------|-----------------------------------------------|
| `name`      | string | Имя файла Excel (например, `Book1.xlsx`).    |
| `sheetName` | string | Имя листа, содержащего правило (например, `Sheet1`). |
| `index`     | integer| Индекс правила условного форматирования (начиная с 0). |

### Параметры запроса

| Имя           | Тип    | Обязательный | Описание                                    |
|---------------|--------|-------------|---------------------------------------------|
| `cellArea`    | string | **Да**       | Диапазон ячеек для добавления в нотации A1 (например, `A1:C3`). |
| `folder`      | string | Нет          | Путь к папке, где хранится файл.            |
| `storageName` | string | Нет          | Имя сервиса хранилища.                      |

---

## Пример запроса (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Ожидаемый успешный ответ

```json
{
  "Code": "200",
  "Status": "OK",
  "CellArea": {
    "StartRow": 0,
    "StartColumn": 0,
    "EndRow": 2,
    "EndColumn": 2
  }
}
```

**Схема ответа – `CellArea`**

| Свойство       | Тип | Описание                                   |
|----------------|-----|--------------------------------------------|
| `StartRow`     | int | Индекс первой строки (начиная с 0).        |
| `StartColumn`  | int | Индекс первого столбца (начиная с 0).      |
| `EndRow`       | int | Индекс последней строки (начиная с 0).     |
| `EndColumn`    | int | Индекс последнего столбца (начиная с 0).   |

---

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен.         |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера.              |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                         |
---

## Примеры SDK

Ниже приведены короткие фрагменты кода для наиболее распространённых SDK. Замените `YOUR_APP_SID` и `YOUR_APP_KEY` на свои учётные данные и установите сгенерированный JWT-токен при необходимости.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.Sdk;
using Aspose.Cells.Cloud.Sdk.Model;

var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY"
};

var api = new ConditionalFormattingsApi(config);
var result = api.PutWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: null,
    storageName: null);

Console.WriteLine(result);
```

### Java

```java
import com.aspose.cells.cloud.ApiClient;
import com.aspose.cells.cloud.Configuration;
import com.aspose.cells.cloud.api.ConditionalFormattingsApi;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cells.cloud.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### PHP

```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Sdk\Api\ConditionalFormattingsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;

$config = new Configuration();
$config->setAppSid('YOUR_APP_SID');
$config->setAppKey('YOUR_APP_KEY');

$api = new ConditionalFormattingsApi($config);

try {
    $result = $api->putWorksheetFormatConditionArea(
        'Book1.xlsx',
        'Sheet1',
        0,
        'A1:C3',
        null,
        null
    );
    print_r($result);
} catch (Exception $e) {
    echo 'Error: ', $e->getMessage();
}
?>
```

### Ruby

```ruby
require 'aspose_cells_cloud_sdk'

config = AsposeCellsCloud::Configuration.new
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = AsposeCellsCloud::ConditionalFormattingsApi.new
begin
  result = api_instance.put_worksheet_format_condition_area(
    'Book1.xlsx', 'Sheet1', 0, 'A1:C3')
  puts result
rescue StandardError => e
  puts "Error: #{e}"
end
```

### Node.js

```javascript
const { Configuration, ConditionalFormattingsApi } = require('asposecellscloudsdk');

const config = new Configuration();
config.appSid = 'YOUR_APP_SID';
config.appKey = 'YOUR_APP_KEY';

const api = new ConditionalFormattingsApi(config);

api.putWorksheetFormatConditionArea('Book1.xlsx', 'Sheet1', 0, 'A1:C3')
   .then(res => console.log(res))
   .catch(err => console.error('Error:', err));
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk.rest import ApiException
from asposecellscloudsdk import Configuration, ApiClient
from asposecellscloudsdk.api import conditional_formattings_api

config = Configuration()
config.app_sid = 'YOUR_APP_SID'
config.app_key = 'YOUR_APP_KEY'

api_instance = conditional_formattings_api.ConditionalFormattingsApi(ApiClient(config))

try:
    result = api_instance.put_worksheet_format_condition_area(
        name='Book1.xlsx',
        sheet_name='Sheet1',
        index=0,
        cell_area='A1:C3')
    print(result)
except ApiException as e:
    print("Exception:", e)
```

### Android (Java)

```java
import com.aspose.cloud.cells.api.ConditionalFormattingsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.client.Configuration;

Configuration config = new Configuration();
config.setAppSid("YOUR_APP_SID");
config.setAppKey("YOUR_APP_KEY");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(new ApiClient(config));

try {
    com.aspose.cloud.cells.model.ResponseMessage resp = api.putWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", null, null);
    System.out.println(resp);
} catch (Exception e) {
    e.printStackTrace();
}
```

### Swift

```swift
import AsposeCellsCloud

let config = Configuration(appSid: "YOUR_APP_SID", appKey: "YOUR_APP_KEY")
let api = ConditionalFormattingsApi(configuration: config)

api.putWorksheetFormatConditionArea(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    cellArea: "A1:C3",
    folder: nil,
    storageName: nil) { result, error in
        if let err = error {
            print("Error:", err)
        } else if let res = result {
            print(res)
        }
}
```

### Perl

```perl
use AsposeCellsCloud::Api::ConditionalFormattingsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    app_sid  => 'YOUR_APP_SID',
    app_key  => 'YOUR_APP_KEY'
);
my $api = AsposeCellsCloud::Api::ConditionalFormattingsApi->new($config);

my $result = $api->putWorksheetFormatConditionArea(
    name      => 'Book1.xlsx',
    sheetName => 'Sheet1',
    index     => 0,
    cellArea  => 'A1:C3'
);
print $result;
```

### Go

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/sdk"
)

func main() {
    config := sdk.NewConfiguration()
    config.AppSid = "YOUR_APP_SID"
    config.AppKey = "YOUR_APP_KEY"

    api := sdk.NewConditionalFormattingsApi(config)

    resp, _, err := api.PutWorksheetFormatConditionArea(
        "Book1.xlsx", "Sheet1", 0, "A1:C3", nil, nil)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println(resp)
}
```

---

## Примечания и советы

- **Формат CellArea** – Должен быть допустимым диапазоном A1 (`A1`, `A1:C3`, `Sheet2!B2:D5`). Недопустимые форматы возвращают **400 Bad Request**.
- **Перекрывающиеся диапазоны** – Добавление диапазона, перекрывающего существующий диапазон того же правила, вызывает **409 Conflict**.
- **Индексация с нуля** – Индексы строк и столбцов в ответе начинаются с `0`. При необходимости преобразуйте их в 1-индексную нотацию Excel.
- **Хранилище** – Если параметры `folder` и `storageName` опущены, API использует хранилище по умолчанию/корневую папку.

---

## Связанные операции

- **Удаление диапазона ячеек** – `DELETE /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area`
- **Добавление условия к условному форматированию** – `POST /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`
- **Получение условного форматирования** – `GET /cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}`

Эти операции можно комбинировать для построения полных рабочих процессов условного форматирования.

---