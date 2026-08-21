---
title: "Получить вторую ось категорий диаграммы"
type: docs
url: /ru/charts/second-category-axis/get/
weight: 60
keywords: "Получить вторую ось категорий диаграммы, Aspose.Cells Cloud API, ось диаграммы Excel, REST API, вторая ось категорий, Aspose.Cells"
description: "Получить вторую ось категорий диаграммы в рабочем листе Excel с использованием REST API Aspose.Cells Cloud. Включает формат запроса, параметры, пример cURL, схему ответа, коды состояния и примечания по использованию."
ArticleTitle: "Получить вторую ось категорий диаграммы – Aspose.Cells Cloud API"
---

Этот REST API позволяет получить **вторую ось категорий** диаграммы.

## API GetChartSecondCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud безопасны и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение параметра (path/query) | Описание                                                |
| ------------- | ------ | ----------------------------------- | ------------------------------------------------------- |
| name          | string | path                                | Имя файла Excel, хранящегося в облаке.                  |
| sheetName     | string | path                                | Имя рабочего листа, содержащего диаграмму.             |
| chartIndex    | integer| path                                | Индекс диаграммы (начиная с 0), для которой запрашивается ось. |
| folder        | string | query                               | Путь к папке в хранилище, где расположен файл.          |
| storageName   | string | query                               | Имя хранилища Aspose Cloud для использования (необязательно). |

### **Ответ**

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Second Category Axis",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий токен JWT.           |
| 413 | Payload Too Large           | Загруженный файл превышает допустимый размер.           |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                          |

## Как использовать API GetChartSecondCategoryAxis с SDK

### Спецификация API GetChartSecondCategoryAxis

Операция **GetChartSecondCategoryAxis** описана в [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) и позволяет выполнять прямые REST-взаимодействия из веб-браузера или любого HTTP-клиента.

Вы можете использовать утилиту командной строки `cURL` для удобного доступа к веб-сервисам Aspose.Cells. Ниже приведён пример вызова API с помощью `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Second Category Axis",
    "IsVisible": true,
    "AxisLine": { "Style": "Solid", "Weight": 1 },
    "TickMarks": "Inside",
    "Label": {
      "Font": { "Size": 10, "Color": "#000000" },
      "Format": "General"
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ интеграции этого API в ваш проект. SDK обрабатывают низкоуровневые детали, такие как аутентификация, построение запросов и разбор ответов, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов операции **Get Chart Second Category Axis** с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Настройка клиента API
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// Построение запроса
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// Выполнение
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Axis Name: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // Настройка клиента API
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // Построение запроса
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // Выполнение
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Axis Name: " + response.getAxis().getName());
    }
}
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
use Aspose\Cells\Cloud\Sdk\Api\ChartsApi;
use Aspose\Cells\Cloud\Sdk\Configuration;
use Aspose\Cells\Cloud\Sdk\Model\Requests\GetChartSecondCategoryAxisRequest;

// Настройка
$config = new Configuration();
$config->setClientId('<your-client-id>');
$config->setClientSecret('<your-client-secret>');

$apiInstance = new ChartsApi($config);

$request = new GetChartSecondCategoryAxisRequest(
    'Sample.xlsx',       // name
    'Sheet1',            // sheetName
    0,                   // chartIndex
    'Documents',         // folder
    null                 // storageName
);

try {
    $result = $apiInstance->getChartSecondCategoryAxis($request);
    echo "Axis Name: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Exception when calling ChartsApi->getChartSecondCategoryAxis: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# Настройка SDK
config = AsposeCellsCloud::Configuration.new
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = AsposeCellsCloud::ChartsApi.new

begin
  result = api_instance.get_chart_second_category_axis(
    name: 'Sample.xlsx',
    sheet_name: 'Sheet1',
    chart_index: 0,
    folder: 'Documents'
  )
  puts "Axis Name: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Exception when calling ChartsApi->get_chart_second_category_axis: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# Настройка клиента API
config = asposecellscloud.Configuration()
config.client_id = '<your-client-id>'
config.client_secret = '<your-client-secret>'

api_instance = ChartsApi(asposecellscloud.ApiClient(config))

request = GetChartSecondCategoryAxisRequest(
    name='Sample.xlsx',
    sheet_name='Sheet1',
    chart_index=0,
    folder='Documents'
)

try:
    response = api_instance.get_chart_second_category_axis(request)
    print('Axis Name:', response.axis.name)
except ApiException as e:
    print('Exception when calling ChartsApi->get_chart_second_category_axis:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Пример для Node.js с использованием SDK Aspose.Cells Cloud
const { ChartsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    clientId: '<your-client-id>',
    clientSecret: '<your-client-secret>'
});
const api = new ChartsApi(config);

(async () => {
    try {
        const response = await api.getChartSecondCategoryAxis({
            name: 'Sample.xlsx',
            sheetName: 'Sheet1',
            chartIndex: 0,
            folder: 'Documents'
        });
        console.log('Axis Name:', response.axis.name);
    } catch (error) {
        console.error('Error:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Пример для Android (Java) с использованием SDK Aspose.Cells Cloud для Android
import com.aspose.cells.cloud.sdk.api.ChartsApi;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.model.requests.*;

public class GetSecondCategoryAxisAndroid {
    public void execute() {
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        try {
            AxisResponse response = api.getChartSecondCategoryAxis(request);
            System.out.println("Axis Name: " + response.getAxis().getName());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
import AsposeCellsCloud

let config = Configuration(clientId: "<your-client-id>", clientSecret: "<your-client-secret>")
let api = ChartsApi(configuration: config)

let request = GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: nil
)

api.getChartSecondCategoryAxis(request: request) { result, error in
    if let axis = result?.axis {
        print("Axis Name: \(axis.name ?? "")")
    } else if let err = error {
        print("Error: \(err)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
use Aspose::Cells::Cloud::Sdk::Api::ChartsApi;
use Aspose::Cells::Cloud::Sdk::Configuration;

my $config = Aspose::Cells::Cloud::Sdk::Configuration->new(
    client_id     => '<your-client-id>',
    client_secret => '<your-client-secret>'
);
my $api = Aspose::Cells::Cloud::Sdk::Api::ChartsApi->new($config);

my $response = $api->get_chart_second_category_axis(
    name        => 'Sample.xlsx',
    sheet_name  => 'Sheet1',
    chart_index => 0,
    folder      => 'Documents'
);
print "Axis Name: " . $response->axis->name . "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
package main

import (
    "fmt"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"
    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3/api"
)

func main() {
    cfg := asposecellscloud.NewConfiguration()
    cfg.ClientId = "<your-client-id>"
    cfg.ClientSecret = "<your-client-secret>"

    apiInstance := api.NewChartsApi(cfg)

    request := asposecellscloud.GetChartSecondCategoryAxisRequest{
        Name:      "Sample.xlsx",
        SheetName: "Sheet1",
        ChartIndex: 0,
        Folder:    "Documents",
        StorageName: nil,
    }

    result, _, err := apiInstance.GetChartSecondCategoryAxis(request)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    fmt.Println("Axis Name:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}