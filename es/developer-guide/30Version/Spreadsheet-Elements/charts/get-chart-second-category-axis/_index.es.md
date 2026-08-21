---
title: "Obtener el eje de categoría secundaria de un gráfico"
type: docs
url: /charts/second-category-axis/get/
weight: 60
keywords: "Obtener el eje de categoría secundaria de un gráfico, Aspose.Cells Cloud API, eje de gráfico de Excel, API REST, eje de categoría secundaria, Aspose.Cells"
description: "Recuperar el eje de categoría secundaria de un gráfico en una hoja de cálculo de Excel mediante la API REST de Aspose.Cells Cloud. Incluye el formato de solicitud, parámetros, ejemplo con cURL, esquema de respuesta, códigos de estado y notas de uso."
ArticleTitle: "Obtener el eje de categoría secundaria de un gráfico – Aspose.Cells Cloud API"
---

Esta API REST recupera el **eje de categoría secundaria** de un gráfico.

## API GetChartSecondCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación del parámetro (ruta / consulta) | Descripción                                                  |
| -------------------- | ------- | ----------------------------------------- | ------------------------------------------------------------ |
| name                 | string  | path                                      | Nombre del archivo de Excel almacenado en la nube.          |
| sheetName            | string  | path                                      | Nombre de la hoja de cálculo que contiene el gráfico.       |
| chartIndex           | integer | path                                      | Índice basado en cero del gráfico cuyo eje se solicita.      |
| folder               | string  | query                                     | Ruta de la carpeta en el almacenamiento donde se encuentra el archivo. |
| storageName          | string  | query                                     | Nombre del almacenamiento de Aspose Cloud a utilizar (opcional). |

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "Name": "Eje de categoría secundaria",
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

**Códigos de estado HTTP**

| Código | Significado                 | Descripción                                                  |
|--------|-----------------------------|--------------------------------------------------------------|
| 200    | OK                          | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta        | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado               | Token JWT inválido o ausente.                                |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.                |
| 500    | Error interno del servidor  | Error inesperado en el servidor.                             |

## Cómo usar la API GetChartSecondCategoryAxis con SDK

### Especificación de la API GetChartSecondCategoryAxis

La operación **Get-Chart-Second-Category-Axis** está definida en la [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondCategoryAxis) y permite interacciones REST directas desde un navegador web o cualquier cliente HTTP.

Puede utilizar la herramienta de línea de comandos `cURL` para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API con `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

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
    "Name": "Eje de categoría secundaria",
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

### Uso de los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de integrar esta API en su proyecto. Los SDK gestionan los detalles de bajo nivel, como autenticación, construcción de solicitudes y análisis de respuestas, permitiéndole centrarse en la lógica de negocio. Consulte la lista completa de SDK de Aspose.Cells Cloud en el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo llamar a la operación **Obtener el eje de categoría secundaria de un gráfico** con distintos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Configurar cliente API
var config = new Configuration
{
    ClientId = "<your-client-id>",
    ClientSecret = "<your-client-secret>"
};
var apiInstance = new ChartsApi(config);

// Construir solicitud
var request = new GetChartSecondCategoryAxisRequest(
    name: "Sample.xlsx",
    sheetName: "Sheet1",
    chartIndex: 0,
    folder: "Documents",
    storageName: null
);

// Ejecutar
var response = apiInstance.GetChartSecondCategoryAxis(request);
Console.WriteLine($"Nombre del eje: {response.Axis.Name}");
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
import com.aspose.cells.cloud.api.ChartsApi;
import com.aspose.cells.cloud.model.*;
import com.aspose.cells.cloud.model.requests.*;

public class GetSecondCategoryAxis {
    public static void main(String[] args) {
        // Configurar cliente API
        Configuration config = new Configuration();
        config.setClientId("<your-client-id>");
        config.setClientSecret("<your-client-secret>");

        ChartsApi api = new ChartsApi(config);

        // Construir solicitud
        GetChartSecondCategoryAxisRequest request = new GetChartSecondCategoryAxisRequest(
                "Sample.xlsx", "Sheet1", 0, "Documents", null);

        // Ejecutar
        AxisResponse response = api.getChartSecondCategoryAxis(request);
        System.out.println("Nombre del eje: " + response.getAxis().getName());
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

// Configurar
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
    echo "Nombre del eje: " . $result->getAxis()->getName();
} catch (Exception $e) {
    echo 'Excepción al llamar a ChartsApi->getChartSecondCategoryAxis: ', $e->getMessage(), PHP_EOL;
}
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
require 'aspose_cells_cloud'

# Configurar SDK
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
  puts "Nombre del eje: #{result.axis.name}"
rescue AsposeCellsCloud::ApiError => e
  puts "Excepción al llamar a ChartsApi->get_chart_second_category_axis: #{e}"
end
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
import asposecellscloud
from asposecellscloud.rest import ApiException
from asposecellscloud.apis.charts_api import ChartsApi
from asposecellscloud.models import GetChartSecondCategoryAxisRequest

# Configurar cliente API
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
    print('Nombre del eje:', response.axis.name)
except ApiException as e:
    print('Excepción al llamar a ChartsApi->get_chart_second_category_axis:', e)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Ejemplo en Node.js usando el SDK de Aspose.Cells Cloud
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
        console.log('Nombre del eje:', response.axis.name);
    } catch (error) {
        console.error('Error:', error);
    }
})();
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Ejemplo en Android (Java) usando el SDK de Aspose.Cells Cloud para Android
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
            System.out.println("Nombre del eje: " + response.getAxis().getName());
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
        print("Nombre del eje: \(axis.name ?? "")")
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
print "Nombre del eje: " . $response->axis->name . "\n";
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
    fmt.Println("Nombre del eje:", result.Axis.Name)
}
```

{{< /tab >}}

{{< /tabs >}}