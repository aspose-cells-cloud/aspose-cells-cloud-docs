---
title: "Aspose.Cells Cloud API – Обновление оси значений диаграммы (POST /valueaxis)"
description: "Обновите ось значений диаграммы в электронной таблице Excel с использованием REST API Aspose.Cells Cloud. Включает адрес endpoint, параметры, схему тела запроса, примеры (cURL и SDK), ответы и обработку ошибок."
keywords:
  - Aspose.Cells Cloud
  - Обновление оси значений диаграммы
  - REST API
  - Ось диаграммы Excel
  - POST valueaxis
  - Пример cURL
  - SDK
  - JSON-полезная нагрузка
  - Настройки оси диаграммы
last_updated: 2026-07-30
---

# Обновление оси значений диаграммы (POST /valueaxis)

**Краткое описание:**  
Измените ось значений конкретной диаграммы в электронной таблице Excel, хранящейся в Aspose Cloud. В одном запросе можно задать границы, интервалы делений, логарифмический масштаб и другие параметры оси.

---

## Предварительные требования

1. **JWT-токен доступа** – получите токен, следуя инструкциям в руководстве [Аутентификация](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
2. Целевой **файл рабочей книги** должен уже быть загружен в облачное хранилище Aspose Cloud (или в хранилище по умолчанию).  
3. Знайте имя **листовой страницы** и **индекс диаграммы (начиная с 0)**, которую вы хотите изменить.

---

## Адрес endpoint

```
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

*Замените заполнители на реальные значения.*

| Заполнитель | Описание |
|-------------|----------|
| `{name}` | Имя файла Excel (например, `Book1.xlsx`). |
| `{sheetName}` | Листовая страница, содержащая диаграмму (например, `Sheet1`). |
| `{chartIndex}` | Индекс диаграммы (начиная с 0) (например, `0`). |

---

## Аутентификация

API использует **аутентификацию по токену JWT**. Включите токен в заголовке `Authorization`:

```
Authorization: Bearer <jwt token>
```

---

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

## Параметры запроса

| Имя              | Расположение | Тип    | Обязательный | Описание |
|------------------|--------------|--------|-------------|----------|
| **name**         | Path         | string | Да          | Имя файла Excel, хранящегося в облаке. |
| **sheetName**    | Path         | string | Да          | Листовая страница, содержащая диаграмму. |
| **chartIndex**   | Path         | int    | Да          | Индекс диаграммы (начиная с 0), которую нужно обновить. |
| **axis**         | Body         | object | Да          | Настройки оси (см. *Схема тела запроса*). |
| **folder**       | Query        | string | Нет         | Путь к папке в облаке, где находится файл. |
| **storageName**  | Query        | string | Нет         | Имя используемого сервиса хранилища. |

---

## Схема тела запроса (объект `axis`)

Необходимо указывать только те свойства, которые требуется изменить.

| Свойство       | Тип     | Обязательное | Описание |
|----------------|---------|--------------|----------|
| `minimum`      | number  | Нет          | Нижняя граница оси. |
| `maximum`      | number  | Нет          | Верхняя граница оси. |
| `majorUnit`    | number  | Нет          | Интервал между основными метками. |
| `minorUnit`    | number  | Нет          | Интервал между вспомогательными метками. |
| `logBase`      | number  | Нет          | Основание логарифма, если `isLogarithmic` равно `true`. |
| `isLogarithmic`| boolean | Нет          | Использует ли ось логарифмический масштаб. |
| `displayUnit`  | string  | Нет          | Метка единицы отображения на оси (например, `"Thousands"`). |
| `tickMark`     | string  | Нет          | Стиль меток (`"inside"`, `"outside"` и т.д.). |
| `crossAt`      | number  | Нет          | Позиция, где ось пересекает перпендикулярную ось. |

### Пример тела запроса

```json
{
  "minimum": 0,
  "maximum": 200,
  "majorUnit": 20,
  "minorUnit": 5,
  "logBase": 10,
  "isLogarithmic": false,
  "displayUnit": "Units",
  "tickMark": "inside",
  "crossAt": 0
}
```

---

## Примеры запросов

### cURL

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/<code class=\"placeholder\">{name}</code>/worksheets/<code class=\"placeholder\">{sheetName}</code>/charts/<code class=\"placeholder\">{chartIndex}</code>/valueaxis?folder=<code class=\"placeholder\">{folder}</code>&storageName=<code class=\"placeholder\">{storageName}</code>" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "minimum": 0,
        "maximum": 200,
        "majorUnit": 20,
        "minorUnit": 5,
        "logBase": 10,
        "isLogarithmic": false,
        "displayUnit": "Units",
        "tickMark": "inside",
        "crossAt": 0
      }'
```

### Примеры SDK  

{{< tabs tabTotal="10" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var api = new ChartsApi("client_id", "client_secret");
var axis = new Axis()
{
    Minimum = 0,
    Maximum = 200,
    MajorUnit = 20,
    MinorUnit = 5,
    LogBase = 10,
    IsLogarithmic = false,
    DisplayUnit = "Units",
    TickMark = "inside",
    CrossAt = 0
};

var response = api.PostChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
Console.WriteLine($"Status: {response.Status}");
```
{{< /tab >}}

{{< tab tabNum="2" >}}
```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.Axis;

ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
System.out.println("Value axis updated.");
```
{{< /tab >}}

{{< tab tabNum="3" >}}
```php
<?php
require 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\ChartsApi;
use Aspose\Cells\Cloud\Model\Axis;

$api = new ChartsApi('client_id', 'client_secret');
$axis = new Axis([
    'minimum' => 0,
    'maximum' => 200,
    'majorUnit' => 20,
    'minorUnit' => 5,
    'logBase' => 10,
    'isLogarithmic' => false,
    'displayUnit' => 'Units',
    'tickMark' => 'inside',
    'crossAt' => 0
]);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
echo "Value axis updated.\n";
?>
```
{{< /tab >}}

{{< tab tabNum="4" >}}
```ruby
require 'aspose_cells_cloud'

api = AsposeCellsCloud::ChartsApi.new('client_id', 'client_secret')
axis = AsposeCellsCloud::Axis.new(
  minimum: 0,
  maximum: 200,
  majorUnit: 20,
  minorUnit: 5,
  logBase: 10,
  isLogarithmic: false,
  displayUnit: 'Units',
  tickMark: 'inside',
  crossAt: 0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
puts 'Value axis updated.'
```
{{< /tab >}}

{{< tab tabNum="5" >}}
```python
from asposecellscloud import ChartsApi, Axis

api = ChartsApi('client_id', 'client_secret')
axis = Axis(
    minimum=0,
    maximum=200,
    majorUnit=20,
    minorUnit=5,
    logBase=10,
    isLogarithmic=False,
    displayUnit='Units',
    tickMark='inside',
    crossAt=0
)

api.post_chart_value_axis('Book1.xlsx', 'Sheet1', 0, axis)
print('Value axis updated.')
```
{{< /tab >}}

{{< tab tabNum="6" >}}
```javascript
// Пример для Node.js
const { ChartsApi, Axis } = require('asposecellscloud');

const api = new ChartsApi('client_id', 'client_secret');
const axis = new Axis({
    minimum: 0,
    maximum: 200,
    majorUnit: 20,
    minorUnit: 5,
    logBase: 10,
    isLogarithmic: false,
    displayUnit: 'Units',
    tickMark: 'inside',
    crossAt: 0
});

api.postChartValueAxis('Book1.xlsx', 'Sheet1', 0, axis)
   .then(response => console.log('Value axis updated.'))
   .catch(err => console.error(err));
```
{{< /tab >}}

{{< tab tabNum="7" >}}
```java
// Пример для Android (Java)
ChartsApi api = new ChartsApi("client_id", "client_secret");
Axis axis = new Axis()
        .minimum(0.0)
        .maximum(200.0)
        .majorUnit(20.0)
        .minorUnit(5.0)
        .logBase(10.0)
        .isLogarithmic(false)
        .displayUnit("Units")
        .tickMark("inside")
        .crossAt(0.0);

api.postChartValueAxis("Book1.xlsx", "Sheet1", 0, axis);
```
{{< /tab >}}

{{< tab tabNum="8" >}}
```swift
import AsposeCellsCloud

let api = ChartsApi(clientId: "client_id", clientSecret: "client_secret")
var axis = Axis()
axis.minimum = 0
axis.maximum = 200
axis.majorUnit = 20
axis.minorUnit = 5
axis.logBase = 10
axis.isLogarithmic = false
axis.displayUnit = "Units"
axis.tickMark = "inside"
axis.crossAt = 0

api.postChartValueAxis(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, axis: axis) { result, error in
    if let error = error {
        print("Error: \\(error)")
    } else {
        print("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< tab tabNum="9" >}}
```perl
use Aspose::Cells::Cloud::Api::ChartsApi;
use Aspose::Cells::Cloud::Model::Axis;

my $api  = ChartsApi->new('client_id', 'client_secret');
my $axis = Axis->new(
    minimum        => 0,
    maximum        => 200,
    majorUnit      => 20,
    minorUnit      => 5,
    logBase        => 10,
    isLogarithmic  => JSON::false,
    displayUnit    => 'Units',
    tickMark       => 'inside',
    crossAt        => 0
);

$api->postChartValueAxis('Book1.xlsx', 'Sheet1', 0, $axis);
print "Value axis updated.\n";
```
{{< /tab >}}

{{< tab tabNum="10" >}}
```go
package main

import (
    "context"
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/api"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v2/model"
)

func main() {
    cfg := api.NewConfiguration()
    cfg.AddDefaultHeader("client_id", "client_id")
    cfg.AddDefaultHeader("client_secret", "client_secret")
    client := api.NewAPIClient(cfg)

    axis := model.Axis{
        Minimum:       0,
        Maximum:       200,
        MajorUnit:     20,
        MinorUnit:     5,
        LogBase:       10,
        IsLogarithmic: false,
        DisplayUnit:   "Units",
        TickMark:      "inside",
        CrossAt:       0,
    }

    _, err := client.ChartsApi.PostChartValueAxis(context.Background(), "Book1.xlsx", "Sheet1", 0, axis)
    if err != nil {
        fmt.Println("Error:", err)
    } else {
        fmt.Println("Value axis updated.")
    }
}
```
{{< /tab >}}

{{< /tabs >}}

---

## Ответы

### Успех (200)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Тип ответа: `CellsCloudResponse`.

**Коды HTTP-статуса**

| Код | Значение                    | Описание |
|-----|-----------------------------|----------|
| 200 | OK (ОК)                    | Фильтр успешно применен; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой payload) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

---

## Дополнительные ресурсы

- **Спецификация OpenAPI** – [Просмотр / загрузка JSON/YAML](https://apireference.aspose.cloud/cells/#/Charts/PostChartValueAxis)  
- **Репозиторий SDK** – <https://github.com/aspose-cells-cloud>  
- **Руководство по аутентификации** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>

---

*Для любых вопросов или обратной связи свяжитесь с командой поддержки Aspose.Cells Cloud.*