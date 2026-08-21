---
title: "Zweite Kategorienachse eines Diagramms abrufen"
type: docs
url: /de/charts/second-category-axis/get/
weight: 60
keywords: "Zweite Kategorienachse eines Diagramms abrufen, Aspose.Cells Cloud API, Excel-Diagrammachse, REST API, zweite Kategorienachse, Aspose.Cells"
description: "Rufen Sie die zweite Kategorienachse eines Diagramms in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API ab. Enthält Anforderungsformat, Parameter, Beispiel-cURL, Antwortschema, HTTP-Statuscodes und Nutzungshinweise."
ArticleTitle: "Zweite Kategorienachse eines Diagramms abrufen – Aspose.Cells Cloud API"
---

Diese REST API ruft die **zweite Kategorienachse** eines Diagramms ab.

## GetChartSecondCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ    | Parameterposition (Pfad/Abfrage) | Beschreibung                                                |
| ------------- | ------ | -------------------------------- | ----------------------------------------------------------- |
| name          | string | path                             | Name der Excel-Datei, die in der Cloud gespeichert ist.     |
| sheetName     | string | path                             | Name des Arbeitsblatts, das das Diagramm enthält.          |
| chartIndex    | integer| path                             | Nullbasierter Index des Diagramms, dessen Achse abgerufen wird. |
| folder        | string | query                            | Ordnerpfad im Speicher, in dem sich die Datei befindet.    |
| storageName   | string | query                            | Name des Aspose Cloud-Speichers, der verwendet werden soll (optional). |

### **Antwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Zweite Kategorienachse",
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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails.           |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Wie man die GetChartSecondCategoryAxis API mit SDKs verwendet

### GetChartSecondCategoryAxis API-Spezifikation

Die **Get-Chart-Second-Category-Axis**-Operation ist in der [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) definiert und ermöglicht direkte REST-Interaktionen über einen Webbrowser oder jeden HTTP-Client.

Sie können das Kommandozeilentool `cURL` verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die API mit `cURL` aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

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
    "Name": "Zweite Kategorienachse",
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

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Methode, um diese API in Ihr Projekt zu integrieren. SDKs übernehmen Details auf unterster Ebene wie Authentifizierung, Anforderungserstellung und Antwortparsen, sodass Sie sich auf die Geschäftslogik konzentrieren können. Die vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie die **Get Chart Second Category Axis**-Operation mit verschiedenen SDKs aufgerufen wird:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// API-Client konfigurieren
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// Anforderung erstellen
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// Ausführen
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Achsenname: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // API-Client konfigurieren
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // Anforderung erstellen
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // Ausführen
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Achsenname: " + response.getAxis().getName());
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

// Konfigurieren
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
    echo "Achsenname: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Exception beim Aufrufen von ChartsApi->getChartSecondCategoryAxis: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# SDK konfigurieren
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
  puts "Achsenname: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Fehler beim Aufrufen von ChartsApi->get_chart_second_category_axis: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# API-Client konfigurieren
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
    print('Achsenname:', response.axis.name)
except ApiException as e:
    print('Fehler beim Aufrufen von ChartsApi->get_chart_second_category_axis:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js-Beispiel mit dem Aspose.Cells Cloud SDK
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
        console.log('Achsenname:', response.axis.name);
    } catch (error) {
        console.error('Fehler:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android-(Java-)Beispiel mit dem Aspose.Cells Cloud SDK für Android
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
            System.out.println("Achsenname: " + response.getAxis().getName());
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
        print("Achsenname: \(axis.name ?? "")")
    } else if let err = error {
        print("Fehler: \(err)")
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
print "Achsenname: " . $response->axis->name . "\n";
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
        fmt.Println("Fehler:", err)
        return
    }
    fmt.Println("Achsenname:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}