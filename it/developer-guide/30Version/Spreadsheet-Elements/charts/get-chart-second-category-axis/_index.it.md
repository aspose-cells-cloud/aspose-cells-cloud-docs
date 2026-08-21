---
title: "Ottenere l'Asse Secondario di Categoria di un Grafico"
type: docs
url: /charts/second-category-axis/get/
weight: 60
keywords: "Ottenere l'Asse Secondario di Categoria di un Grafico, API Cloud Aspose.Cells, Asse grafico Excel, API REST, asse secondario di categoria, Aspose.Cells"
description: "Recupera l'asse secondario di categoria di un grafico in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Include il formato della richiesta, i parametri, un esempio cURL, lo schema di risposta, i codici di stato e note sull'uso."
ArticleTitle: "Ottenere l'Asse Secondario di Categoria di un Grafico – Aspose.Cells Cloud API"
---

Questa REST API recupera l'**asse secondario di categoria** di un grafico.

## GetChartSecondCategoryAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome Parametro | Tipo    | Posizione Parametro (path/query) | Descrizione                                             |
| -------------- | ------- | -------------------------------- | ------------------------------------------------------- |
| name           | string  | path                             | Nome del file Excel memorizzato nel cloud.              |
| sheetName      | string  | path                             | Nome del foglio di calcolo contenente il grafico.       |
| chartIndex     | integer | path                             | Indice in base zero del grafico il cui asse è richiesto.|
| folder         | string  | query                            | Percorso della cartella nella memoria dove si trova il file. |
| storageName    | string  | query                            | Nome della memoria Aspose Cloud da utilizzare (opzionale). |

### **Risposta**

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

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione.                            |
| 500  | Errore interno del server   | Errore imprevisto nel server.                                               |

## Come utilizzare l'API GetChartSecondCategoryAxis con gli SDK

### Specifica dell'API GetChartSecondCategoryAxis

L'operazione **Get-Chart-Second-Category-Axis** è definita nella [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) e consente interazioni REST dirette da un browser web o da qualsiasi client HTTP.

Puoi utilizzare lo strumento a riga di comando `cURL` per accedere facilmente ai servizi web di Aspose.Cells. Il seguente esempio mostra come chiamare l'API con `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

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

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per integrare questa API nel proprio progetto. Gli SDK gestiscono i dettagli di basso livello come l'autenticazione, la costruzione delle richieste e l'analisi delle risposte, consentendoti di concentrarti sulla logica di business. Consulta l'elenco completo degli SDK di Aspose.Cells Cloud nel [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice mostrano come chiamare l'operazione **Ottenere l'Asse Secondario di Categoria di un Grafico** con vari SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configura il client API
var config = new Configuration
{
    ClientId = "<il-tuo-client-id>",
    ClientSecret = "<il-tuo-client-secret>"
};
var apiInstance = new ChartsApi(config);

// Costruisci la richiesta
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// Esegui
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Nome asse: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // Configura il client API
        Configuration config = new Configuration();
        config.setClientId("<il-tuo-client-id>");
        config.setClientSecret("<il-tuo-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // Costruisci la richiesta
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // Esegui
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Nome asse: " + response.getAxis().getName());
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

// Configura
$config = new Configuration();
$config->setClientId('<il-tuo-client-id>');
$config->setClientSecret('<il-tuo-client-secret>');

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
    echo "Nome asse: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Eccezione durante la chiamata a ChartsApi->getChartSecondCategoryAxis: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# Configura SDK
config = AsposeCellsCloud::Configuration.new
config.client_id = '<il-tuo-client-id>'
config.client_secret = '<il-tuo-client-secret>'

api_instance = AsposeCellsCloud::ChartsApi.new

begin
  result = api_instance.get_chart_second_category_axis(
    name: 'Sample.xlsx',
    sheet_name: 'Sheet1',
    chart_index: 0,
    folder: 'Documents'
  )
  puts "Nome asse: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Eccezione durante la chiamata a ChartsApi->get_chart_second_category_axis: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# Configura il client API
config = asposecellscloud.Configuration()
config.client_id = '<il-tuo-client-id>'
config.client_secret = '<il-tuo-client-secret>'

api_instance = ChartsApi(asposecellscloud.ApiClient(config))

request = GetChartSecondCategoryAxisRequest(
    name='Sample.xlsx',
    sheet_name='Sheet1',
    chart_index=0,
    folder='Documents'
)

try:
    response = api_instance.get_chart_second_category_axis(request)
    print('Nome asse:', response.axis.name)
except ApiException as e:
    print('Eccezione durante la chiamata a ChartsApi->get_chart_second_category_axis:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Esempio Node.js che utilizza l'SDK di Aspose.Cells Cloud
const { ChartsApi, Configuration } = require('asposecellscloud');

const config = new Configuration({
    clientId: '<il-tuo-client-id>',
    clientSecret: '<il-tuo-client-secret>'
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
        console.log('Nome asse:', response.axis.name);
    } catch (error) {
        console.error('Errore:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Esempio Android (Java) che utilizza l'SDK di Aspose.Cells Cloud per Android
import com.aspose.cells.cloud.sdk.api.ChartsApi;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.model.requests.*;

public class GetSecondCategoryAxisAndroid {
    public void execute() {
        Configuration config = new Configuration();
        config.setClientId("<il-tuo-client-id>");
        config.setClientSecret("<il-tuo-client-secret>");

        ChartsApi api = new ChartsApi(config);
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        try {
            AxisResponse response = api.getChartSecondCategoryAxis(request);
            System.out.println("Nome asse: " + response.getAxis().getName());
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

let config = Configuration(clientId: "<il-tuo-client-id>", clientSecret: "<il-tuo-client-secret>")
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
        print("Nome asse: \(axis.name ?? "")")
    } else if let err = error {
        print("Errore: \(err)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
use Aspose::Cells::Cloud::Sdk::Api::ChartsApi;
use Aspose::Cells::Cloud::Sdk::Configuration;

my $config = Aspose::Cells::Cloud::Sdk::Configuration->new(
    client_id     => '<il-tuo-client-id>',
    client_secret => '<il-tuo-client-secret>'
);
my $api = Aspose::Cells::Cloud::Sdk::Api::ChartsApi->new($config);

my $response = $api->get_chart_second_category_axis(
    name        => 'Sample.xlsx',
    sheet_name  => 'Sheet1',
    chart_index => 0,
    folder      => 'Documents'
);
print "Nome asse: " . $response->axis->name . "\n";
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
    cfg.ClientId = "<il-tuo-client-id>"
    cfg.ClientSecret = "<il-tuo-client-secret>"

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
        fmt.Println("Errore:", err)
        return
    }
    fmt.Println("Nome asse:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}