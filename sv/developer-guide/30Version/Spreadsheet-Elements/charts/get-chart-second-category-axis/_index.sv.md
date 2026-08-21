---
title: "Hämta diagrammets andra kategoriaxel"
type: docs
url: /sv/charts/second-category-axis/get/
weight: 60
keywords: "Hämta diagrammets andra kategoriaxel, Aspose.Cells Cloud API, Excel-diagramaxel, REST API, andra kategoriaxel, Aspose.Cells"
description: "Hämta den andra kategoriaxeln för ett diagram i ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar begäranformat, parametrar, exempel på cURL, svarschema, statuskoder och användningsnoteringar."
ArticleTitle: "Hämta diagrammets andra kategoriaxel – Aspose.Cells Cloud API"
---

Denna REST API hämtar **den andra kategoriaxeln** för ett diagram.

## GetChartSecondCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parametername   | Typ    | Parameterplats (path/query) | Beskrivning                                             |
| --------------- | ------ | --------------------------- | ------------------------------------------------------- |
| name            | string | path                        | Namnet på Excel-filen som lagras i molnet.              |
| sheetName       | string | path                        | Namnet på det kalkylblad som innehåller diagrammet.     |
| chartIndex      | integer| path                        | Nollbaserat index för diagrammet vars axel begärs.      |
| folder          | string | query                       | Mappsökväg i lagringen där filen finns.                 |
| storageName     | string | query                       | Namnet på Aspose Cloud-lagringen som ska användas (valfritt). |

### **Svar**

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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                     |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.   |
| 500 | Internal Server Error       | Oväntat serverfel.                                  |

## Hur du använder GetChartSecondCategoryAxis API med SDK:er

### GetChartSecondCategoryAxis API-specifikation

**Get-Chart-Second-Category-Axis**-åtgärden definieras i [OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) och möjliggör direkta REST-interaktioner från en webbläsare eller valfri HTTP-klient.

Du kan använda kommandoradsverktyget `cURL` för enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar API:et med `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att integrera detta API i ditt projekt. SDK:er hanterar detaljer på låg nivå såsom autentisering, begäranssammanställning och svarsparsetning, så att du kan fokusera på affärslogik. Se den fullständiga listan över Aspose.Cells Cloud SDK:er i [GitHub-förrådet](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur du anropar **Get Chart Second Category Axis**-åtgärden med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Konfigurera API-klient
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// Skapa begäran
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// Kör
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Axelns namn: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // Konfigurera API-klient
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // Skapa begäran
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // Kör
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Axelns namn: " + response.getAxis().getName());
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

// Konfigurera
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
    echo "Axelns namn: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Undantag vid anrop av ChartsApi->getChartSecondCategoryAxis: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# Konfigurera SDK
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
  puts "Axelns namn: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Undantag vid anrop av ChartsApi->get_chart_second_category_axis: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# Konfigurera API-klient
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
    print('Axelns namn:', response.axis.name)
except ApiException as e:
    print('Undantag vid anrop av ChartsApi->get_chart_second_category_axis:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js-exempel med Aspose.Cells Cloud SDK
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
        console.log('Axelns namn:', response.axis.name);
    } catch (error) {
        console.error('Fel:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android-exempel (Java) med Aspose.Cells Cloud SDK för Android
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
            System.out.println("Axelns namn: " + response.getAxis().getName());
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
        print("Axelns namn: \(axis.name ?? "")")
    } else if let err = error {
        print("Fel: \(err)")
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
print "Axelns namn: " . $response->axis->name . "\n";
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
        fmt.Println("Fel:", err)
        return
    }
    fmt.Println("Axelns namn:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}