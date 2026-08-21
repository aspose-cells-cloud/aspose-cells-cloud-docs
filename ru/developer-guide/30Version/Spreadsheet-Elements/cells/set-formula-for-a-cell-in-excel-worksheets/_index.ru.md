---
title: "Установка формулы ячейки в рабочих листах Excel"
type: docs
url: /ru/set-formula-for-a-cell-in-excel-worksheets/
weight: 80
keywords: "Excel, Aspose.Cells, REST API, установка формулы, рабочий лист, ячейка, облачный SDK, cURL"
description: "Узнайте, как установить формулу для конкретной ячейки в рабочем листе Excel с использованием Aspose.Cells Cloud REST API. Включает пример cURL, полный список параметров, обработку ошибок и примеры кода SDK."
---

Этот REST API устанавливает **формулу ячейки** в файл Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```

## Безопасность и аутентификация

Aspose.Cells Cloud API защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**Параметры запроса**

| Имя параметра | Тип    | Местоположение | Обязательный | Описание                                 |
|---------------|--------|----------------|-------------|------------------------------------------|
| name          | string | path           | Да          | Имя документа Excel.                     |
| sheetName     | string | path           | Да          | Имя рабочего листа.                      |
| cellName      | string | path           | Да          | Адрес целевой ячейки (например, **A1**). |
| value         | string | query          | Нет         | Значение, присваиваемое ячейке.          |
| type          | string | query          | Нет         | Тип данных значения (например, **string**). |
| formula       | string | query          | Нет         | Формула, применяемая к ячейке (например, **sum(A1,A2)**). |
| folder        | string | query          | Нет         | Папка, содержащая документ.              |
| storageName   | string | query          | Нет         | Имя службы хранилища.                    |

## **Ответ**

Возвращает объект CellResponse.

- **Обзор полей ответа**

| Поле            | Тип     | Описание                                            |
| --------------- | ------- | --------------------------------------------------- |
| `Name`          | string  | Адрес ячейки (например, `F341`).                    |
| `Row`           | integer | Индекс строки (отсчёт от нуля).                      |
| `Column`        | integer | Индекс столбца (отсчёт от нуля).                    |
| `Value`         | string  | Отображаемое значение ячейки.                        |
| `Type`          | string  | Тип данных ячейки (например, `IsString`).            |
| `Formula`       | string  | Текст формулы, если ячейка содержит формулу.         |
| `IsFormula`     | bool    | Указывает, содержит ли ячейка формулу.               |
| `IsMerged`      | bool    | Указывает, входит ли ячейка в объединённый диапазон. |
| `IsArrayHeader` | bool    | Указывает, является ли ячейка заголовком массива.    |
| `IsInArray`     | bool    | Указывает, принадлежит ли ячейка массиву.            |
| `IsErrorValue`  | bool    | Указывает, содержит ли ячейка значение ошибки.       |
| `IsInTable`     | bool    | Указывает, находится ли ячейка внутри таблицы.       |
| `IsStyleSet`    | bool    | Указывает, применён ли к ячейке стиль.               |
| `HtmlString`    | string  | HTML-кодированное представление значения ячейки.     |
| `Style.link`    | object  | Гиперссылка на ресурс стиля.                          |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                     |
|-----|-----------------------------|--------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции.    |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Неверный или отсутствующий JWT-токен.                        |
| 413 | Payload Too Large           | Загружаемый файл превышает лимит размера.                    |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                               |

## Как использовать API PostWorksheetCellSetValue с SDK

### Спецификация API PostWorksheetCellSetValue

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) определяет общедоступное программное интерфейсное определение и позволяет выполнять взаимодействие REST напрямую из веб-браузера.

Используйте утилиту командной строки cURL для вызова веб-сервисов Aspose.Cells.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A1?value=1234&type=string&formula=sum(A2:A15)" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access‑token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Пример на C# — установка формулы для ячейки
// Замените <access-token>, <file-name> и т.д. своими значениями.
var api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
var response = api.PostWorksheetCellSetValue(
    name: "myWorkbook.xlsx",
    sheetName: "Sheet1",
    cellName: "A3",
    value: "1234",
    type: "string",
    formula: "SUM(A1,A2)",
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Пример на Java — установка формулы для ячейки
CellsApi api = new CellsApi("<client-id>", "<client-secret>", "https://api.aspose.cloud");
PostWorksheetCellSetValueRequest request = new PostWorksheetCellSetValueRequest()
        .name("myWorkbook.xlsx")
        .sheetName("Sheet1")
        .cellName("A3")
        .value("1234")
        .type("string")
        .formula("SUM(A1,A2)");
CellsResponse response = api.postWorksheetCellSetValue(request);
System.out.println(response.getStatus());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Пример на PHP — установка формулы для ячейки
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppKey('<client-id>');
$config->setAppSid('<client-secret>');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$result = $apiInstance->postWorksheetCellSetValue(
    "myWorkbook.xlsx",
    "Sheet1",
    "A3",
    "1234",
    "string",
    "SUM(A1,A2)"
);
echo $result->getStatus();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Пример на Ruby — установка формулы для ячейки
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.api_key['client_id'] = '<client-id>'
config.api_key['client_secret'] = '<client-secret>'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::CellsApi.new
result = api.post_worksheet_cell_set_value(
  name: 'myWorkbook.xlsx',
  sheet_name: 'Sheet1',
  cell_name: 'A3',
  value: '1234',
  type: 'string',
  formula: 'SUM(A1,A2)'
)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Пример на Python — установка формулы для ячейки
import asposecellscloud

client = asposecellscloud.CellsApiClient(
    client_id='<client-id>',
    client_secret='<client-secret>',
    base_url='https://api.aspose.cloud'
)

api = asposecellscloud.CellsApi(client)
response = api.post_worksheet_cell_set_value(
    name='myWorkbook.xlsx',
    sheet_name='Sheet1',
    cell_name='A3',
    value='1234',
    type='string',
    formula='SUM(A1,A2)'
)
print(response.status)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Пример на Node.js — установка формулы для ячейки
const { CellsApi, ApiClient } = require('asposecellscloud');
const client = new ApiClient();
client.config = {
    clientId: '<client-id>',
    clientSecret: '<client-secret>',
    baseUrl: 'https://api.aspose.cloud'
};

const cellsApi = new CellsApi(client);
cellsApi.postWorksheetCellSetValue({
    name: 'myWorkbook.xlsx',
    sheetName: 'Sheet1',
    cellName: 'A3',
    value: '1234',
    type: 'string',
    formula: 'SUM(A1,A2)'
}).then(res => console.log(res.status));
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Пример на Android (Java) — установка формулы для ячейки
// Аналогично стандартному примеру на Java; убедитесь, что используется SDK, совместимый с Android.
```

{{< /tab >}}

{{< tab tabNum="8" >}}

**Пример на Swift недоступен**. SDK для Swift в настоящее время находится в разработке.

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Пример на Perl — установка формулы для ячейки
use AsposeCellsCloud::CellsApi;
my $api_instance = AsposeCellsCloud::CellsApi->new(
    client_id => '<client-id>',
    client_secret => '<client-secret>',
    base_url => 'https://api.aspose.cloud'
);
my $result = $api_instance->post_worksheet_cell_set_value(
    name => 'myWorkbook.xlsx',
    sheet_name => 'Sheet1',
    cell_name => 'A3',
    value => '1234',
    type => 'string',
    formula => 'SUM(A1,A2)'
);
print $result->{Status};
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Пример на Go — установка формулы для ячейки
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration()
    config.ClientId = "<client-id>"
    config.ClientSecret = "<client-secret>"
    config.BasePath = "https://api.aspose.cloud"

    api := asposecellscloud.NewAPIClient(config).CellsApi
    resp, _, err := api.PostWorksheetCellSetValue(
        "myWorkbook.xlsx",
        "Sheet1",
        "A3",
        map[string]string{
            "value":   "1234",
            "type":    "string",
            "formula": "SUM(A1,A2)",
        },
        nil,
        nil,
    )
    if err != nil {
        fmt.Println(err)
        return
    }
    fmt.Println(resp.Status)
}
```

{{< /tab >}}

{{< /tabs >}}