---
title: "Obtener el título de un gráfico desde una hoja de cálculo"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Chart Title"
  - "Excel"
  - "REST API"
  - "Get Chart Title"
  - "cURL"
  - "SDK"
  - "Excel chart automation"
  - "GET chart title"
description: "Aprenda cómo recuperar el título de un gráfico desde una hoja de cálculo de Excel usando la API REST de Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, autenticación y ejemplos de código con cURL y SDK."
ArticleTitle: "Obtener el título de un gráfico desde una hoja de cálculo"
---

Esta API REST recupera el título de un gráfico almacenado en una hoja de cálculo de un libro de Excel.

**Prerrequisitos**: Para llamar a este punto de conexión debe tener un token de acceso válido de Aspose.Cells Cloud OAuth2/JWT con el ámbito `Cells.Read`. El libro ya debe haberse cargado en la ubicación de almacenamiento especificada.

## API GetWorksheetChartTitle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de solicitud

| Nombre del parámetro | Tipo    | Ubicación | Descripción                                      |
| --------------------- | ------- | --------- | ------------------------------------------------ |
| name                  | string  | path      | Nombre del archivo del libro.                    |
| sheetName             | string  | path      | Nombre de la hoja de cálculo que contiene el gráfico. |
| chartIndex            | integer | path      | Índice de base cero del gráfico.                 |
| folder                | string  | query     | Ruta de carpeta donde se almacena el libro.     |
| storageName           | string  | query     | Nombre del servicio de almacenamiento.          |

La [Especificación de OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos **cURL** para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar una llamada a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Ventas Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Campos de respuesta**

| Campo               | Descripción                                      |
| ------------------- | ------------------------------------------------ |
| `Title.Text`        | El texto real que se muestra como título del gráfico. |
| `Title.Font.Name`   | Familia tipográfica utilizada para el título (por ejemplo, *Arial*). |
| `Title.Font.Size`   | Tamaño de fuente en puntos.                      |
| `Title.Font.IsBold` | Indica si el texto del título está en negrita.   |

**Códigos de estado de respuesta**

| Código | Descripción |
|--------|-------------|
| 200 OK | El título del gráfico se recuperó correctamente. |
| 401 Unauthorized | La autenticación falló o el token falta o no es válido. |
| 404 Not Found | El libro, la hoja de cálculo o el gráfico especificados no existen. |
| 500 Internal Server Error | Ocurrió un error inesperado en el servidor. |

**Notas**: El índice del gráfico es de base cero; asegúrese de que el gráfico exista. Si el libro no se ha cargado, cárguelo primero mediante la API correspondiente.

**Cómo extraer el título en un script (usando `jq`)**

```bash
# Suponiendo que la respuesta JSON se guarda en response.json
title=$(jq -r '.Title.Text' response.json)
echo "Título del gráfico: $title"
```

## Familia de SDK en la nube

Utilizar un SDK es la mejor manera de acelerar el desarrollo. Un SDK gestiona los detalles de bajo nivel para que usted se enfoque en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Ejemplo en C# usando el SDK de Aspose.Cells Cloud
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Ejemplo en Java usando el SDK de Aspose.Cells Cloud
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Ejemplo en PHP usando el SDK de Aspose.Cells Cloud
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ejemplo en Ruby usando el SDK de Aspose.Cells Cloud
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Ejemplo en Python usando el SDK de Aspose.Cells Cloud
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Ejemplo en Node.js usando el SDK de Aspose.Cells Cloud
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Ejemplo en Android (Java) usando el SDK de Aspose.Cells Cloud
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Ejemplo en Swift usando el SDK de Aspose.Cells Cloud
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Título del gráfico: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Ejemplo en Perl usando el SDK de Aspose.Cells Cloud
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

También puede consultar la documentación individual del SDK para escenarios más avanzados, como actualizar o eliminar un título de gráfico.

**Consulte también**: [Actualizar el título de un gráfico](/charts/title/put/), [Eliminar el título de un gráfico](/charts/title/delete/).
---