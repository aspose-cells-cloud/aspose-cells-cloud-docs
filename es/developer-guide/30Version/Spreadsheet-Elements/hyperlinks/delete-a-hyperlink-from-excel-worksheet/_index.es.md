---
title: "Eliminar hipervínculo de hoja de cálculo"
type: docs
url: /es/hyperlinks/delete/
description: "Elimine un hipervínculo de hoja de cálculo por índice mediante la API de Aspose.Cells Cloud. Aprenda los parámetros requeridos, la autenticación y vea ejemplos de código para C#, Java, Python y más."
keywords: "Aspose.Cells, Cloud, eliminar hipervínculo, API de Excel, REST, hipervínculo de hoja de cálculo"
ArticleTitle: "Eliminar hipervínculo de hoja de cálculo – Documentación de la API de Aspose.Cells Cloud"
weight: 40
---

Esta API REST elimina un hipervínculo de hoja de cálculo por su índice en una hoja de cálculo de Excel.

## Seguridad y autenticación
Las API de Aspose.Cells Cloud son seguras y requieren [autenticación basada en tokens JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### API REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo    | Ubicación | Obligatorio | Descripción                                                   |
| ------------------- | ------- | --------- | ----------- | ------------------------------------------------------------- |
| **name**            | string  | path      | ✅          | Nombre del documento de Excel.                                |
| **sheetName**       | string  | path      | ✅          | Nombre de la hoja de cálculo.                                 |
| **hyperlinkIndex**  | integer | path      | ✅          | Índice de base cero del hipervínculo que se va a eliminar.   |
| **folder**          | string  | query     | ❌          | Carpeta que contiene el documento (valor predeterminado: raíz). |
| **storageName**     | string  | query     | ❌          | Nombre del servicio de almacenamiento (se usa el almacenamiento predeterminado si se omite). |

#### Respuestas

| Código de estado              | Descripción                                             | Cuerpo de ejemplo                                  |
| ----------------------------- | ------------------------------------------------------- | -------------------------------------------------- |
| **200 OK**                    | Hipervínculo eliminado correctamente.                   | `{"Code":200,"Status":"OK"}`                       |
| **400 Bad Request**           | Parámetros faltantes o no válidos.                      | `{"Code":400,"Message":"Índice de hipervínculo no válido."}` |
| **401 Unauthorized**          | Token de autenticación faltante o no válido.            | `{"Code":401,"Message":"Token de acceso no válido."}`   |
| **404 Not Found**             | El archivo, la hoja de cálculo o el índice del hipervínculo no existe. | `{"Code":404,"Message":"Recurso no encontrado."}`     |
| **500 Internal Server Error** | Error inesperado del servidor.                          | `{"Code":500,"Message":"Error interno del servidor."}`  |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlink) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo llamar a la API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la forma más rápida de desarrollar. Un SDK maneja los detalles de bajo nivel para que pueda centrarse en su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK. Se proporcionan fragmentos de código en línea para mayor confiabilidad; se mantiene un enlace al Gist original como referencia.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// ExampleDeleteWorksheetHyperlink.cs
// Fuente: https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("<client_id>", "<client_secret>");
var response = apiInstance.DeleteWorksheetHyperlink(
    name: "test1.xlsx",
    sheetName: "Sheet1",
    hyperlinkIndex: 0,
    folder: null,
    storageName: null);
Console.WriteLine(response.Status);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Example_DeleteWorksheetHyperlink.java
// Fuente: https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.*;

CellsApi api = new CellsApi("<client_id>", "<client_secret>");
ApiResponse<Void> response = api.deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
System.out.println("Estado: " + response.getStatusCode());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Example_DeleteWorksheetHyperlink.php
// Fuente: https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152
require_once('vendor/autoload.php');

$config = new Aspose\Cells\Configuration();
$config->setAppSid('<client_id>');
$config->setAppKey('<client_secret>');

$apiInstance = new Aspose\Cells\Api\CellsApi($config);
$response = $apiInstance->deleteWorksheetHyperlink(
    "test1.xlsx",
    "Sheet1",
    0,
    null,
    null);
echo $response->getStatusCode();
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Example_DeleteWorksheetHyperlink.rb
# Fuente: https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca
require 'aspose_cells_cloud'

api = AsposeCellsCloud::CellsApi.new('<client_id>', '<client_secret>')
result = api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
puts result.status
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```javascript
// Example_DeleteWorksheetHyperlink.ts (Node.js)
// Fuente: https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0
const AsposeCellsCloud = require("asposecellscloud");
const api = new AsposeCellsCloud.CellsApi("<client_id>", "<client_secret>");

api
  .deleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, null, null)
  .then(() => console.log("Hipervínculo eliminado"))
  .catch((err) => console.error(err));
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```python
# Example_DeleteWorksheetHyperlink.py
# Fuente: https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1
from asposecellscloud import CellsApi, Configuration

config = Configuration(app_sid='<client_id>', app_key='<client_secret>')
api = CellsApi(config)

api.delete_worksheet_hyperlink('test1.xlsx', 'Sheet1', 0)
print('Hipervínculo eliminado')
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```perl
# Example_DeleteWorksheetHyperlink.pl
# Fuente: https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca
use AsposeCellsCloud::CellsApi;

my $api_instance = AsposeCellsCloud::CellsApi->new('<client_id>', '<client_secret>');
my $result = $api_instance->delete_worksheet_hyperlink(
    name => 'test1.xlsx',
    sheet_name => 'Sheet1',
    hyperlink_index => 0);
print "Estado: $result->{status}\n";
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```go
// Example_DeleteWorksheetHyperlink.go
// Fuente: https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185
package main

import (
    "fmt"
    "github.com/asposecellscloud/asposecellscloud-go/v3"
)

func main() {
    config := asposecellscloud.NewConfiguration("<client_id>", "<client_secret>")
    api := asposecellscloud.NewAPIClient(config).CellsApi
    _, err := api.DeleteWorksheetHyperlink("test1.xlsx", "Sheet1", 0, nil, nil)
    if err != nil {
        fmt.Println(err)
    } else {
        fmt.Println("Hipervínculo eliminado")
    }
}
```

{{< /tab >}}

{{< /tabs >}}